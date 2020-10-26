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
$ docker pull odoo@sha256:5052ae73998844d9943e0541b05499e7454ef028d7dbb4a19a6ff52a4548cace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:6663f3c1af03cd67861174689e776130f398031a5c981b0a1ba9ae2ebe25271d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 MB (396807500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3aab04da7cfe893d47d2c9fb1a9ef8fc363b4f122764daa2e587a439fde64be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:55:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:55:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:55:34 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:55:36 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 13 Oct 2020 17:57:56 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Oct 2020 17:58:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:58:19 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:58:19 GMT
ENV ODOO_VERSION=12.0
# Mon, 26 Oct 2020 17:49:33 GMT
ARG ODOO_RELEASE=20201026
# Mon, 26 Oct 2020 17:49:33 GMT
ARG ODOO_SHA=848d079fdfa76f57bd742c3385096d6743c9532e
# Mon, 26 Oct 2020 17:50:29 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=848d079fdfa76f57bd742c3385096d6743c9532e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 26 Oct 2020 17:50:30 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 26 Oct 2020 17:50:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 26 Oct 2020 17:50:31 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=848d079fdfa76f57bd742c3385096d6743c9532e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 26 Oct 2020 17:50:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Oct 2020 17:50:31 GMT
EXPOSE 8069 8071 8072
# Mon, 26 Oct 2020 17:50:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Oct 2020 17:50:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 26 Oct 2020 17:50:32 GMT
USER odoo
# Mon, 26 Oct 2020 17:50:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Oct 2020 17:50:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e899471950fb23135e6e3ba4bf5e7d333956a9c8fefef201edb318f76ce8a`  
		Last Modified: Tue, 13 Oct 2020 18:03:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469473cc24d8d8f285e28db154936eb275da7e3a962ebb2fb2f6008212d92a36`  
		Last Modified: Tue, 13 Oct 2020 18:04:13 GMT  
		Size: 219.6 MB (219609741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c32bdce53191bc591f6a2ef86c27ad27c001afe93d12b1b168c7a49d0c8cf79`  
		Last Modified: Tue, 13 Oct 2020 18:03:26 GMT  
		Size: 2.4 MB (2430770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd870da114a745cbea66677bec90b500570bdfbd3c22ad988b098c8fb150963f`  
		Last Modified: Tue, 13 Oct 2020 18:03:31 GMT  
		Size: 22.3 MB (22262444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd9e4e85442ac43c234d9070ee63ea574c6f429d4fd370bda467cb21205462`  
		Last Modified: Mon, 26 Oct 2020 17:52:51 GMT  
		Size: 130.0 MB (129979816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd81e14b527645e77b654e15d56c3e74161d4f47b59ad2736ec366b8cb1e026`  
		Last Modified: Mon, 26 Oct 2020 17:52:18 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a3b813bda17baff0123e37940371656e6c7841a768d11e5606468ee82be605`  
		Last Modified: Mon, 26 Oct 2020 17:52:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd6a0cc35acfc3f6b393c038c039dba7543ad657a47e3edefd9ab08266a1610`  
		Last Modified: Mon, 26 Oct 2020 17:52:18 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62543f4e2f716adb398fd5114bad7455d1ebc0b3caa976eecb6d23c0aa40987`  
		Last Modified: Mon, 26 Oct 2020 17:52:18 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:5052ae73998844d9943e0541b05499e7454ef028d7dbb4a19a6ff52a4548cace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:6663f3c1af03cd67861174689e776130f398031a5c981b0a1ba9ae2ebe25271d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 MB (396807500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3aab04da7cfe893d47d2c9fb1a9ef8fc363b4f122764daa2e587a439fde64be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:55:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:55:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:55:34 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:55:36 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 13 Oct 2020 17:57:56 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Oct 2020 17:58:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:58:19 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:58:19 GMT
ENV ODOO_VERSION=12.0
# Mon, 26 Oct 2020 17:49:33 GMT
ARG ODOO_RELEASE=20201026
# Mon, 26 Oct 2020 17:49:33 GMT
ARG ODOO_SHA=848d079fdfa76f57bd742c3385096d6743c9532e
# Mon, 26 Oct 2020 17:50:29 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=848d079fdfa76f57bd742c3385096d6743c9532e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 26 Oct 2020 17:50:30 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 26 Oct 2020 17:50:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 26 Oct 2020 17:50:31 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=848d079fdfa76f57bd742c3385096d6743c9532e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 26 Oct 2020 17:50:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Oct 2020 17:50:31 GMT
EXPOSE 8069 8071 8072
# Mon, 26 Oct 2020 17:50:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Oct 2020 17:50:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 26 Oct 2020 17:50:32 GMT
USER odoo
# Mon, 26 Oct 2020 17:50:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Oct 2020 17:50:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e899471950fb23135e6e3ba4bf5e7d333956a9c8fefef201edb318f76ce8a`  
		Last Modified: Tue, 13 Oct 2020 18:03:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469473cc24d8d8f285e28db154936eb275da7e3a962ebb2fb2f6008212d92a36`  
		Last Modified: Tue, 13 Oct 2020 18:04:13 GMT  
		Size: 219.6 MB (219609741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c32bdce53191bc591f6a2ef86c27ad27c001afe93d12b1b168c7a49d0c8cf79`  
		Last Modified: Tue, 13 Oct 2020 18:03:26 GMT  
		Size: 2.4 MB (2430770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd870da114a745cbea66677bec90b500570bdfbd3c22ad988b098c8fb150963f`  
		Last Modified: Tue, 13 Oct 2020 18:03:31 GMT  
		Size: 22.3 MB (22262444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd9e4e85442ac43c234d9070ee63ea574c6f429d4fd370bda467cb21205462`  
		Last Modified: Mon, 26 Oct 2020 17:52:51 GMT  
		Size: 130.0 MB (129979816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd81e14b527645e77b654e15d56c3e74161d4f47b59ad2736ec366b8cb1e026`  
		Last Modified: Mon, 26 Oct 2020 17:52:18 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a3b813bda17baff0123e37940371656e6c7841a768d11e5606468ee82be605`  
		Last Modified: Mon, 26 Oct 2020 17:52:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd6a0cc35acfc3f6b393c038c039dba7543ad657a47e3edefd9ab08266a1610`  
		Last Modified: Mon, 26 Oct 2020 17:52:18 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62543f4e2f716adb398fd5114bad7455d1ebc0b3caa976eecb6d23c0aa40987`  
		Last Modified: Mon, 26 Oct 2020 17:52:18 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:2e7f3575562b11689fd54db9e47bc17ff76291d0a92b3a47d4b1a3d67c603c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:7860fc88c019e29b84a97d2fd006021ef55a10c5b0911bcd2c6e40610f829ed6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (386016861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8ca41af2c832287c797cf5a631ad74f3a76767ef9ca12bbf5a75dfec476060`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Mon, 26 Oct 2020 17:47:59 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Mon, 26 Oct 2020 17:48:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Mon, 26 Oct 2020 17:48:12 GMT
RUN npm install -g rtlcss
# Mon, 26 Oct 2020 17:48:12 GMT
ENV ODOO_VERSION=13.0
# Mon, 26 Oct 2020 17:48:13 GMT
ARG ODOO_RELEASE=20201026
# Mon, 26 Oct 2020 17:48:13 GMT
ARG ODOO_SHA=d3f043345c04674bba81762d0afd88dab52aab36
# Mon, 26 Oct 2020 17:49:19 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=d3f043345c04674bba81762d0afd88dab52aab36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 26 Oct 2020 17:49:20 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 26 Oct 2020 17:49:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 26 Oct 2020 17:49:21 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=d3f043345c04674bba81762d0afd88dab52aab36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 26 Oct 2020 17:49:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Oct 2020 17:49:22 GMT
EXPOSE 8069 8071 8072
# Mon, 26 Oct 2020 17:49:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Oct 2020 17:49:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 26 Oct 2020 17:49:23 GMT
USER odoo
# Mon, 26 Oct 2020 17:49:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Oct 2020 17:49:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086dfd04ee4f09e3759168af225fb6366b6e33e604235abf1da4e3aea207c9d8`  
		Last Modified: Mon, 26 Oct 2020 17:52:13 GMT  
		Size: 207.1 MB (207077082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab0ca83605acca7d829847eac227f94f377dab01aae73e84e2a3496b2ea03f9`  
		Last Modified: Mon, 26 Oct 2020 17:51:36 GMT  
		Size: 2.4 MB (2432974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4997f88b88be6c179a0d473e2f0e9d90ee165e3a84cc19f956c383f31eb8e7b9`  
		Last Modified: Mon, 26 Oct 2020 17:51:35 GMT  
		Size: 1.1 MB (1118722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9248837ddaf17f82e79802675267956f2677c4597424a70d20e4678f1230d9cf`  
		Last Modified: Mon, 26 Oct 2020 17:52:12 GMT  
		Size: 148.3 MB (148293462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b415321b39c882a09388b258fd89a03ad61a723564994944a688d47f6e3576`  
		Last Modified: Mon, 26 Oct 2020 17:51:34 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0d32f4ada70f0c1d7287ddc857dbc1a16acfde7b37ef3a9977513c5611fa00`  
		Last Modified: Mon, 26 Oct 2020 17:51:35 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8971ccfac10acd1895f9f536d3c2708f0e20688ba81caa091d3972f888cddbfc`  
		Last Modified: Mon, 26 Oct 2020 17:51:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b209ecf5ab89d4ceaac437ed0e9a13ff4e785b0606f49476faf2c8d37d4b9`  
		Last Modified: Mon, 26 Oct 2020 17:51:35 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:2e7f3575562b11689fd54db9e47bc17ff76291d0a92b3a47d4b1a3d67c603c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:7860fc88c019e29b84a97d2fd006021ef55a10c5b0911bcd2c6e40610f829ed6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (386016861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8ca41af2c832287c797cf5a631ad74f3a76767ef9ca12bbf5a75dfec476060`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Mon, 26 Oct 2020 17:47:59 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Mon, 26 Oct 2020 17:48:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Mon, 26 Oct 2020 17:48:12 GMT
RUN npm install -g rtlcss
# Mon, 26 Oct 2020 17:48:12 GMT
ENV ODOO_VERSION=13.0
# Mon, 26 Oct 2020 17:48:13 GMT
ARG ODOO_RELEASE=20201026
# Mon, 26 Oct 2020 17:48:13 GMT
ARG ODOO_SHA=d3f043345c04674bba81762d0afd88dab52aab36
# Mon, 26 Oct 2020 17:49:19 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=d3f043345c04674bba81762d0afd88dab52aab36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 26 Oct 2020 17:49:20 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 26 Oct 2020 17:49:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 26 Oct 2020 17:49:21 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=d3f043345c04674bba81762d0afd88dab52aab36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 26 Oct 2020 17:49:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Oct 2020 17:49:22 GMT
EXPOSE 8069 8071 8072
# Mon, 26 Oct 2020 17:49:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Oct 2020 17:49:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 26 Oct 2020 17:49:23 GMT
USER odoo
# Mon, 26 Oct 2020 17:49:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Oct 2020 17:49:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086dfd04ee4f09e3759168af225fb6366b6e33e604235abf1da4e3aea207c9d8`  
		Last Modified: Mon, 26 Oct 2020 17:52:13 GMT  
		Size: 207.1 MB (207077082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab0ca83605acca7d829847eac227f94f377dab01aae73e84e2a3496b2ea03f9`  
		Last Modified: Mon, 26 Oct 2020 17:51:36 GMT  
		Size: 2.4 MB (2432974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4997f88b88be6c179a0d473e2f0e9d90ee165e3a84cc19f956c383f31eb8e7b9`  
		Last Modified: Mon, 26 Oct 2020 17:51:35 GMT  
		Size: 1.1 MB (1118722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9248837ddaf17f82e79802675267956f2677c4597424a70d20e4678f1230d9cf`  
		Last Modified: Mon, 26 Oct 2020 17:52:12 GMT  
		Size: 148.3 MB (148293462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b415321b39c882a09388b258fd89a03ad61a723564994944a688d47f6e3576`  
		Last Modified: Mon, 26 Oct 2020 17:51:34 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0d32f4ada70f0c1d7287ddc857dbc1a16acfde7b37ef3a9977513c5611fa00`  
		Last Modified: Mon, 26 Oct 2020 17:51:35 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8971ccfac10acd1895f9f536d3c2708f0e20688ba81caa091d3972f888cddbfc`  
		Last Modified: Mon, 26 Oct 2020 17:51:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b209ecf5ab89d4ceaac437ed0e9a13ff4e785b0606f49476faf2c8d37d4b9`  
		Last Modified: Mon, 26 Oct 2020 17:51:35 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:335d31e83074a79e1ad8be65587558d24a1ea90c0d2b3b7e65cc91b9f170a97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:d5996828dca5d3ec89c3b85cd2b8ac9882a0f034f43b44c5e42476f7804f81a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.1 MB (399132183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70de954aa8a5672fc15a662bc3d389a5a0378a20082e7235cf4cabd78c3d8799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Mon, 26 Oct 2020 17:45:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Mon, 26 Oct 2020 17:45:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Oct 2020 17:45:21 GMT
RUN npm install -g rtlcss
# Mon, 26 Oct 2020 17:45:21 GMT
ENV ODOO_VERSION=14.0
# Mon, 26 Oct 2020 17:45:21 GMT
ARG ODOO_RELEASE=20201026
# Mon, 26 Oct 2020 17:45:22 GMT
ARG ODOO_SHA=f03d267d3a055dbc798b799efbfcb1eb9a739b23
# Mon, 26 Oct 2020 17:46:22 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=f03d267d3a055dbc798b799efbfcb1eb9a739b23
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 26 Oct 2020 17:46:23 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 26 Oct 2020 17:46:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 26 Oct 2020 17:46:24 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=f03d267d3a055dbc798b799efbfcb1eb9a739b23
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 26 Oct 2020 17:46:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Oct 2020 17:46:25 GMT
EXPOSE 8069 8071 8072
# Mon, 26 Oct 2020 17:46:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Oct 2020 17:46:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 26 Oct 2020 17:46:26 GMT
USER odoo
# Mon, 26 Oct 2020 17:46:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Oct 2020 17:46:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c69f32ce0e0b8c40da731c837dc4af71c91d64af3a383306b1998b87065248f`  
		Last Modified: Mon, 26 Oct 2020 17:51:27 GMT  
		Size: 213.1 MB (213119031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79914c2df80be97bf35af10e222d03a9673bdb70868542859f4ca306713ea83f`  
		Last Modified: Mon, 26 Oct 2020 17:50:46 GMT  
		Size: 2.4 MB (2435820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64083ae2108cec48181a94003bae0b8399a4a7b6471f1e2d1be462f3b80856bf`  
		Last Modified: Mon, 26 Oct 2020 17:50:45 GMT  
		Size: 1.1 MB (1118509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2505f32265502f0cc51cd314eedff3c942eeae4b2a48ae2b3c6d3deb5804fd15`  
		Last Modified: Mon, 26 Oct 2020 17:51:25 GMT  
		Size: 155.4 MB (155364193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801aa271fa0dbca6968e84036087daf6593eb7da7789f7753320a4b88e22a1c9`  
		Last Modified: Mon, 26 Oct 2020 17:50:44 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e087a17956065e1edcd4a3944203ee7036938e64d8bdaa280a8c940c9432efba`  
		Last Modified: Mon, 26 Oct 2020 17:50:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af253c038bd894d5fcffb3b7ef15d383be92dbdb30aeed1ac64572e2492e1823`  
		Last Modified: Mon, 26 Oct 2020 17:50:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04601c66bc5b679efe6b3c6b2d240cea0c9a2e7fbc236ba28da1e781f689010`  
		Last Modified: Mon, 26 Oct 2020 17:50:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:335d31e83074a79e1ad8be65587558d24a1ea90c0d2b3b7e65cc91b9f170a97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:d5996828dca5d3ec89c3b85cd2b8ac9882a0f034f43b44c5e42476f7804f81a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.1 MB (399132183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70de954aa8a5672fc15a662bc3d389a5a0378a20082e7235cf4cabd78c3d8799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Mon, 26 Oct 2020 17:45:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Mon, 26 Oct 2020 17:45:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Oct 2020 17:45:21 GMT
RUN npm install -g rtlcss
# Mon, 26 Oct 2020 17:45:21 GMT
ENV ODOO_VERSION=14.0
# Mon, 26 Oct 2020 17:45:21 GMT
ARG ODOO_RELEASE=20201026
# Mon, 26 Oct 2020 17:45:22 GMT
ARG ODOO_SHA=f03d267d3a055dbc798b799efbfcb1eb9a739b23
# Mon, 26 Oct 2020 17:46:22 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=f03d267d3a055dbc798b799efbfcb1eb9a739b23
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 26 Oct 2020 17:46:23 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 26 Oct 2020 17:46:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 26 Oct 2020 17:46:24 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=f03d267d3a055dbc798b799efbfcb1eb9a739b23
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 26 Oct 2020 17:46:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Oct 2020 17:46:25 GMT
EXPOSE 8069 8071 8072
# Mon, 26 Oct 2020 17:46:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Oct 2020 17:46:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 26 Oct 2020 17:46:26 GMT
USER odoo
# Mon, 26 Oct 2020 17:46:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Oct 2020 17:46:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c69f32ce0e0b8c40da731c837dc4af71c91d64af3a383306b1998b87065248f`  
		Last Modified: Mon, 26 Oct 2020 17:51:27 GMT  
		Size: 213.1 MB (213119031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79914c2df80be97bf35af10e222d03a9673bdb70868542859f4ca306713ea83f`  
		Last Modified: Mon, 26 Oct 2020 17:50:46 GMT  
		Size: 2.4 MB (2435820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64083ae2108cec48181a94003bae0b8399a4a7b6471f1e2d1be462f3b80856bf`  
		Last Modified: Mon, 26 Oct 2020 17:50:45 GMT  
		Size: 1.1 MB (1118509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2505f32265502f0cc51cd314eedff3c942eeae4b2a48ae2b3c6d3deb5804fd15`  
		Last Modified: Mon, 26 Oct 2020 17:51:25 GMT  
		Size: 155.4 MB (155364193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801aa271fa0dbca6968e84036087daf6593eb7da7789f7753320a4b88e22a1c9`  
		Last Modified: Mon, 26 Oct 2020 17:50:44 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e087a17956065e1edcd4a3944203ee7036938e64d8bdaa280a8c940c9432efba`  
		Last Modified: Mon, 26 Oct 2020 17:50:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af253c038bd894d5fcffb3b7ef15d383be92dbdb30aeed1ac64572e2492e1823`  
		Last Modified: Mon, 26 Oct 2020 17:50:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04601c66bc5b679efe6b3c6b2d240cea0c9a2e7fbc236ba28da1e781f689010`  
		Last Modified: Mon, 26 Oct 2020 17:50:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:335d31e83074a79e1ad8be65587558d24a1ea90c0d2b3b7e65cc91b9f170a97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:d5996828dca5d3ec89c3b85cd2b8ac9882a0f034f43b44c5e42476f7804f81a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.1 MB (399132183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70de954aa8a5672fc15a662bc3d389a5a0378a20082e7235cf4cabd78c3d8799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Mon, 26 Oct 2020 17:45:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Mon, 26 Oct 2020 17:45:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Oct 2020 17:45:21 GMT
RUN npm install -g rtlcss
# Mon, 26 Oct 2020 17:45:21 GMT
ENV ODOO_VERSION=14.0
# Mon, 26 Oct 2020 17:45:21 GMT
ARG ODOO_RELEASE=20201026
# Mon, 26 Oct 2020 17:45:22 GMT
ARG ODOO_SHA=f03d267d3a055dbc798b799efbfcb1eb9a739b23
# Mon, 26 Oct 2020 17:46:22 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=f03d267d3a055dbc798b799efbfcb1eb9a739b23
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 26 Oct 2020 17:46:23 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 26 Oct 2020 17:46:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 26 Oct 2020 17:46:24 GMT
# ARGS: ODOO_RELEASE=20201026 ODOO_SHA=f03d267d3a055dbc798b799efbfcb1eb9a739b23
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 26 Oct 2020 17:46:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Oct 2020 17:46:25 GMT
EXPOSE 8069 8071 8072
# Mon, 26 Oct 2020 17:46:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Oct 2020 17:46:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 26 Oct 2020 17:46:26 GMT
USER odoo
# Mon, 26 Oct 2020 17:46:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Oct 2020 17:46:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c69f32ce0e0b8c40da731c837dc4af71c91d64af3a383306b1998b87065248f`  
		Last Modified: Mon, 26 Oct 2020 17:51:27 GMT  
		Size: 213.1 MB (213119031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79914c2df80be97bf35af10e222d03a9673bdb70868542859f4ca306713ea83f`  
		Last Modified: Mon, 26 Oct 2020 17:50:46 GMT  
		Size: 2.4 MB (2435820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64083ae2108cec48181a94003bae0b8399a4a7b6471f1e2d1be462f3b80856bf`  
		Last Modified: Mon, 26 Oct 2020 17:50:45 GMT  
		Size: 1.1 MB (1118509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2505f32265502f0cc51cd314eedff3c942eeae4b2a48ae2b3c6d3deb5804fd15`  
		Last Modified: Mon, 26 Oct 2020 17:51:25 GMT  
		Size: 155.4 MB (155364193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801aa271fa0dbca6968e84036087daf6593eb7da7789f7753320a4b88e22a1c9`  
		Last Modified: Mon, 26 Oct 2020 17:50:44 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e087a17956065e1edcd4a3944203ee7036938e64d8bdaa280a8c940c9432efba`  
		Last Modified: Mon, 26 Oct 2020 17:50:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af253c038bd894d5fcffb3b7ef15d383be92dbdb30aeed1ac64572e2492e1823`  
		Last Modified: Mon, 26 Oct 2020 17:50:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04601c66bc5b679efe6b3c6b2d240cea0c9a2e7fbc236ba28da1e781f689010`  
		Last Modified: Mon, 26 Oct 2020 17:50:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
