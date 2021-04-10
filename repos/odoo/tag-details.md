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
$ docker pull odoo@sha256:b8ae39d654265741995a9f1f345479d5dd8037066fb6149fdc539c68da4433ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:5b4cebba3c2c3f99fe5eff55f3eb64fbe12acd98bf938dc58df5538642951163
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542565595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c764643e83f0c525fd944e2ec676492fe77a7aacee0438f783214c0e2c069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:37:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:37:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:37:46 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:37:47 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 10 Apr 2021 12:39:11 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:39:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
ENV ODOO_VERSION=12.0
# Sat, 10 Apr 2021 12:39:39 GMT
ARG ODOO_RELEASE=20210407
# Sat, 10 Apr 2021 12:39:39 GMT
ARG ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
# Sat, 10 Apr 2021 12:40:47 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 10 Apr 2021 12:40:48 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 10 Apr 2021 12:40:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 10 Apr 2021 12:40:49 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 10 Apr 2021 12:40:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 10 Apr 2021 12:40:50 GMT
EXPOSE 8069 8071 8072
# Sat, 10 Apr 2021 12:40:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 10 Apr 2021 12:40:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 10 Apr 2021 12:40:50 GMT
USER odoo
# Sat, 10 Apr 2021 12:40:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 12:40:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf89834cbbd2b3cee3b8a944f6b45e4a1507584664ee0a1b02259590615d59`  
		Last Modified: Sat, 10 Apr 2021 12:42:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b11cee4db50450b66bc29b47f68b86380f02d6097f24e2b69a05dab9b82788`  
		Last Modified: Sat, 10 Apr 2021 12:43:18 GMT  
		Size: 219.6 MB (219645154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98555f4c9e696b99e0a4429cafe8848f74f7baa37c2265bd07bdc5d7ca50ece3`  
		Last Modified: Sat, 10 Apr 2021 12:42:52 GMT  
		Size: 2.2 MB (2224102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd66427a8f8ee5f5e15e695a9171413d51a17fd3fa05b78c6b7b8f7f2b8a259`  
		Last Modified: Sat, 10 Apr 2021 12:42:56 GMT  
		Size: 22.0 MB (22046831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642f1e46fabe0947cdec7b008bdb7c0fafaa277ddb851aa3a97b08140da0dd7`  
		Last Modified: Sat, 10 Apr 2021 12:43:23 GMT  
		Size: 276.1 MB (276118580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de58d655e8891e05744a045305b4001f4e0098305dfd8bf65033aa86cf85faa9`  
		Last Modified: Sat, 10 Apr 2021 12:42:49 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da397443b5ac95bf63bed3c0f516052fdc5901f40f4f13d7e8012fc5217ae1d9`  
		Last Modified: Sat, 10 Apr 2021 12:42:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dacc905c276ac00d9ee646dff2f94a87c374c8e34d6348bcb032725ef00d30`  
		Last Modified: Sat, 10 Apr 2021 12:42:49 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584c65c1e5c6efd6cd46fec17cdd1f2cbeaccf05b6361960de8496dda1991ec1`  
		Last Modified: Sat, 10 Apr 2021 12:42:49 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:b8ae39d654265741995a9f1f345479d5dd8037066fb6149fdc539c68da4433ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:5b4cebba3c2c3f99fe5eff55f3eb64fbe12acd98bf938dc58df5538642951163
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542565595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c764643e83f0c525fd944e2ec676492fe77a7aacee0438f783214c0e2c069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:37:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:37:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:37:46 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:37:47 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 10 Apr 2021 12:39:11 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:39:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
ENV ODOO_VERSION=12.0
# Sat, 10 Apr 2021 12:39:39 GMT
ARG ODOO_RELEASE=20210407
# Sat, 10 Apr 2021 12:39:39 GMT
ARG ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
# Sat, 10 Apr 2021 12:40:47 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 10 Apr 2021 12:40:48 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 10 Apr 2021 12:40:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 10 Apr 2021 12:40:49 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 10 Apr 2021 12:40:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 10 Apr 2021 12:40:50 GMT
EXPOSE 8069 8071 8072
# Sat, 10 Apr 2021 12:40:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 10 Apr 2021 12:40:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 10 Apr 2021 12:40:50 GMT
USER odoo
# Sat, 10 Apr 2021 12:40:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 12:40:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf89834cbbd2b3cee3b8a944f6b45e4a1507584664ee0a1b02259590615d59`  
		Last Modified: Sat, 10 Apr 2021 12:42:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b11cee4db50450b66bc29b47f68b86380f02d6097f24e2b69a05dab9b82788`  
		Last Modified: Sat, 10 Apr 2021 12:43:18 GMT  
		Size: 219.6 MB (219645154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98555f4c9e696b99e0a4429cafe8848f74f7baa37c2265bd07bdc5d7ca50ece3`  
		Last Modified: Sat, 10 Apr 2021 12:42:52 GMT  
		Size: 2.2 MB (2224102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd66427a8f8ee5f5e15e695a9171413d51a17fd3fa05b78c6b7b8f7f2b8a259`  
		Last Modified: Sat, 10 Apr 2021 12:42:56 GMT  
		Size: 22.0 MB (22046831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642f1e46fabe0947cdec7b008bdb7c0fafaa277ddb851aa3a97b08140da0dd7`  
		Last Modified: Sat, 10 Apr 2021 12:43:23 GMT  
		Size: 276.1 MB (276118580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de58d655e8891e05744a045305b4001f4e0098305dfd8bf65033aa86cf85faa9`  
		Last Modified: Sat, 10 Apr 2021 12:42:49 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da397443b5ac95bf63bed3c0f516052fdc5901f40f4f13d7e8012fc5217ae1d9`  
		Last Modified: Sat, 10 Apr 2021 12:42:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dacc905c276ac00d9ee646dff2f94a87c374c8e34d6348bcb032725ef00d30`  
		Last Modified: Sat, 10 Apr 2021 12:42:49 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584c65c1e5c6efd6cd46fec17cdd1f2cbeaccf05b6361960de8496dda1991ec1`  
		Last Modified: Sat, 10 Apr 2021 12:42:49 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:5b899f11393d1583c1ba04d6fa9ed5caf4b9cd04f627f547b1430404529609a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:578a20a0b50c5f146fc395d53ab9d205ade1f2dadfe675648e09700798ad6734
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532294209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c9ce400b0e5c6d8fa99f305c25b6b6b10faddc5b47d099e3165314e98dbfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:35:54 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:36:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:36:13 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:36:14 GMT
ENV ODOO_VERSION=13.0
# Sat, 10 Apr 2021 12:36:14 GMT
ARG ODOO_RELEASE=20210407
# Sat, 10 Apr 2021 12:36:14 GMT
ARG ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
# Sat, 10 Apr 2021 12:37:28 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 10 Apr 2021 12:37:32 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 10 Apr 2021 12:37:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 10 Apr 2021 12:37:33 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 10 Apr 2021 12:37:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 10 Apr 2021 12:37:34 GMT
EXPOSE 8069 8071 8072
# Sat, 10 Apr 2021 12:37:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 10 Apr 2021 12:37:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 10 Apr 2021 12:37:34 GMT
USER odoo
# Sat, 10 Apr 2021 12:37:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 12:37:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f81febf0e37dd17e29257f92caf652e1fead27661526fffe25491be70915d3`  
		Last Modified: Sat, 10 Apr 2021 12:42:31 GMT  
		Size: 207.1 MB (207124621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79303e39ab88305c57546603826b66e6eb084ae3937717320b18885c8f73fb60`  
		Last Modified: Sat, 10 Apr 2021 12:42:03 GMT  
		Size: 2.3 MB (2345472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185986373d8432024fd24e5a223928c83785fd54e9527e2380262b64e621206b`  
		Last Modified: Sat, 10 Apr 2021 12:42:06 GMT  
		Size: 896.8 KB (896834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a56902d213b680669581bb65815157bcb39f6f1d374e5b0ebcab3aa9e5ad7c`  
		Last Modified: Sat, 10 Apr 2021 12:42:38 GMT  
		Size: 294.8 MB (294785474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ee96a440d204f6a7c2727118db5a00785f6805f09164c3beb9d0a71162dc72`  
		Last Modified: Sat, 10 Apr 2021 12:42:00 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4adba6b397e814e7887fe082478b5318f6b2bcb9f60cca706ec8dc142b4234`  
		Last Modified: Sat, 10 Apr 2021 12:42:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a242c1386fa56f9858437f43f8275909228545092096e92c723fc93f4bf60c21`  
		Last Modified: Sat, 10 Apr 2021 12:42:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defccd9743004f429ba5a7263f2da740f4fd913e81bd328523d3801c59d8211e`  
		Last Modified: Sat, 10 Apr 2021 12:42:00 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:5b899f11393d1583c1ba04d6fa9ed5caf4b9cd04f627f547b1430404529609a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:578a20a0b50c5f146fc395d53ab9d205ade1f2dadfe675648e09700798ad6734
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532294209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c9ce400b0e5c6d8fa99f305c25b6b6b10faddc5b47d099e3165314e98dbfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:35:54 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:36:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:36:13 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:36:14 GMT
ENV ODOO_VERSION=13.0
# Sat, 10 Apr 2021 12:36:14 GMT
ARG ODOO_RELEASE=20210407
# Sat, 10 Apr 2021 12:36:14 GMT
ARG ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
# Sat, 10 Apr 2021 12:37:28 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 10 Apr 2021 12:37:32 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 10 Apr 2021 12:37:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 10 Apr 2021 12:37:33 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 10 Apr 2021 12:37:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 10 Apr 2021 12:37:34 GMT
EXPOSE 8069 8071 8072
# Sat, 10 Apr 2021 12:37:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 10 Apr 2021 12:37:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 10 Apr 2021 12:37:34 GMT
USER odoo
# Sat, 10 Apr 2021 12:37:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 12:37:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f81febf0e37dd17e29257f92caf652e1fead27661526fffe25491be70915d3`  
		Last Modified: Sat, 10 Apr 2021 12:42:31 GMT  
		Size: 207.1 MB (207124621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79303e39ab88305c57546603826b66e6eb084ae3937717320b18885c8f73fb60`  
		Last Modified: Sat, 10 Apr 2021 12:42:03 GMT  
		Size: 2.3 MB (2345472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185986373d8432024fd24e5a223928c83785fd54e9527e2380262b64e621206b`  
		Last Modified: Sat, 10 Apr 2021 12:42:06 GMT  
		Size: 896.8 KB (896834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a56902d213b680669581bb65815157bcb39f6f1d374e5b0ebcab3aa9e5ad7c`  
		Last Modified: Sat, 10 Apr 2021 12:42:38 GMT  
		Size: 294.8 MB (294785474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ee96a440d204f6a7c2727118db5a00785f6805f09164c3beb9d0a71162dc72`  
		Last Modified: Sat, 10 Apr 2021 12:42:00 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4adba6b397e814e7887fe082478b5318f6b2bcb9f60cca706ec8dc142b4234`  
		Last Modified: Sat, 10 Apr 2021 12:42:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a242c1386fa56f9858437f43f8275909228545092096e92c723fc93f4bf60c21`  
		Last Modified: Sat, 10 Apr 2021 12:42:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defccd9743004f429ba5a7263f2da740f4fd913e81bd328523d3801c59d8211e`  
		Last Modified: Sat, 10 Apr 2021 12:42:00 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:dabf4f7840b283cbfe736fb469db8572706efe65f66025a9445bf6a9fdba46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:04384b61e1ef32f4814c443599bb8252c368270ce9c3f86e368c6510396c291e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.9 MB (515863607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6085d42f19a023b54f5174a53417a7893112d971bbe2f9a70154ac645546d2ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Sat, 10 Apr 2021 12:32:51 GMT
ARG ODOO_RELEASE=20210407
# Sat, 10 Apr 2021 12:32:51 GMT
ARG ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
# Sat, 10 Apr 2021 12:34:23 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 10 Apr 2021 12:34:25 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 10 Apr 2021 12:34:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 10 Apr 2021 12:34:27 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 10 Apr 2021 12:34:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 10 Apr 2021 12:34:28 GMT
EXPOSE 8069 8071 8072
# Sat, 10 Apr 2021 12:34:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 10 Apr 2021 12:34:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 10 Apr 2021 12:34:29 GMT
USER odoo
# Sat, 10 Apr 2021 12:34:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 12:34:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df087de27948df1896e2eeba6f91888dd021d36942b9009ba960e5ee08f169`  
		Last Modified: Sat, 10 Apr 2021 12:41:46 GMT  
		Size: 272.3 MB (272306134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9556b66e592d1c78a7fad473288359ac14de2e8d24cbfe755a1d0a43134c795`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f095c92e9e8999227768539bd2e3147adbd65825f1428c7035a6fd36e490ac`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af963c2abcff6c449dfbdcad75867a9dc55533843c21a3376808abbf1462424`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504c99a0ff59f39e596d40a3505188b7c5ca23155e1d6a7e4e2db399dfd847d7`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:dabf4f7840b283cbfe736fb469db8572706efe65f66025a9445bf6a9fdba46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:04384b61e1ef32f4814c443599bb8252c368270ce9c3f86e368c6510396c291e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.9 MB (515863607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6085d42f19a023b54f5174a53417a7893112d971bbe2f9a70154ac645546d2ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Sat, 10 Apr 2021 12:32:51 GMT
ARG ODOO_RELEASE=20210407
# Sat, 10 Apr 2021 12:32:51 GMT
ARG ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
# Sat, 10 Apr 2021 12:34:23 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 10 Apr 2021 12:34:25 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 10 Apr 2021 12:34:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 10 Apr 2021 12:34:27 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 10 Apr 2021 12:34:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 10 Apr 2021 12:34:28 GMT
EXPOSE 8069 8071 8072
# Sat, 10 Apr 2021 12:34:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 10 Apr 2021 12:34:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 10 Apr 2021 12:34:29 GMT
USER odoo
# Sat, 10 Apr 2021 12:34:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 12:34:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df087de27948df1896e2eeba6f91888dd021d36942b9009ba960e5ee08f169`  
		Last Modified: Sat, 10 Apr 2021 12:41:46 GMT  
		Size: 272.3 MB (272306134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9556b66e592d1c78a7fad473288359ac14de2e8d24cbfe755a1d0a43134c795`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f095c92e9e8999227768539bd2e3147adbd65825f1428c7035a6fd36e490ac`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af963c2abcff6c449dfbdcad75867a9dc55533843c21a3376808abbf1462424`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504c99a0ff59f39e596d40a3505188b7c5ca23155e1d6a7e4e2db399dfd847d7`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:dabf4f7840b283cbfe736fb469db8572706efe65f66025a9445bf6a9fdba46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:04384b61e1ef32f4814c443599bb8252c368270ce9c3f86e368c6510396c291e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.9 MB (515863607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6085d42f19a023b54f5174a53417a7893112d971bbe2f9a70154ac645546d2ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Sat, 10 Apr 2021 12:32:51 GMT
ARG ODOO_RELEASE=20210407
# Sat, 10 Apr 2021 12:32:51 GMT
ARG ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
# Sat, 10 Apr 2021 12:34:23 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 10 Apr 2021 12:34:25 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 10 Apr 2021 12:34:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 10 Apr 2021 12:34:27 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 10 Apr 2021 12:34:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 10 Apr 2021 12:34:28 GMT
EXPOSE 8069 8071 8072
# Sat, 10 Apr 2021 12:34:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 10 Apr 2021 12:34:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 10 Apr 2021 12:34:29 GMT
USER odoo
# Sat, 10 Apr 2021 12:34:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 12:34:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df087de27948df1896e2eeba6f91888dd021d36942b9009ba960e5ee08f169`  
		Last Modified: Sat, 10 Apr 2021 12:41:46 GMT  
		Size: 272.3 MB (272306134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9556b66e592d1c78a7fad473288359ac14de2e8d24cbfe755a1d0a43134c795`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f095c92e9e8999227768539bd2e3147adbd65825f1428c7035a6fd36e490ac`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af963c2abcff6c449dfbdcad75867a9dc55533843c21a3376808abbf1462424`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504c99a0ff59f39e596d40a3505188b7c5ca23155e1d6a7e4e2db399dfd847d7`  
		Last Modified: Sat, 10 Apr 2021 12:41:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
