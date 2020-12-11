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
$ docker pull odoo@sha256:ae98f96e5ba9e46c1aad48eb4d9e86293481e49565bf1906235011383b516af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:ec6997ea071e45a588d62b409014fddd4b5d309358a19c421f26eb1e0ee97ebb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396691270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038eace26139681cf99737b52f89afe447d7783714a7439fdbb8722c59750813`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:22:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:22:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:22:07 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:22:10 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 11 Dec 2020 17:23:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:23:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:24:10 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:24:10 GMT
ENV ODOO_VERSION=12.0
# Fri, 11 Dec 2020 17:24:10 GMT
ARG ODOO_RELEASE=20201208
# Fri, 11 Dec 2020 17:24:10 GMT
ARG ODOO_SHA=9b055f129756442f58fce0b3d819be4a0e61709e
# Fri, 11 Dec 2020 17:24:57 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=9b055f129756442f58fce0b3d819be4a0e61709e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 11 Dec 2020 17:24:58 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 11 Dec 2020 17:24:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 11 Dec 2020 17:25:00 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=9b055f129756442f58fce0b3d819be4a0e61709e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 11 Dec 2020 17:25:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 11 Dec 2020 17:25:00 GMT
EXPOSE 8069 8071 8072
# Fri, 11 Dec 2020 17:25:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 11 Dec 2020 17:25:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 11 Dec 2020 17:25:01 GMT
USER odoo
# Fri, 11 Dec 2020 17:25:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 17:25:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a5fca80cf5e4be20355b1886a25d710803679f0a7c71ded0c3de6cae19c19d`  
		Last Modified: Fri, 11 Dec 2020 17:27:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99fdce30aebd92be43edc52d36e352ca174d0cf9a2ede367bc7ace614b2746c`  
		Last Modified: Fri, 11 Dec 2020 17:28:27 GMT  
		Size: 219.6 MB (219607697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1f090eb0f54f5b004406240879df2b21117f6e204f42865488fda72dc7d163`  
		Last Modified: Fri, 11 Dec 2020 17:27:24 GMT  
		Size: 2.2 MB (2222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce3bbc0a15d1cc1dad99fd8f34e340d95df6039650826577c8a8ceb35221431`  
		Last Modified: Fri, 11 Dec 2020 17:27:38 GMT  
		Size: 22.1 MB (22069709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea661c3d4a71059d87a3123d2601b1d4bcdecb29397ded4a933954a2dcb8acae`  
		Last Modified: Fri, 11 Dec 2020 17:28:36 GMT  
		Size: 130.3 MB (130261003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb433ff907be5118444a8a0fad44cbbf57d98649958b714d69c2d551d00347b`  
		Last Modified: Fri, 11 Dec 2020 17:27:22 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99d4a73f46b2cb71ec92948003985fcb8bd7f1a90c436a26baf5e45a65b1c9b`  
		Last Modified: Fri, 11 Dec 2020 17:27:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce7b9e19236503cdc25057e45ee97968520e550d4fcbf096f8acd68b773049`  
		Last Modified: Fri, 11 Dec 2020 17:27:22 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bccdc2d363956d2314d00dfb7d23745666edcac4b9d8407ca98eabbd4dde6d`  
		Last Modified: Fri, 11 Dec 2020 17:27:22 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:ae98f96e5ba9e46c1aad48eb4d9e86293481e49565bf1906235011383b516af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:ec6997ea071e45a588d62b409014fddd4b5d309358a19c421f26eb1e0ee97ebb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396691270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038eace26139681cf99737b52f89afe447d7783714a7439fdbb8722c59750813`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:22:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:22:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:22:07 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:22:10 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 11 Dec 2020 17:23:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:23:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:24:10 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:24:10 GMT
ENV ODOO_VERSION=12.0
# Fri, 11 Dec 2020 17:24:10 GMT
ARG ODOO_RELEASE=20201208
# Fri, 11 Dec 2020 17:24:10 GMT
ARG ODOO_SHA=9b055f129756442f58fce0b3d819be4a0e61709e
# Fri, 11 Dec 2020 17:24:57 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=9b055f129756442f58fce0b3d819be4a0e61709e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 11 Dec 2020 17:24:58 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 11 Dec 2020 17:24:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 11 Dec 2020 17:25:00 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=9b055f129756442f58fce0b3d819be4a0e61709e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 11 Dec 2020 17:25:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 11 Dec 2020 17:25:00 GMT
EXPOSE 8069 8071 8072
# Fri, 11 Dec 2020 17:25:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 11 Dec 2020 17:25:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 11 Dec 2020 17:25:01 GMT
USER odoo
# Fri, 11 Dec 2020 17:25:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 17:25:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a5fca80cf5e4be20355b1886a25d710803679f0a7c71ded0c3de6cae19c19d`  
		Last Modified: Fri, 11 Dec 2020 17:27:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99fdce30aebd92be43edc52d36e352ca174d0cf9a2ede367bc7ace614b2746c`  
		Last Modified: Fri, 11 Dec 2020 17:28:27 GMT  
		Size: 219.6 MB (219607697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1f090eb0f54f5b004406240879df2b21117f6e204f42865488fda72dc7d163`  
		Last Modified: Fri, 11 Dec 2020 17:27:24 GMT  
		Size: 2.2 MB (2222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce3bbc0a15d1cc1dad99fd8f34e340d95df6039650826577c8a8ceb35221431`  
		Last Modified: Fri, 11 Dec 2020 17:27:38 GMT  
		Size: 22.1 MB (22069709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea661c3d4a71059d87a3123d2601b1d4bcdecb29397ded4a933954a2dcb8acae`  
		Last Modified: Fri, 11 Dec 2020 17:28:36 GMT  
		Size: 130.3 MB (130261003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb433ff907be5118444a8a0fad44cbbf57d98649958b714d69c2d551d00347b`  
		Last Modified: Fri, 11 Dec 2020 17:27:22 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99d4a73f46b2cb71ec92948003985fcb8bd7f1a90c436a26baf5e45a65b1c9b`  
		Last Modified: Fri, 11 Dec 2020 17:27:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce7b9e19236503cdc25057e45ee97968520e550d4fcbf096f8acd68b773049`  
		Last Modified: Fri, 11 Dec 2020 17:27:22 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bccdc2d363956d2314d00dfb7d23745666edcac4b9d8407ca98eabbd4dde6d`  
		Last Modified: Fri, 11 Dec 2020 17:27:22 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:8f9a2561fd85d28668ce8273d2b2d85b900265255acbc4956cb96891108afeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:cbaa58abeddde4b9774899abfdfd734f0b8371f5530192f2c0a70b99262b37b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.2 MB (386240200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2537e096d149e03565864f4a07f4378a344e2447ef1af64b643ccbdd120439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:20:10 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:20:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:20:26 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:20:27 GMT
ENV ODOO_VERSION=13.0
# Fri, 11 Dec 2020 17:20:27 GMT
ARG ODOO_RELEASE=20201208
# Fri, 11 Dec 2020 17:20:27 GMT
ARG ODOO_SHA=acb26cf02f554009ba99510acc5631d29616dd10
# Fri, 11 Dec 2020 17:21:42 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=acb26cf02f554009ba99510acc5631d29616dd10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 11 Dec 2020 17:21:43 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 11 Dec 2020 17:21:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 11 Dec 2020 17:21:44 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=acb26cf02f554009ba99510acc5631d29616dd10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 11 Dec 2020 17:21:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 11 Dec 2020 17:21:44 GMT
EXPOSE 8069 8071 8072
# Fri, 11 Dec 2020 17:21:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 11 Dec 2020 17:21:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 11 Dec 2020 17:21:45 GMT
USER odoo
# Fri, 11 Dec 2020 17:21:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 17:21:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d85901c4050548f6d6f629e8fb1ae22d74aba09c4f622fa69c57c40128bed5`  
		Last Modified: Fri, 11 Dec 2020 17:27:04 GMT  
		Size: 207.1 MB (207077357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e6fcfad7aecb0170d1af106384e043637b3d5f6b51e1fe4f69519e772fe2f`  
		Last Modified: Fri, 11 Dec 2020 17:26:22 GMT  
		Size: 2.3 MB (2343918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681e2f39973b063caa7a47829a5d8bb6cc6a404aeb719d5ffd7974ab79630330`  
		Last Modified: Fri, 11 Dec 2020 17:26:22 GMT  
		Size: 927.4 KB (927358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd2c6e256a2ed51149b10f99f61298efc64e98e95d23a70e9215dd3cb6c600e`  
		Last Modified: Fri, 11 Dec 2020 17:27:14 GMT  
		Size: 148.8 MB (148789866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453de851530c6c482e2ad17e6a3db08f99aa6a3bf6435cf3ed2628d53fae35d`  
		Last Modified: Fri, 11 Dec 2020 17:26:21 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3581a3b45b26943652541275fc750909b6bdcd1f618a8f7afcd167d1b6100b5e`  
		Last Modified: Fri, 11 Dec 2020 17:26:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead780d90b5cfa8a30ced0e218f9e8257f0e2f538714b07485719dee031b94a`  
		Last Modified: Fri, 11 Dec 2020 17:26:21 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4f1b6d9f073a7fbad430f3c9f1dcfe55628422e9a211284bee0b1ddcd0f801`  
		Last Modified: Fri, 11 Dec 2020 17:26:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:8f9a2561fd85d28668ce8273d2b2d85b900265255acbc4956cb96891108afeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:cbaa58abeddde4b9774899abfdfd734f0b8371f5530192f2c0a70b99262b37b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.2 MB (386240200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2537e096d149e03565864f4a07f4378a344e2447ef1af64b643ccbdd120439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:20:10 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:20:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:20:26 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:20:27 GMT
ENV ODOO_VERSION=13.0
# Fri, 11 Dec 2020 17:20:27 GMT
ARG ODOO_RELEASE=20201208
# Fri, 11 Dec 2020 17:20:27 GMT
ARG ODOO_SHA=acb26cf02f554009ba99510acc5631d29616dd10
# Fri, 11 Dec 2020 17:21:42 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=acb26cf02f554009ba99510acc5631d29616dd10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 11 Dec 2020 17:21:43 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 11 Dec 2020 17:21:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 11 Dec 2020 17:21:44 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=acb26cf02f554009ba99510acc5631d29616dd10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 11 Dec 2020 17:21:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 11 Dec 2020 17:21:44 GMT
EXPOSE 8069 8071 8072
# Fri, 11 Dec 2020 17:21:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 11 Dec 2020 17:21:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 11 Dec 2020 17:21:45 GMT
USER odoo
# Fri, 11 Dec 2020 17:21:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 17:21:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d85901c4050548f6d6f629e8fb1ae22d74aba09c4f622fa69c57c40128bed5`  
		Last Modified: Fri, 11 Dec 2020 17:27:04 GMT  
		Size: 207.1 MB (207077357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e6fcfad7aecb0170d1af106384e043637b3d5f6b51e1fe4f69519e772fe2f`  
		Last Modified: Fri, 11 Dec 2020 17:26:22 GMT  
		Size: 2.3 MB (2343918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681e2f39973b063caa7a47829a5d8bb6cc6a404aeb719d5ffd7974ab79630330`  
		Last Modified: Fri, 11 Dec 2020 17:26:22 GMT  
		Size: 927.4 KB (927358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd2c6e256a2ed51149b10f99f61298efc64e98e95d23a70e9215dd3cb6c600e`  
		Last Modified: Fri, 11 Dec 2020 17:27:14 GMT  
		Size: 148.8 MB (148789866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453de851530c6c482e2ad17e6a3db08f99aa6a3bf6435cf3ed2628d53fae35d`  
		Last Modified: Fri, 11 Dec 2020 17:26:21 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3581a3b45b26943652541275fc750909b6bdcd1f618a8f7afcd167d1b6100b5e`  
		Last Modified: Fri, 11 Dec 2020 17:26:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead780d90b5cfa8a30ced0e218f9e8257f0e2f538714b07485719dee031b94a`  
		Last Modified: Fri, 11 Dec 2020 17:26:21 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4f1b6d9f073a7fbad430f3c9f1dcfe55628422e9a211284bee0b1ddcd0f801`  
		Last Modified: Fri, 11 Dec 2020 17:26:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:9c8398763f0a202195379733226d8e6091cb02e0e7f0fa479ae820c05f68deb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:3569f9fc3f37a71ac4445bb2de30c7c760ff9af27a47579a8af8160b65730c7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.2 MB (404214462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6cd4ad707b86f3ce69aa4b495affde6258edb55a540e737f5e2de45b6969c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:17:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:17:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:17:16 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:17:16 GMT
ENV ODOO_VERSION=14.0
# Fri, 11 Dec 2020 17:17:16 GMT
ARG ODOO_RELEASE=20201208
# Fri, 11 Dec 2020 17:17:16 GMT
ARG ODOO_SHA=37dd5d71d5b8439fddf88d7e161cc3502721c4b5
# Fri, 11 Dec 2020 17:18:15 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=37dd5d71d5b8439fddf88d7e161cc3502721c4b5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 11 Dec 2020 17:18:17 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 11 Dec 2020 17:18:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 11 Dec 2020 17:18:19 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=37dd5d71d5b8439fddf88d7e161cc3502721c4b5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 11 Dec 2020 17:18:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 11 Dec 2020 17:18:19 GMT
EXPOSE 8069 8071 8072
# Fri, 11 Dec 2020 17:18:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 11 Dec 2020 17:18:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 11 Dec 2020 17:18:20 GMT
USER odoo
# Fri, 11 Dec 2020 17:18:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 17:18:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bc76188888637b8d6d4343790322715f6ff67e2f556d95ba4007bba46aa4b4`  
		Last Modified: Fri, 11 Dec 2020 17:26:02 GMT  
		Size: 213.1 MB (213118166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1489eaa0a91c1579cd0b86042b35ce651421b6d4be8baac3ff6f5e28fc88b423`  
		Last Modified: Fri, 11 Dec 2020 17:25:21 GMT  
		Size: 2.3 MB (2346249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8179dcb4a5c98894d38fdcf9748cbea2ad22a70c2b85c8118ca1f2f23e42afe1`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 927.4 KB (927408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390f29d1a221d4588ac1a2b553a70ff517a91836d630aa350150b9bc619bdf4`  
		Last Modified: Fri, 11 Dec 2020 17:26:12 GMT  
		Size: 160.7 MB (160720940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b323ab5c3f88bf247561a0fd558d05a7a76d7b5a31b7b739887ed7225ec44b`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe64693cfd693e783fff8b089c6d70574a60134d3e8282b3a0541eab98c58e4`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e47370cf02b2e124a425a0247fb5096623be6c3839e68887a55c60d25e2cd6`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1a10b2ec20203fac8cf65cfb5d1f2da38c32632ad61e9129bf27c439b6c429`  
		Last Modified: Fri, 11 Dec 2020 17:25:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:9c8398763f0a202195379733226d8e6091cb02e0e7f0fa479ae820c05f68deb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:3569f9fc3f37a71ac4445bb2de30c7c760ff9af27a47579a8af8160b65730c7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.2 MB (404214462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6cd4ad707b86f3ce69aa4b495affde6258edb55a540e737f5e2de45b6969c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:17:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:17:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:17:16 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:17:16 GMT
ENV ODOO_VERSION=14.0
# Fri, 11 Dec 2020 17:17:16 GMT
ARG ODOO_RELEASE=20201208
# Fri, 11 Dec 2020 17:17:16 GMT
ARG ODOO_SHA=37dd5d71d5b8439fddf88d7e161cc3502721c4b5
# Fri, 11 Dec 2020 17:18:15 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=37dd5d71d5b8439fddf88d7e161cc3502721c4b5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 11 Dec 2020 17:18:17 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 11 Dec 2020 17:18:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 11 Dec 2020 17:18:19 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=37dd5d71d5b8439fddf88d7e161cc3502721c4b5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 11 Dec 2020 17:18:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 11 Dec 2020 17:18:19 GMT
EXPOSE 8069 8071 8072
# Fri, 11 Dec 2020 17:18:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 11 Dec 2020 17:18:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 11 Dec 2020 17:18:20 GMT
USER odoo
# Fri, 11 Dec 2020 17:18:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 17:18:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bc76188888637b8d6d4343790322715f6ff67e2f556d95ba4007bba46aa4b4`  
		Last Modified: Fri, 11 Dec 2020 17:26:02 GMT  
		Size: 213.1 MB (213118166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1489eaa0a91c1579cd0b86042b35ce651421b6d4be8baac3ff6f5e28fc88b423`  
		Last Modified: Fri, 11 Dec 2020 17:25:21 GMT  
		Size: 2.3 MB (2346249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8179dcb4a5c98894d38fdcf9748cbea2ad22a70c2b85c8118ca1f2f23e42afe1`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 927.4 KB (927408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390f29d1a221d4588ac1a2b553a70ff517a91836d630aa350150b9bc619bdf4`  
		Last Modified: Fri, 11 Dec 2020 17:26:12 GMT  
		Size: 160.7 MB (160720940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b323ab5c3f88bf247561a0fd558d05a7a76d7b5a31b7b739887ed7225ec44b`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe64693cfd693e783fff8b089c6d70574a60134d3e8282b3a0541eab98c58e4`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e47370cf02b2e124a425a0247fb5096623be6c3839e68887a55c60d25e2cd6`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1a10b2ec20203fac8cf65cfb5d1f2da38c32632ad61e9129bf27c439b6c429`  
		Last Modified: Fri, 11 Dec 2020 17:25:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:9c8398763f0a202195379733226d8e6091cb02e0e7f0fa479ae820c05f68deb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:3569f9fc3f37a71ac4445bb2de30c7c760ff9af27a47579a8af8160b65730c7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.2 MB (404214462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6cd4ad707b86f3ce69aa4b495affde6258edb55a540e737f5e2de45b6969c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:17:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:17:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:17:16 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:17:16 GMT
ENV ODOO_VERSION=14.0
# Fri, 11 Dec 2020 17:17:16 GMT
ARG ODOO_RELEASE=20201208
# Fri, 11 Dec 2020 17:17:16 GMT
ARG ODOO_SHA=37dd5d71d5b8439fddf88d7e161cc3502721c4b5
# Fri, 11 Dec 2020 17:18:15 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=37dd5d71d5b8439fddf88d7e161cc3502721c4b5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 11 Dec 2020 17:18:17 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 11 Dec 2020 17:18:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 11 Dec 2020 17:18:19 GMT
# ARGS: ODOO_RELEASE=20201208 ODOO_SHA=37dd5d71d5b8439fddf88d7e161cc3502721c4b5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 11 Dec 2020 17:18:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 11 Dec 2020 17:18:19 GMT
EXPOSE 8069 8071 8072
# Fri, 11 Dec 2020 17:18:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 11 Dec 2020 17:18:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 11 Dec 2020 17:18:20 GMT
USER odoo
# Fri, 11 Dec 2020 17:18:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 17:18:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bc76188888637b8d6d4343790322715f6ff67e2f556d95ba4007bba46aa4b4`  
		Last Modified: Fri, 11 Dec 2020 17:26:02 GMT  
		Size: 213.1 MB (213118166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1489eaa0a91c1579cd0b86042b35ce651421b6d4be8baac3ff6f5e28fc88b423`  
		Last Modified: Fri, 11 Dec 2020 17:25:21 GMT  
		Size: 2.3 MB (2346249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8179dcb4a5c98894d38fdcf9748cbea2ad22a70c2b85c8118ca1f2f23e42afe1`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 927.4 KB (927408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390f29d1a221d4588ac1a2b553a70ff517a91836d630aa350150b9bc619bdf4`  
		Last Modified: Fri, 11 Dec 2020 17:26:12 GMT  
		Size: 160.7 MB (160720940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b323ab5c3f88bf247561a0fd558d05a7a76d7b5a31b7b739887ed7225ec44b`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe64693cfd693e783fff8b089c6d70574a60134d3e8282b3a0541eab98c58e4`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e47370cf02b2e124a425a0247fb5096623be6c3839e68887a55c60d25e2cd6`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1a10b2ec20203fac8cf65cfb5d1f2da38c32632ad61e9129bf27c439b6c429`  
		Last Modified: Fri, 11 Dec 2020 17:25:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
