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
$ docker pull odoo@sha256:592798f9cb772a97b7225210b0dad6867c266ec4540352249b27f472a341620c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:a25097a9e16b2b1a393a091c40c31091b5059ab8c5cd7cc61f42ad9e2db59d82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396739519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450b05890368ef750f12616c4e94cc6b17decb8e60f0a2fea3021ba75e3c6cf6`
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
# Mon, 04 Jan 2021 18:24:23 GMT
ARG ODOO_RELEASE=20210104
# Mon, 04 Jan 2021 18:24:23 GMT
ARG ODOO_SHA=d2d08a4c0dfac6b1aeeb616d9c948eb441876670
# Mon, 04 Jan 2021 18:25:13 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=d2d08a4c0dfac6b1aeeb616d9c948eb441876670
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 04 Jan 2021 18:25:14 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 04 Jan 2021 18:25:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 04 Jan 2021 18:25:15 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=d2d08a4c0dfac6b1aeeb616d9c948eb441876670
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 04 Jan 2021 18:25:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 Jan 2021 18:25:15 GMT
EXPOSE 8069 8071 8072
# Mon, 04 Jan 2021 18:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 Jan 2021 18:25:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 04 Jan 2021 18:25:16 GMT
USER odoo
# Mon, 04 Jan 2021 18:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Jan 2021 18:25:16 GMT
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
	-	`sha256:c4078a798960cb32f3dac6aabcd98dea671e7dc78bc123e23a41bdc1b6ecfc41`  
		Last Modified: Mon, 04 Jan 2021 18:27:15 GMT  
		Size: 130.3 MB (130309252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23def59242ec7a2f25cff0f1f7731a5e5d64a255243e5057d808a17604497920`  
		Last Modified: Mon, 04 Jan 2021 18:26:50 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d54d8621f6a86689a1a4f4b3489ca98bbf545356d0a431c5b21395f9bd9f3a`  
		Last Modified: Mon, 04 Jan 2021 18:26:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd811b127840ecdc890cea20859dc9b6850f3467d111703fa6a246f4d046a2b0`  
		Last Modified: Mon, 04 Jan 2021 18:26:51 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1dba757fe4b7cf74e566d608b644dae23e8e967b8be9bcb54ed29e133d472c`  
		Last Modified: Mon, 04 Jan 2021 18:26:50 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:592798f9cb772a97b7225210b0dad6867c266ec4540352249b27f472a341620c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:a25097a9e16b2b1a393a091c40c31091b5059ab8c5cd7cc61f42ad9e2db59d82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396739519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450b05890368ef750f12616c4e94cc6b17decb8e60f0a2fea3021ba75e3c6cf6`
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
# Mon, 04 Jan 2021 18:24:23 GMT
ARG ODOO_RELEASE=20210104
# Mon, 04 Jan 2021 18:24:23 GMT
ARG ODOO_SHA=d2d08a4c0dfac6b1aeeb616d9c948eb441876670
# Mon, 04 Jan 2021 18:25:13 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=d2d08a4c0dfac6b1aeeb616d9c948eb441876670
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 04 Jan 2021 18:25:14 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 04 Jan 2021 18:25:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 04 Jan 2021 18:25:15 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=d2d08a4c0dfac6b1aeeb616d9c948eb441876670
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 04 Jan 2021 18:25:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 Jan 2021 18:25:15 GMT
EXPOSE 8069 8071 8072
# Mon, 04 Jan 2021 18:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 Jan 2021 18:25:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 04 Jan 2021 18:25:16 GMT
USER odoo
# Mon, 04 Jan 2021 18:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Jan 2021 18:25:16 GMT
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
	-	`sha256:c4078a798960cb32f3dac6aabcd98dea671e7dc78bc123e23a41bdc1b6ecfc41`  
		Last Modified: Mon, 04 Jan 2021 18:27:15 GMT  
		Size: 130.3 MB (130309252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23def59242ec7a2f25cff0f1f7731a5e5d64a255243e5057d808a17604497920`  
		Last Modified: Mon, 04 Jan 2021 18:26:50 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d54d8621f6a86689a1a4f4b3489ca98bbf545356d0a431c5b21395f9bd9f3a`  
		Last Modified: Mon, 04 Jan 2021 18:26:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd811b127840ecdc890cea20859dc9b6850f3467d111703fa6a246f4d046a2b0`  
		Last Modified: Mon, 04 Jan 2021 18:26:51 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1dba757fe4b7cf74e566d608b644dae23e8e967b8be9bcb54ed29e133d472c`  
		Last Modified: Mon, 04 Jan 2021 18:26:50 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:3b695fe6357e5f762486230c1444ef428c56ce09462a0a56bd3d972cb8ee49d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:a6a8bca7b8d9fe0b42f63c425f1ed6c62052f1740900a91c9bbb870a3cd7bba9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386347472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aabe33663f052a01a095eb77877e580ccb82e6900283262ce6b9f225e62f298`
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
# Mon, 04 Jan 2021 18:23:18 GMT
ARG ODOO_RELEASE=20210104
# Mon, 04 Jan 2021 18:23:18 GMT
ARG ODOO_SHA=15b85a12eb661426316e255cfc888a1ca0914db1
# Mon, 04 Jan 2021 18:24:08 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=15b85a12eb661426316e255cfc888a1ca0914db1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 04 Jan 2021 18:24:09 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 04 Jan 2021 18:24:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 04 Jan 2021 18:24:10 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=15b85a12eb661426316e255cfc888a1ca0914db1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 04 Jan 2021 18:24:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 Jan 2021 18:24:10 GMT
EXPOSE 8069 8071 8072
# Mon, 04 Jan 2021 18:24:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 Jan 2021 18:24:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 04 Jan 2021 18:24:11 GMT
USER odoo
# Mon, 04 Jan 2021 18:24:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Jan 2021 18:24:12 GMT
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
	-	`sha256:0ac46abf7482e9e525b0b0ccc28fed7c7c4db36cd2283f6e16f30434e996c394`  
		Last Modified: Mon, 04 Jan 2021 18:26:43 GMT  
		Size: 148.9 MB (148897140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e96f73d5de8f474e186f2e9f542c5d90aeb70f193c132a46b1c1ebbd3d5423`  
		Last Modified: Mon, 04 Jan 2021 18:26:14 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0996a25fcaf09233919de01602b04afc3752231a6267a223f8b048815f21f1a4`  
		Last Modified: Mon, 04 Jan 2021 18:26:15 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f07f207a689005aecdb09d18c947a57d0fb5b473faae83506e6c2267ac36f5`  
		Last Modified: Mon, 04 Jan 2021 18:26:14 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df79841a0ed296041aea76d3c497e8a66e215d57e79f68e8703db7fa365e840`  
		Last Modified: Mon, 04 Jan 2021 18:26:14 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:3b695fe6357e5f762486230c1444ef428c56ce09462a0a56bd3d972cb8ee49d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:a6a8bca7b8d9fe0b42f63c425f1ed6c62052f1740900a91c9bbb870a3cd7bba9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386347472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aabe33663f052a01a095eb77877e580ccb82e6900283262ce6b9f225e62f298`
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
# Mon, 04 Jan 2021 18:23:18 GMT
ARG ODOO_RELEASE=20210104
# Mon, 04 Jan 2021 18:23:18 GMT
ARG ODOO_SHA=15b85a12eb661426316e255cfc888a1ca0914db1
# Mon, 04 Jan 2021 18:24:08 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=15b85a12eb661426316e255cfc888a1ca0914db1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 04 Jan 2021 18:24:09 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 04 Jan 2021 18:24:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 04 Jan 2021 18:24:10 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=15b85a12eb661426316e255cfc888a1ca0914db1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 04 Jan 2021 18:24:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 Jan 2021 18:24:10 GMT
EXPOSE 8069 8071 8072
# Mon, 04 Jan 2021 18:24:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 Jan 2021 18:24:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 04 Jan 2021 18:24:11 GMT
USER odoo
# Mon, 04 Jan 2021 18:24:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Jan 2021 18:24:12 GMT
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
	-	`sha256:0ac46abf7482e9e525b0b0ccc28fed7c7c4db36cd2283f6e16f30434e996c394`  
		Last Modified: Mon, 04 Jan 2021 18:26:43 GMT  
		Size: 148.9 MB (148897140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e96f73d5de8f474e186f2e9f542c5d90aeb70f193c132a46b1c1ebbd3d5423`  
		Last Modified: Mon, 04 Jan 2021 18:26:14 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0996a25fcaf09233919de01602b04afc3752231a6267a223f8b048815f21f1a4`  
		Last Modified: Mon, 04 Jan 2021 18:26:15 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f07f207a689005aecdb09d18c947a57d0fb5b473faae83506e6c2267ac36f5`  
		Last Modified: Mon, 04 Jan 2021 18:26:14 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df79841a0ed296041aea76d3c497e8a66e215d57e79f68e8703db7fa365e840`  
		Last Modified: Mon, 04 Jan 2021 18:26:14 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:02bdcf58a3801d13f62fa2ade4a183e4bfbfb056fee9ed64c06c45e24eab4687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:23dfc9de3548f16817fe648a0dda17c566faa31ae806bf53281f1f74e886edd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.4 MB (404367818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147ca9fc691922defa55503b41157dffd74d146003953c932fc584fc259e3ca2`
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
# Mon, 04 Jan 2021 18:22:01 GMT
ARG ODOO_RELEASE=20210104
# Mon, 04 Jan 2021 18:22:02 GMT
ARG ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
# Mon, 04 Jan 2021 18:23:00 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 04 Jan 2021 18:23:01 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 04 Jan 2021 18:23:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 04 Jan 2021 18:23:02 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 04 Jan 2021 18:23:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 Jan 2021 18:23:02 GMT
EXPOSE 8069 8071 8072
# Mon, 04 Jan 2021 18:23:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 Jan 2021 18:23:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 04 Jan 2021 18:23:03 GMT
USER odoo
# Mon, 04 Jan 2021 18:23:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Jan 2021 18:23:03 GMT
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
	-	`sha256:82fbb70cacb8b09b8fb9a8d04fda82f6540427fc50545a0a676139bba4a4a186`  
		Last Modified: Mon, 04 Jan 2021 18:26:05 GMT  
		Size: 160.9 MB (160874293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599b946630292f82db18c345e9ec3a140ff7e812b12ee9d98133a59530046de9`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c8bcdc0422486b06953fe304dee0bb7b18eeaa78c26b5135278c2b724f955e`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa23a330216453fefb15e67922a055fe1541489b613804acbd14f94f51e22c5d`  
		Last Modified: Mon, 04 Jan 2021 18:25:34 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd1dc685ce01a39daccda579f6ff9adff94ced9efc19811e2f6153f9a8f58de`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:02bdcf58a3801d13f62fa2ade4a183e4bfbfb056fee9ed64c06c45e24eab4687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:23dfc9de3548f16817fe648a0dda17c566faa31ae806bf53281f1f74e886edd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.4 MB (404367818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147ca9fc691922defa55503b41157dffd74d146003953c932fc584fc259e3ca2`
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
# Mon, 04 Jan 2021 18:22:01 GMT
ARG ODOO_RELEASE=20210104
# Mon, 04 Jan 2021 18:22:02 GMT
ARG ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
# Mon, 04 Jan 2021 18:23:00 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 04 Jan 2021 18:23:01 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 04 Jan 2021 18:23:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 04 Jan 2021 18:23:02 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 04 Jan 2021 18:23:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 Jan 2021 18:23:02 GMT
EXPOSE 8069 8071 8072
# Mon, 04 Jan 2021 18:23:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 Jan 2021 18:23:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 04 Jan 2021 18:23:03 GMT
USER odoo
# Mon, 04 Jan 2021 18:23:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Jan 2021 18:23:03 GMT
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
	-	`sha256:82fbb70cacb8b09b8fb9a8d04fda82f6540427fc50545a0a676139bba4a4a186`  
		Last Modified: Mon, 04 Jan 2021 18:26:05 GMT  
		Size: 160.9 MB (160874293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599b946630292f82db18c345e9ec3a140ff7e812b12ee9d98133a59530046de9`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c8bcdc0422486b06953fe304dee0bb7b18eeaa78c26b5135278c2b724f955e`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa23a330216453fefb15e67922a055fe1541489b613804acbd14f94f51e22c5d`  
		Last Modified: Mon, 04 Jan 2021 18:25:34 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd1dc685ce01a39daccda579f6ff9adff94ced9efc19811e2f6153f9a8f58de`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:02bdcf58a3801d13f62fa2ade4a183e4bfbfb056fee9ed64c06c45e24eab4687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:23dfc9de3548f16817fe648a0dda17c566faa31ae806bf53281f1f74e886edd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.4 MB (404367818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147ca9fc691922defa55503b41157dffd74d146003953c932fc584fc259e3ca2`
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
# Mon, 04 Jan 2021 18:22:01 GMT
ARG ODOO_RELEASE=20210104
# Mon, 04 Jan 2021 18:22:02 GMT
ARG ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
# Mon, 04 Jan 2021 18:23:00 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 04 Jan 2021 18:23:01 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 04 Jan 2021 18:23:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 04 Jan 2021 18:23:02 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 04 Jan 2021 18:23:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 Jan 2021 18:23:02 GMT
EXPOSE 8069 8071 8072
# Mon, 04 Jan 2021 18:23:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 Jan 2021 18:23:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 04 Jan 2021 18:23:03 GMT
USER odoo
# Mon, 04 Jan 2021 18:23:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Jan 2021 18:23:03 GMT
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
	-	`sha256:82fbb70cacb8b09b8fb9a8d04fda82f6540427fc50545a0a676139bba4a4a186`  
		Last Modified: Mon, 04 Jan 2021 18:26:05 GMT  
		Size: 160.9 MB (160874293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599b946630292f82db18c345e9ec3a140ff7e812b12ee9d98133a59530046de9`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c8bcdc0422486b06953fe304dee0bb7b18eeaa78c26b5135278c2b724f955e`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa23a330216453fefb15e67922a055fe1541489b613804acbd14f94f51e22c5d`  
		Last Modified: Mon, 04 Jan 2021 18:25:34 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd1dc685ce01a39daccda579f6ff9adff94ced9efc19811e2f6153f9a8f58de`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
