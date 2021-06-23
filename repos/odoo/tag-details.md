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
$ docker pull odoo@sha256:a9c037f53c07c0ae0f2c7ab5c0ed1e3934a2e7002565e4e7c1e9e3b4257b0e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:bf8a59626bcd8b68507e6eb2d07d9baffc63fa540caf302dac1dddb2cb0f39bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538363370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10500b2967685971ff16de1877b1194857f784fbb23b9f8bf72a8f5c08ceb69`
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
# Wed, 23 Jun 2021 07:54:14 GMT
ARG ODOO_RELEASE=20210618
# Wed, 23 Jun 2021 07:54:14 GMT
ARG ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
# Wed, 23 Jun 2021 07:55:20 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 23 Jun 2021 07:55:21 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 23 Jun 2021 07:55:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 23 Jun 2021 07:55:23 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 23 Jun 2021 07:55:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 23 Jun 2021 07:55:23 GMT
EXPOSE 8069 8071 8072
# Wed, 23 Jun 2021 07:55:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 23 Jun 2021 07:55:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 23 Jun 2021 07:55:24 GMT
USER odoo
# Wed, 23 Jun 2021 07:55:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jun 2021 07:55:24 GMT
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
	-	`sha256:560609a0b5c83bc51ce89e814fd4768e4afa10f38b7b47a372776d94ccdf1769`  
		Last Modified: Wed, 23 Jun 2021 07:58:38 GMT  
		Size: 271.9 MB (271926002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeb507b6a5d113b9a325b4df76b673fd86de55731b39095f90d5a7d522ef4a8`  
		Last Modified: Wed, 23 Jun 2021 07:57:56 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd641daa8363a27bc61dec885551d796def80bf596b2be75be755329ca912e`  
		Last Modified: Wed, 23 Jun 2021 07:57:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6c0fc016b914f73391ac14bbf9b39e2c984e6342b0dd0048c279b3368643ed`  
		Last Modified: Wed, 23 Jun 2021 07:57:56 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0967bbf2e826a19575cb50a99689418e77bf7622f005ca286806c1e97391d35d`  
		Last Modified: Wed, 23 Jun 2021 07:57:56 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:a9c037f53c07c0ae0f2c7ab5c0ed1e3934a2e7002565e4e7c1e9e3b4257b0e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:bf8a59626bcd8b68507e6eb2d07d9baffc63fa540caf302dac1dddb2cb0f39bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538363370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10500b2967685971ff16de1877b1194857f784fbb23b9f8bf72a8f5c08ceb69`
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
# Wed, 23 Jun 2021 07:54:14 GMT
ARG ODOO_RELEASE=20210618
# Wed, 23 Jun 2021 07:54:14 GMT
ARG ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
# Wed, 23 Jun 2021 07:55:20 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 23 Jun 2021 07:55:21 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 23 Jun 2021 07:55:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 23 Jun 2021 07:55:23 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 23 Jun 2021 07:55:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 23 Jun 2021 07:55:23 GMT
EXPOSE 8069 8071 8072
# Wed, 23 Jun 2021 07:55:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 23 Jun 2021 07:55:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 23 Jun 2021 07:55:24 GMT
USER odoo
# Wed, 23 Jun 2021 07:55:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jun 2021 07:55:24 GMT
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
	-	`sha256:560609a0b5c83bc51ce89e814fd4768e4afa10f38b7b47a372776d94ccdf1769`  
		Last Modified: Wed, 23 Jun 2021 07:58:38 GMT  
		Size: 271.9 MB (271926002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeb507b6a5d113b9a325b4df76b673fd86de55731b39095f90d5a7d522ef4a8`  
		Last Modified: Wed, 23 Jun 2021 07:57:56 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd641daa8363a27bc61dec885551d796def80bf596b2be75be755329ca912e`  
		Last Modified: Wed, 23 Jun 2021 07:57:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6c0fc016b914f73391ac14bbf9b39e2c984e6342b0dd0048c279b3368643ed`  
		Last Modified: Wed, 23 Jun 2021 07:57:56 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0967bbf2e826a19575cb50a99689418e77bf7622f005ca286806c1e97391d35d`  
		Last Modified: Wed, 23 Jun 2021 07:57:56 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:87e4ed6f28c46310b11bdfba35ed0a9deccacc63b44d945cdd7acbb4daa974ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:f53dc1f59b57f58398996b094fb3cc0ddc8c0532e63ebac59332d8ff27575e4b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.2 MB (528188491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae6927c69af84d1da9ef36424e6515a700769c58861a92acc3c4ae20306c207`
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
# Wed, 23 Jun 2021 07:49:53 GMT
ARG ODOO_RELEASE=20210618
# Wed, 23 Jun 2021 07:49:54 GMT
ARG ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
# Wed, 23 Jun 2021 07:51:31 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 23 Jun 2021 07:51:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 23 Jun 2021 07:51:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 23 Jun 2021 07:51:36 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 23 Jun 2021 07:51:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 23 Jun 2021 07:51:37 GMT
EXPOSE 8069 8071 8072
# Wed, 23 Jun 2021 07:51:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 23 Jun 2021 07:51:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 23 Jun 2021 07:51:38 GMT
USER odoo
# Wed, 23 Jun 2021 07:51:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jun 2021 07:51:38 GMT
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
	-	`sha256:8d54e607c84570bc58cb97ba8a906e315001d1fcabf5a6d68824470cc6642a8f`  
		Last Modified: Wed, 23 Jun 2021 07:57:42 GMT  
		Size: 290.7 MB (290685427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b26a20ec11b2f0b8830982598e3060d141d91a96012146368f938697b6474`  
		Last Modified: Wed, 23 Jun 2021 07:57:00 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8965e43693a7f7a79241a7ee8ad79389856e1b0d19ee7e187226fd4df8112b0f`  
		Last Modified: Wed, 23 Jun 2021 07:57:00 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b2f04e335f12bdec53306642748d85691a72cdc5eb00e9cc3d176662a167b0`  
		Last Modified: Wed, 23 Jun 2021 07:57:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9de620069d6f2191a31b99c1d2b78e18c84dd3c900712ad271b0d39fe10f39`  
		Last Modified: Wed, 23 Jun 2021 07:57:00 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:87e4ed6f28c46310b11bdfba35ed0a9deccacc63b44d945cdd7acbb4daa974ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:f53dc1f59b57f58398996b094fb3cc0ddc8c0532e63ebac59332d8ff27575e4b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.2 MB (528188491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae6927c69af84d1da9ef36424e6515a700769c58861a92acc3c4ae20306c207`
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
# Wed, 23 Jun 2021 07:49:53 GMT
ARG ODOO_RELEASE=20210618
# Wed, 23 Jun 2021 07:49:54 GMT
ARG ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
# Wed, 23 Jun 2021 07:51:31 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 23 Jun 2021 07:51:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 23 Jun 2021 07:51:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 23 Jun 2021 07:51:36 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 23 Jun 2021 07:51:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 23 Jun 2021 07:51:37 GMT
EXPOSE 8069 8071 8072
# Wed, 23 Jun 2021 07:51:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 23 Jun 2021 07:51:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 23 Jun 2021 07:51:38 GMT
USER odoo
# Wed, 23 Jun 2021 07:51:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jun 2021 07:51:38 GMT
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
	-	`sha256:8d54e607c84570bc58cb97ba8a906e315001d1fcabf5a6d68824470cc6642a8f`  
		Last Modified: Wed, 23 Jun 2021 07:57:42 GMT  
		Size: 290.7 MB (290685427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b26a20ec11b2f0b8830982598e3060d141d91a96012146368f938697b6474`  
		Last Modified: Wed, 23 Jun 2021 07:57:00 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8965e43693a7f7a79241a7ee8ad79389856e1b0d19ee7e187226fd4df8112b0f`  
		Last Modified: Wed, 23 Jun 2021 07:57:00 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b2f04e335f12bdec53306642748d85691a72cdc5eb00e9cc3d176662a167b0`  
		Last Modified: Wed, 23 Jun 2021 07:57:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9de620069d6f2191a31b99c1d2b78e18c84dd3c900712ad271b0d39fe10f39`  
		Last Modified: Wed, 23 Jun 2021 07:57:00 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:7de567fdf445247234966998c646b7008dc6cac97ac6fe3f59f87c8e5a030fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:974b58c219c826775aa608500af0c0ba0b00ec38cc43fb81232ca184041b26ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.2 MB (514243483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8542a70ba613340d6aa4689718dc6d9c79fd637de7fd9da71c7f993234fff89f`
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
# Wed, 23 Jun 2021 07:46:34 GMT
ARG ODOO_RELEASE=20210618
# Wed, 23 Jun 2021 07:46:35 GMT
ARG ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
# Wed, 23 Jun 2021 07:48:04 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 23 Jun 2021 07:48:08 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 23 Jun 2021 07:48:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 23 Jun 2021 07:48:10 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 23 Jun 2021 07:48:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 23 Jun 2021 07:48:10 GMT
EXPOSE 8069 8071 8072
# Wed, 23 Jun 2021 07:48:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 23 Jun 2021 07:48:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 23 Jun 2021 07:48:11 GMT
USER odoo
# Wed, 23 Jun 2021 07:48:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jun 2021 07:48:12 GMT
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
	-	`sha256:e8bc8abecbdc04a5d0303e1e6dc8fac565e54e6c649494551ed32081d337c669`  
		Last Modified: Wed, 23 Jun 2021 07:56:45 GMT  
		Size: 270.7 MB (270688492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9097117f7273fa2d9cac337082546669b2b9953335276d23278b4617888b12`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2944cbd19a110fc0b58b5bfdad50d8a67bceda86864b6cea4cb66ab9f157da`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03b3d7f8c796e7827b8d84364985b4e0cc67661234a9616cb83120399a2b9fc`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfd9a8d36647ec0e450bfd3c67c1e1a9649c7ff0ab1fb9f8bfd27504cd5549e`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:7de567fdf445247234966998c646b7008dc6cac97ac6fe3f59f87c8e5a030fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:974b58c219c826775aa608500af0c0ba0b00ec38cc43fb81232ca184041b26ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.2 MB (514243483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8542a70ba613340d6aa4689718dc6d9c79fd637de7fd9da71c7f993234fff89f`
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
# Wed, 23 Jun 2021 07:46:34 GMT
ARG ODOO_RELEASE=20210618
# Wed, 23 Jun 2021 07:46:35 GMT
ARG ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
# Wed, 23 Jun 2021 07:48:04 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 23 Jun 2021 07:48:08 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 23 Jun 2021 07:48:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 23 Jun 2021 07:48:10 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 23 Jun 2021 07:48:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 23 Jun 2021 07:48:10 GMT
EXPOSE 8069 8071 8072
# Wed, 23 Jun 2021 07:48:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 23 Jun 2021 07:48:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 23 Jun 2021 07:48:11 GMT
USER odoo
# Wed, 23 Jun 2021 07:48:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jun 2021 07:48:12 GMT
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
	-	`sha256:e8bc8abecbdc04a5d0303e1e6dc8fac565e54e6c649494551ed32081d337c669`  
		Last Modified: Wed, 23 Jun 2021 07:56:45 GMT  
		Size: 270.7 MB (270688492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9097117f7273fa2d9cac337082546669b2b9953335276d23278b4617888b12`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2944cbd19a110fc0b58b5bfdad50d8a67bceda86864b6cea4cb66ab9f157da`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03b3d7f8c796e7827b8d84364985b4e0cc67661234a9616cb83120399a2b9fc`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfd9a8d36647ec0e450bfd3c67c1e1a9649c7ff0ab1fb9f8bfd27504cd5549e`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:7de567fdf445247234966998c646b7008dc6cac97ac6fe3f59f87c8e5a030fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:974b58c219c826775aa608500af0c0ba0b00ec38cc43fb81232ca184041b26ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.2 MB (514243483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8542a70ba613340d6aa4689718dc6d9c79fd637de7fd9da71c7f993234fff89f`
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
# Wed, 23 Jun 2021 07:46:34 GMT
ARG ODOO_RELEASE=20210618
# Wed, 23 Jun 2021 07:46:35 GMT
ARG ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
# Wed, 23 Jun 2021 07:48:04 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 23 Jun 2021 07:48:08 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 23 Jun 2021 07:48:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 23 Jun 2021 07:48:10 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 23 Jun 2021 07:48:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 23 Jun 2021 07:48:10 GMT
EXPOSE 8069 8071 8072
# Wed, 23 Jun 2021 07:48:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 23 Jun 2021 07:48:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 23 Jun 2021 07:48:11 GMT
USER odoo
# Wed, 23 Jun 2021 07:48:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jun 2021 07:48:12 GMT
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
	-	`sha256:e8bc8abecbdc04a5d0303e1e6dc8fac565e54e6c649494551ed32081d337c669`  
		Last Modified: Wed, 23 Jun 2021 07:56:45 GMT  
		Size: 270.7 MB (270688492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9097117f7273fa2d9cac337082546669b2b9953335276d23278b4617888b12`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2944cbd19a110fc0b58b5bfdad50d8a67bceda86864b6cea4cb66ab9f157da`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03b3d7f8c796e7827b8d84364985b4e0cc67661234a9616cb83120399a2b9fc`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfd9a8d36647ec0e450bfd3c67c1e1a9649c7ff0ab1fb9f8bfd27504cd5549e`  
		Last Modified: Wed, 23 Jun 2021 07:55:45 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
