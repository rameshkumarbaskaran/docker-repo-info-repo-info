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
$ docker pull odoo@sha256:5003c1e54eb222c408c4ca02fc4786c3c83bd3e675a8876096653528403d2125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:0ded8ad61ea0dbe977f6de0504d16215cc94ad799b773ca1c5653155b5696ba4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.0 MB (541041774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b0ecc9cccbcec02c19a375a1ebef1e2feb05080573aea90a5b9412c4bf230`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:33:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:33:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:33:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:33:50 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Feb 2021 17:35:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:36:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:16 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:17 GMT
ENV ODOO_VERSION=12.0
# Wed, 17 Feb 2021 19:27:05 GMT
ARG ODOO_RELEASE=20210217
# Wed, 17 Feb 2021 19:27:05 GMT
ARG ODOO_SHA=1fe634da61ffb3d7292d502e004cdb1c576afee8
# Wed, 17 Feb 2021 19:28:07 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1fe634da61ffb3d7292d502e004cdb1c576afee8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Feb 2021 19:28:08 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 17 Feb 2021 19:28:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Feb 2021 19:28:09 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1fe634da61ffb3d7292d502e004cdb1c576afee8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Feb 2021 19:28:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Feb 2021 19:28:10 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Feb 2021 19:28:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Feb 2021 19:28:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Feb 2021 19:28:10 GMT
USER odoo
# Wed, 17 Feb 2021 19:28:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Feb 2021 19:28:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1cabf5609130f825def08a86940a9a06f7025505559b2c7e652b60a9e05005`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab23230155ecde52cbc43dbfe8141ef3dcbfaa6a5e242654c5ff6071e727f0a9`  
		Last Modified: Tue, 09 Feb 2021 17:41:19 GMT  
		Size: 219.6 MB (219611261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ff187134bcc9d0cf0a66450af847efce4bd9dc973a88ae485acff4a4b3df1`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 2.2 MB (2222432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5ca9709c7ca8d1819e6f5e6a2a15591eb75f5cf82ba48c2825cde329116c8`  
		Last Modified: Tue, 09 Feb 2021 17:41:01 GMT  
		Size: 22.1 MB (22055467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0957e45a5255215e18ce1106409694ef3654be705ff616d640c4e6ccb10961`  
		Last Modified: Wed, 17 Feb 2021 19:30:47 GMT  
		Size: 274.6 MB (274621385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4565cb99416c83095d2a4ad4560adcd1803cf2ddbe51fce7b22ae21fa6fc4c`  
		Last Modified: Wed, 17 Feb 2021 19:30:15 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f209884d7bf26e47a5f75f48a4071a83234b4eebf5401fa1d16bb569cc2bf45`  
		Last Modified: Wed, 17 Feb 2021 19:30:14 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd735b55c77aa587c4c6dee25ad3966e703fd5f7d2d91a7ca052d1f6a9ab250`  
		Last Modified: Wed, 17 Feb 2021 19:30:15 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a627bb8c7513e7d604d40c0c4f6c2b5aff4f168e34bc45b0385df2513d1d5776`  
		Last Modified: Wed, 17 Feb 2021 19:30:15 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:5003c1e54eb222c408c4ca02fc4786c3c83bd3e675a8876096653528403d2125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:0ded8ad61ea0dbe977f6de0504d16215cc94ad799b773ca1c5653155b5696ba4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.0 MB (541041774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b0ecc9cccbcec02c19a375a1ebef1e2feb05080573aea90a5b9412c4bf230`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:33:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:33:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:33:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:33:50 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Feb 2021 17:35:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:36:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:16 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:17 GMT
ENV ODOO_VERSION=12.0
# Wed, 17 Feb 2021 19:27:05 GMT
ARG ODOO_RELEASE=20210217
# Wed, 17 Feb 2021 19:27:05 GMT
ARG ODOO_SHA=1fe634da61ffb3d7292d502e004cdb1c576afee8
# Wed, 17 Feb 2021 19:28:07 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1fe634da61ffb3d7292d502e004cdb1c576afee8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Feb 2021 19:28:08 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 17 Feb 2021 19:28:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Feb 2021 19:28:09 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1fe634da61ffb3d7292d502e004cdb1c576afee8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Feb 2021 19:28:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Feb 2021 19:28:10 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Feb 2021 19:28:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Feb 2021 19:28:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Feb 2021 19:28:10 GMT
USER odoo
# Wed, 17 Feb 2021 19:28:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Feb 2021 19:28:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1cabf5609130f825def08a86940a9a06f7025505559b2c7e652b60a9e05005`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab23230155ecde52cbc43dbfe8141ef3dcbfaa6a5e242654c5ff6071e727f0a9`  
		Last Modified: Tue, 09 Feb 2021 17:41:19 GMT  
		Size: 219.6 MB (219611261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ff187134bcc9d0cf0a66450af847efce4bd9dc973a88ae485acff4a4b3df1`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 2.2 MB (2222432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5ca9709c7ca8d1819e6f5e6a2a15591eb75f5cf82ba48c2825cde329116c8`  
		Last Modified: Tue, 09 Feb 2021 17:41:01 GMT  
		Size: 22.1 MB (22055467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0957e45a5255215e18ce1106409694ef3654be705ff616d640c4e6ccb10961`  
		Last Modified: Wed, 17 Feb 2021 19:30:47 GMT  
		Size: 274.6 MB (274621385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4565cb99416c83095d2a4ad4560adcd1803cf2ddbe51fce7b22ae21fa6fc4c`  
		Last Modified: Wed, 17 Feb 2021 19:30:15 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f209884d7bf26e47a5f75f48a4071a83234b4eebf5401fa1d16bb569cc2bf45`  
		Last Modified: Wed, 17 Feb 2021 19:30:14 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd735b55c77aa587c4c6dee25ad3966e703fd5f7d2d91a7ca052d1f6a9ab250`  
		Last Modified: Wed, 17 Feb 2021 19:30:15 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a627bb8c7513e7d604d40c0c4f6c2b5aff4f168e34bc45b0385df2513d1d5776`  
		Last Modified: Wed, 17 Feb 2021 19:30:15 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:eccca3b4a6d0a204ba71a2e63687729cb1a2b58b35226026697b9978f6f9fff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:ed1abcdd7df0359c3530995861a8bec20007513e28cf511d930ab8acb66736cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530754964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79518242c2c93453b167b2ed734cae67137c74d1b181f405655861f6efc9d259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:32:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:32:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:32:12 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:32:12 GMT
ENV ODOO_VERSION=13.0
# Wed, 17 Feb 2021 19:25:34 GMT
ARG ODOO_RELEASE=20210217
# Wed, 17 Feb 2021 19:25:34 GMT
ARG ODOO_SHA=fe66a740ba64e29872b6adfcb424c0574aa43fb5
# Wed, 17 Feb 2021 19:26:49 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=fe66a740ba64e29872b6adfcb424c0574aa43fb5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Feb 2021 19:26:50 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 17 Feb 2021 19:26:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Feb 2021 19:26:51 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=fe66a740ba64e29872b6adfcb424c0574aa43fb5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Feb 2021 19:26:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Feb 2021 19:26:51 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Feb 2021 19:26:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Feb 2021 19:26:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Feb 2021 19:26:52 GMT
USER odoo
# Wed, 17 Feb 2021 19:26:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Feb 2021 19:26:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df63def913e7acc2a8ee5bbdb8dac5f2449993c30e7aff862b1f01f485f5f2`  
		Last Modified: Tue, 09 Feb 2021 17:40:15 GMT  
		Size: 207.1 MB (207097574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ab203da2fb5d30f709e95af58f20d98a184b7fbc9e8611a5d91717a5fbe1c9`  
		Last Modified: Tue, 09 Feb 2021 17:39:37 GMT  
		Size: 2.3 MB (2343915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16975ddc87358fae6e7b7b9c3809881bdaaf4a63f75c307a3d344c92852557f5`  
		Last Modified: Tue, 09 Feb 2021 17:39:36 GMT  
		Size: 909.0 KB (909031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293924a36fa7e23cf36903148bb53794507f0802c89af0d830e5b89d3f2c6c07`  
		Last Modified: Wed, 17 Feb 2021 19:30:09 GMT  
		Size: 293.3 MB (293306898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e997e94188c0f3562f058224e6365c6895ad8bcbbda29dffafff161c71bdff7c`  
		Last Modified: Wed, 17 Feb 2021 19:29:32 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55dc4989e69c9b5e2857e2e84b2027b5f741f1f375780c6a29e2c30fa969ef7b`  
		Last Modified: Wed, 17 Feb 2021 19:29:32 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c14ce980edb355dc227f0d7891dcb4cfd9f9e7316b98a2bdf06edd4c4ddadd`  
		Last Modified: Wed, 17 Feb 2021 19:29:32 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032ff3e1f1bea51687a7638d4824c613000bb6fb693d32c870e981fa7d06ba01`  
		Last Modified: Wed, 17 Feb 2021 19:29:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:eccca3b4a6d0a204ba71a2e63687729cb1a2b58b35226026697b9978f6f9fff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:ed1abcdd7df0359c3530995861a8bec20007513e28cf511d930ab8acb66736cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530754964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79518242c2c93453b167b2ed734cae67137c74d1b181f405655861f6efc9d259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:32:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:32:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:32:12 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:32:12 GMT
ENV ODOO_VERSION=13.0
# Wed, 17 Feb 2021 19:25:34 GMT
ARG ODOO_RELEASE=20210217
# Wed, 17 Feb 2021 19:25:34 GMT
ARG ODOO_SHA=fe66a740ba64e29872b6adfcb424c0574aa43fb5
# Wed, 17 Feb 2021 19:26:49 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=fe66a740ba64e29872b6adfcb424c0574aa43fb5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Feb 2021 19:26:50 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 17 Feb 2021 19:26:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Feb 2021 19:26:51 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=fe66a740ba64e29872b6adfcb424c0574aa43fb5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Feb 2021 19:26:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Feb 2021 19:26:51 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Feb 2021 19:26:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Feb 2021 19:26:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Feb 2021 19:26:52 GMT
USER odoo
# Wed, 17 Feb 2021 19:26:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Feb 2021 19:26:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df63def913e7acc2a8ee5bbdb8dac5f2449993c30e7aff862b1f01f485f5f2`  
		Last Modified: Tue, 09 Feb 2021 17:40:15 GMT  
		Size: 207.1 MB (207097574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ab203da2fb5d30f709e95af58f20d98a184b7fbc9e8611a5d91717a5fbe1c9`  
		Last Modified: Tue, 09 Feb 2021 17:39:37 GMT  
		Size: 2.3 MB (2343915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16975ddc87358fae6e7b7b9c3809881bdaaf4a63f75c307a3d344c92852557f5`  
		Last Modified: Tue, 09 Feb 2021 17:39:36 GMT  
		Size: 909.0 KB (909031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293924a36fa7e23cf36903148bb53794507f0802c89af0d830e5b89d3f2c6c07`  
		Last Modified: Wed, 17 Feb 2021 19:30:09 GMT  
		Size: 293.3 MB (293306898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e997e94188c0f3562f058224e6365c6895ad8bcbbda29dffafff161c71bdff7c`  
		Last Modified: Wed, 17 Feb 2021 19:29:32 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55dc4989e69c9b5e2857e2e84b2027b5f741f1f375780c6a29e2c30fa969ef7b`  
		Last Modified: Wed, 17 Feb 2021 19:29:32 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c14ce980edb355dc227f0d7891dcb4cfd9f9e7316b98a2bdf06edd4c4ddadd`  
		Last Modified: Wed, 17 Feb 2021 19:29:32 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032ff3e1f1bea51687a7638d4824c613000bb6fb693d32c870e981fa7d06ba01`  
		Last Modified: Wed, 17 Feb 2021 19:29:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:7618dbe02f3c2f92826012255e8ea1ac68dae9a230256235c8bd2df6d2d26a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:d4681fbaec86bd99f4e405ebb5a32f68e04c0e05cffcee9bf63ba691da03e2e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.2 MB (511227922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a20c9642f41cacee65a36460744db6a079b823dd835bfe4bf2e6a9fc407ef57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Wed, 17 Feb 2021 19:24:17 GMT
ARG ODOO_RELEASE=20210217
# Wed, 17 Feb 2021 19:24:17 GMT
ARG ODOO_SHA=1a117bc676fbd84af93be716fde456c1477bb82d
# Wed, 17 Feb 2021 19:25:25 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1a117bc676fbd84af93be716fde456c1477bb82d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Feb 2021 19:25:27 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 17 Feb 2021 19:25:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Feb 2021 19:25:28 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1a117bc676fbd84af93be716fde456c1477bb82d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Feb 2021 19:25:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Feb 2021 19:25:28 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Feb 2021 19:25:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Feb 2021 19:25:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Feb 2021 19:25:29 GMT
USER odoo
# Wed, 17 Feb 2021 19:25:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Feb 2021 19:25:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c038600dbc9ef26a30a672f04100cfd8525fea19007344072f5557721791d1`  
		Last Modified: Wed, 17 Feb 2021 19:29:25 GMT  
		Size: 267.7 MB (267722952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32954c0fc9ad2e9702e6513e066d9f7df63586bbb69d19908d8d34035cdfe22f`  
		Last Modified: Wed, 17 Feb 2021 19:28:32 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca709856a17e54c0370b287bdbc27a69e51dad1e5d8e64047aa7d6409d6a9fac`  
		Last Modified: Wed, 17 Feb 2021 19:28:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499e662c7902de724a3ce5b5f1121b77b68061b7c5ef45aae729abb3eed8050d`  
		Last Modified: Wed, 17 Feb 2021 19:28:32 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793a131e1dfa93a6ee184a7d3352ef2f33bf944ffa143b98880739e90ed4e0b9`  
		Last Modified: Wed, 17 Feb 2021 19:28:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:7618dbe02f3c2f92826012255e8ea1ac68dae9a230256235c8bd2df6d2d26a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:d4681fbaec86bd99f4e405ebb5a32f68e04c0e05cffcee9bf63ba691da03e2e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.2 MB (511227922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a20c9642f41cacee65a36460744db6a079b823dd835bfe4bf2e6a9fc407ef57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Wed, 17 Feb 2021 19:24:17 GMT
ARG ODOO_RELEASE=20210217
# Wed, 17 Feb 2021 19:24:17 GMT
ARG ODOO_SHA=1a117bc676fbd84af93be716fde456c1477bb82d
# Wed, 17 Feb 2021 19:25:25 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1a117bc676fbd84af93be716fde456c1477bb82d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Feb 2021 19:25:27 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 17 Feb 2021 19:25:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Feb 2021 19:25:28 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1a117bc676fbd84af93be716fde456c1477bb82d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Feb 2021 19:25:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Feb 2021 19:25:28 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Feb 2021 19:25:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Feb 2021 19:25:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Feb 2021 19:25:29 GMT
USER odoo
# Wed, 17 Feb 2021 19:25:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Feb 2021 19:25:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c038600dbc9ef26a30a672f04100cfd8525fea19007344072f5557721791d1`  
		Last Modified: Wed, 17 Feb 2021 19:29:25 GMT  
		Size: 267.7 MB (267722952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32954c0fc9ad2e9702e6513e066d9f7df63586bbb69d19908d8d34035cdfe22f`  
		Last Modified: Wed, 17 Feb 2021 19:28:32 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca709856a17e54c0370b287bdbc27a69e51dad1e5d8e64047aa7d6409d6a9fac`  
		Last Modified: Wed, 17 Feb 2021 19:28:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499e662c7902de724a3ce5b5f1121b77b68061b7c5ef45aae729abb3eed8050d`  
		Last Modified: Wed, 17 Feb 2021 19:28:32 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793a131e1dfa93a6ee184a7d3352ef2f33bf944ffa143b98880739e90ed4e0b9`  
		Last Modified: Wed, 17 Feb 2021 19:28:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:7618dbe02f3c2f92826012255e8ea1ac68dae9a230256235c8bd2df6d2d26a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:d4681fbaec86bd99f4e405ebb5a32f68e04c0e05cffcee9bf63ba691da03e2e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.2 MB (511227922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a20c9642f41cacee65a36460744db6a079b823dd835bfe4bf2e6a9fc407ef57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Wed, 17 Feb 2021 19:24:17 GMT
ARG ODOO_RELEASE=20210217
# Wed, 17 Feb 2021 19:24:17 GMT
ARG ODOO_SHA=1a117bc676fbd84af93be716fde456c1477bb82d
# Wed, 17 Feb 2021 19:25:25 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1a117bc676fbd84af93be716fde456c1477bb82d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Feb 2021 19:25:27 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 17 Feb 2021 19:25:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Feb 2021 19:25:28 GMT
# ARGS: ODOO_RELEASE=20210217 ODOO_SHA=1a117bc676fbd84af93be716fde456c1477bb82d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Feb 2021 19:25:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Feb 2021 19:25:28 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Feb 2021 19:25:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Feb 2021 19:25:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Feb 2021 19:25:29 GMT
USER odoo
# Wed, 17 Feb 2021 19:25:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Feb 2021 19:25:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c038600dbc9ef26a30a672f04100cfd8525fea19007344072f5557721791d1`  
		Last Modified: Wed, 17 Feb 2021 19:29:25 GMT  
		Size: 267.7 MB (267722952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32954c0fc9ad2e9702e6513e066d9f7df63586bbb69d19908d8d34035cdfe22f`  
		Last Modified: Wed, 17 Feb 2021 19:28:32 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca709856a17e54c0370b287bdbc27a69e51dad1e5d8e64047aa7d6409d6a9fac`  
		Last Modified: Wed, 17 Feb 2021 19:28:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499e662c7902de724a3ce5b5f1121b77b68061b7c5ef45aae729abb3eed8050d`  
		Last Modified: Wed, 17 Feb 2021 19:28:32 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793a131e1dfa93a6ee184a7d3352ef2f33bf944ffa143b98880739e90ed4e0b9`  
		Last Modified: Wed, 17 Feb 2021 19:28:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
