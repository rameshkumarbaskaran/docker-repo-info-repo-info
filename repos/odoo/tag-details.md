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
$ docker pull odoo@sha256:bf54271de47faa590175722827a30cd02e0829fd834ad7f8a77708f65a6e6681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:9a0fe40fd9ebd93b1609d9b27d18875d18680afadac5a16169c5c15d70bfd7fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540336157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b51bdd2008dc3593b3f7859a6d1d692b49cd559338c58db8cce6b64ecf61a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:52:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:52:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:52:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:56:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:56:59 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:57:02 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:57:02 GMT
ENV ODOO_VERSION=13.0
# Tue, 13 Sep 2022 06:57:02 GMT
ARG ODOO_RELEASE=20220902
# Tue, 13 Sep 2022 06:57:02 GMT
ARG ODOO_SHA=d4da6396aed6e32579f525a45a22a5d4edfd3629
# Tue, 13 Sep 2022 06:58:15 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=d4da6396aed6e32579f525a45a22a5d4edfd3629
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Sep 2022 06:58:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Sep 2022 06:58:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Sep 2022 06:58:19 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=d4da6396aed6e32579f525a45a22a5d4edfd3629
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Sep 2022 06:58:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Sep 2022 06:58:19 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Sep 2022 06:58:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Sep 2022 06:58:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Sep 2022 06:58:20 GMT
USER odoo
# Tue, 13 Sep 2022 06:58:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Sep 2022 06:58:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5fc672d49e136ecb8725a1f4d4d42c67c27dbb0cde157b5c53ae2b79e69aa`  
		Last Modified: Tue, 13 Sep 2022 07:00:46 GMT  
		Size: 207.1 MB (207143846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eba5ac56590f61c1bbc1a6ae4c2a367215fcc0f8681fa113bc534175eefac3`  
		Last Modified: Tue, 13 Sep 2022 07:00:25 GMT  
		Size: 13.4 MB (13442347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79773cdec162998e8fc6cfb2a99a8d2b8ae9db406f671c4f41cfdfca0af9b9d4`  
		Last Modified: Tue, 13 Sep 2022 07:00:22 GMT  
		Size: 454.2 KB (454225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7b965ab1fbcf9330a19881b240b1d750441da1072acaad8fb3a6376f029120`  
		Last Modified: Tue, 13 Sep 2022 07:00:53 GMT  
		Size: 292.2 MB (292162723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac5190b861edb2b4469cbb8a031d0d3c599ffe5d7dc588dfe2d56868843dcf8`  
		Last Modified: Tue, 13 Sep 2022 07:00:20 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7957ef5bd54d157e70f939a58a599d997595ec273c008c7e13c83f726dcbe396`  
		Last Modified: Tue, 13 Sep 2022 07:00:20 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95dd83107fba49c4fb0a123979e7feb8cd5ece92e7bb2bffb9454fb7043b0ff0`  
		Last Modified: Tue, 13 Sep 2022 07:00:20 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7383f62082d048e8592951b0abf7e0151aa19f1ad08673eac23127b97fbfeb78`  
		Last Modified: Tue, 13 Sep 2022 07:00:20 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:bf54271de47faa590175722827a30cd02e0829fd834ad7f8a77708f65a6e6681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:9a0fe40fd9ebd93b1609d9b27d18875d18680afadac5a16169c5c15d70bfd7fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540336157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b51bdd2008dc3593b3f7859a6d1d692b49cd559338c58db8cce6b64ecf61a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:52:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:52:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:52:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:56:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:56:59 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:57:02 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:57:02 GMT
ENV ODOO_VERSION=13.0
# Tue, 13 Sep 2022 06:57:02 GMT
ARG ODOO_RELEASE=20220902
# Tue, 13 Sep 2022 06:57:02 GMT
ARG ODOO_SHA=d4da6396aed6e32579f525a45a22a5d4edfd3629
# Tue, 13 Sep 2022 06:58:15 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=d4da6396aed6e32579f525a45a22a5d4edfd3629
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Sep 2022 06:58:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Sep 2022 06:58:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Sep 2022 06:58:19 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=d4da6396aed6e32579f525a45a22a5d4edfd3629
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Sep 2022 06:58:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Sep 2022 06:58:19 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Sep 2022 06:58:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Sep 2022 06:58:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Sep 2022 06:58:20 GMT
USER odoo
# Tue, 13 Sep 2022 06:58:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Sep 2022 06:58:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5fc672d49e136ecb8725a1f4d4d42c67c27dbb0cde157b5c53ae2b79e69aa`  
		Last Modified: Tue, 13 Sep 2022 07:00:46 GMT  
		Size: 207.1 MB (207143846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eba5ac56590f61c1bbc1a6ae4c2a367215fcc0f8681fa113bc534175eefac3`  
		Last Modified: Tue, 13 Sep 2022 07:00:25 GMT  
		Size: 13.4 MB (13442347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79773cdec162998e8fc6cfb2a99a8d2b8ae9db406f671c4f41cfdfca0af9b9d4`  
		Last Modified: Tue, 13 Sep 2022 07:00:22 GMT  
		Size: 454.2 KB (454225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7b965ab1fbcf9330a19881b240b1d750441da1072acaad8fb3a6376f029120`  
		Last Modified: Tue, 13 Sep 2022 07:00:53 GMT  
		Size: 292.2 MB (292162723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac5190b861edb2b4469cbb8a031d0d3c599ffe5d7dc588dfe2d56868843dcf8`  
		Last Modified: Tue, 13 Sep 2022 07:00:20 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7957ef5bd54d157e70f939a58a599d997595ec273c008c7e13c83f726dcbe396`  
		Last Modified: Tue, 13 Sep 2022 07:00:20 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95dd83107fba49c4fb0a123979e7feb8cd5ece92e7bb2bffb9454fb7043b0ff0`  
		Last Modified: Tue, 13 Sep 2022 07:00:20 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7383f62082d048e8592951b0abf7e0151aa19f1ad08673eac23127b97fbfeb78`  
		Last Modified: Tue, 13 Sep 2022 07:00:20 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:cdf71554f3fa516df335c416d41470aa6f8bd9d965c618536133d52ad1dc9b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:e965b0d29ec831b5c397db5ac16fce8be889f9ff14db06d0994ea9572e90e164
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530836506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b93be14f2e06ea00187a2c1794b3f502b088491fa01ee208d57a6e61223c36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:52:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:52:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:52:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:54:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:54:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:54:16 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:54:16 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Sep 2022 06:54:16 GMT
ARG ODOO_RELEASE=20220902
# Tue, 13 Sep 2022 06:54:16 GMT
ARG ODOO_SHA=5dd3ba425de996c22c1f34383c8897f3c5930c0c
# Tue, 13 Sep 2022 06:55:33 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=5dd3ba425de996c22c1f34383c8897f3c5930c0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Sep 2022 06:55:37 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Sep 2022 06:55:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Sep 2022 06:55:38 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=5dd3ba425de996c22c1f34383c8897f3c5930c0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Sep 2022 06:55:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Sep 2022 06:55:38 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Sep 2022 06:55:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Sep 2022 06:55:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Sep 2022 06:55:38 GMT
USER odoo
# Tue, 13 Sep 2022 06:55:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Sep 2022 06:55:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db956de1ff39a9971927e9b97aed9378d75cda5bc3767047513019ca339ecc`  
		Last Modified: Tue, 13 Sep 2022 07:00:04 GMT  
		Size: 213.2 MB (213182384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e999a30d3af868cc7a2fe2ce4051e6598baec42acba7528ce4cc01707daefc19`  
		Last Modified: Tue, 13 Sep 2022 06:59:40 GMT  
		Size: 13.4 MB (13443898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eae60c9aa41d0da30fc7580b68a75025f6ce13ed515f6f4e535a1730b013df8`  
		Last Modified: Tue, 13 Sep 2022 06:59:38 GMT  
		Size: 454.2 KB (454250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8810aeeccc644aed8e11c1cf6d746cafece404c30ad67cf8c692dd12b74e2e`  
		Last Modified: Tue, 13 Sep 2022 07:00:09 GMT  
		Size: 276.6 MB (276622960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707716931adec3baa7d81e67fc75ae1ec1de71e83074fe6711ef09b45e95e687`  
		Last Modified: Tue, 13 Sep 2022 06:59:35 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb6d78755ef33fdef311f720f0b00baf868cdc8911a9eaad6c034a5df7c72d4`  
		Last Modified: Tue, 13 Sep 2022 06:59:35 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c807c16c062d30cd98304ca0abb2c5681b53211a0b5c25384527722f2210ee0`  
		Last Modified: Tue, 13 Sep 2022 06:59:35 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a29944008e2e8960659c6a20cbf908f8f0ffad2d0b0c974a70643f053b46843`  
		Last Modified: Tue, 13 Sep 2022 06:59:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:cdf71554f3fa516df335c416d41470aa6f8bd9d965c618536133d52ad1dc9b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:e965b0d29ec831b5c397db5ac16fce8be889f9ff14db06d0994ea9572e90e164
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530836506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b93be14f2e06ea00187a2c1794b3f502b088491fa01ee208d57a6e61223c36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:52:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:52:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:52:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:54:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:54:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:54:16 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:54:16 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Sep 2022 06:54:16 GMT
ARG ODOO_RELEASE=20220902
# Tue, 13 Sep 2022 06:54:16 GMT
ARG ODOO_SHA=5dd3ba425de996c22c1f34383c8897f3c5930c0c
# Tue, 13 Sep 2022 06:55:33 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=5dd3ba425de996c22c1f34383c8897f3c5930c0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Sep 2022 06:55:37 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Sep 2022 06:55:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Sep 2022 06:55:38 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=5dd3ba425de996c22c1f34383c8897f3c5930c0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Sep 2022 06:55:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Sep 2022 06:55:38 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Sep 2022 06:55:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Sep 2022 06:55:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Sep 2022 06:55:38 GMT
USER odoo
# Tue, 13 Sep 2022 06:55:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Sep 2022 06:55:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db956de1ff39a9971927e9b97aed9378d75cda5bc3767047513019ca339ecc`  
		Last Modified: Tue, 13 Sep 2022 07:00:04 GMT  
		Size: 213.2 MB (213182384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e999a30d3af868cc7a2fe2ce4051e6598baec42acba7528ce4cc01707daefc19`  
		Last Modified: Tue, 13 Sep 2022 06:59:40 GMT  
		Size: 13.4 MB (13443898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eae60c9aa41d0da30fc7580b68a75025f6ce13ed515f6f4e535a1730b013df8`  
		Last Modified: Tue, 13 Sep 2022 06:59:38 GMT  
		Size: 454.2 KB (454250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8810aeeccc644aed8e11c1cf6d746cafece404c30ad67cf8c692dd12b74e2e`  
		Last Modified: Tue, 13 Sep 2022 07:00:09 GMT  
		Size: 276.6 MB (276622960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707716931adec3baa7d81e67fc75ae1ec1de71e83074fe6711ef09b45e95e687`  
		Last Modified: Tue, 13 Sep 2022 06:59:35 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb6d78755ef33fdef311f720f0b00baf868cdc8911a9eaad6c034a5df7c72d4`  
		Last Modified: Tue, 13 Sep 2022 06:59:35 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c807c16c062d30cd98304ca0abb2c5681b53211a0b5c25384527722f2210ee0`  
		Last Modified: Tue, 13 Sep 2022 06:59:35 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a29944008e2e8960659c6a20cbf908f8f0ffad2d0b0c974a70643f053b46843`  
		Last Modified: Tue, 13 Sep 2022 06:59:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:a031c56ca922d2d6261068a8683ff41bb3b6801fd62ebbd55ae6b4f9b6ea2191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:68b80fe23c7628e9c5598c9cbf691d152b18be1e5ccbf1bfd82695c8a9f1d3be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557834753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64086f4235b99e4fb0fb905f1faa7fea2947dad926e6117b5e073f9ee8a4d33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:49:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:49:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:49:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:50:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:51:11 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:51:11 GMT
ENV ODOO_VERSION=15.0
# Tue, 13 Sep 2022 06:51:12 GMT
ARG ODOO_RELEASE=20220902
# Tue, 13 Sep 2022 06:51:12 GMT
ARG ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
# Tue, 13 Sep 2022 06:52:32 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Sep 2022 06:52:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Sep 2022 06:52:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Sep 2022 06:52:37 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Sep 2022 06:52:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Sep 2022 06:52:37 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Sep 2022 06:52:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Sep 2022 06:52:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Sep 2022 06:52:37 GMT
USER odoo
# Tue, 13 Sep 2022 06:52:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Sep 2022 06:52:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b73f80e874fc2998c5758d4c8d65d96b8f9ff5544bf075b31ed62614eb1071b`  
		Last Modified: Tue, 13 Sep 2022 06:59:13 GMT  
		Size: 220.3 MB (220296011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc15e3be86616ca7da0dcee3866c41e512cc3db88484000d55cc15b194c5b4`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 2.5 MB (2513532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69e7aa750a4c8478c7e63dba1a777a14a00d608706683711ced35910615545`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 449.9 KB (449869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2abdba36a6b1b535554ad4234b99333c91ec73ea7bb7930ef3a5100514d54e1`  
		Last Modified: Tue, 13 Sep 2022 06:59:21 GMT  
		Size: 303.2 MB (303168757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1391fd906b3ad65b2ef8480014aec6e6db9814f08616915ce9ec33f6a62b69a1`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05780b88ded15ca7f26ad55d1e7577d8c58ab7ab00882e8051e19156c26a7f84`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52439d711f43551963deeae77d923287e6c8f67e178ca198ce9ab7bde53d7522`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd51f312699a823b9e7188fe18575bb0016162a05e2524b322dac8412751bc1`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:a031c56ca922d2d6261068a8683ff41bb3b6801fd62ebbd55ae6b4f9b6ea2191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:68b80fe23c7628e9c5598c9cbf691d152b18be1e5ccbf1bfd82695c8a9f1d3be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557834753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64086f4235b99e4fb0fb905f1faa7fea2947dad926e6117b5e073f9ee8a4d33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:49:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:49:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:49:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:50:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:51:11 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:51:11 GMT
ENV ODOO_VERSION=15.0
# Tue, 13 Sep 2022 06:51:12 GMT
ARG ODOO_RELEASE=20220902
# Tue, 13 Sep 2022 06:51:12 GMT
ARG ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
# Tue, 13 Sep 2022 06:52:32 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Sep 2022 06:52:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Sep 2022 06:52:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Sep 2022 06:52:37 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Sep 2022 06:52:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Sep 2022 06:52:37 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Sep 2022 06:52:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Sep 2022 06:52:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Sep 2022 06:52:37 GMT
USER odoo
# Tue, 13 Sep 2022 06:52:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Sep 2022 06:52:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b73f80e874fc2998c5758d4c8d65d96b8f9ff5544bf075b31ed62614eb1071b`  
		Last Modified: Tue, 13 Sep 2022 06:59:13 GMT  
		Size: 220.3 MB (220296011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc15e3be86616ca7da0dcee3866c41e512cc3db88484000d55cc15b194c5b4`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 2.5 MB (2513532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69e7aa750a4c8478c7e63dba1a777a14a00d608706683711ced35910615545`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 449.9 KB (449869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2abdba36a6b1b535554ad4234b99333c91ec73ea7bb7930ef3a5100514d54e1`  
		Last Modified: Tue, 13 Sep 2022 06:59:21 GMT  
		Size: 303.2 MB (303168757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1391fd906b3ad65b2ef8480014aec6e6db9814f08616915ce9ec33f6a62b69a1`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05780b88ded15ca7f26ad55d1e7577d8c58ab7ab00882e8051e19156c26a7f84`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52439d711f43551963deeae77d923287e6c8f67e178ca198ce9ab7bde53d7522`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd51f312699a823b9e7188fe18575bb0016162a05e2524b322dac8412751bc1`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:a031c56ca922d2d6261068a8683ff41bb3b6801fd62ebbd55ae6b4f9b6ea2191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:68b80fe23c7628e9c5598c9cbf691d152b18be1e5ccbf1bfd82695c8a9f1d3be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557834753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64086f4235b99e4fb0fb905f1faa7fea2947dad926e6117b5e073f9ee8a4d33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:49:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:49:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:49:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:50:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:51:11 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:51:11 GMT
ENV ODOO_VERSION=15.0
# Tue, 13 Sep 2022 06:51:12 GMT
ARG ODOO_RELEASE=20220902
# Tue, 13 Sep 2022 06:51:12 GMT
ARG ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
# Tue, 13 Sep 2022 06:52:32 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Sep 2022 06:52:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Sep 2022 06:52:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Sep 2022 06:52:37 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Sep 2022 06:52:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Sep 2022 06:52:37 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Sep 2022 06:52:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Sep 2022 06:52:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Sep 2022 06:52:37 GMT
USER odoo
# Tue, 13 Sep 2022 06:52:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Sep 2022 06:52:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b73f80e874fc2998c5758d4c8d65d96b8f9ff5544bf075b31ed62614eb1071b`  
		Last Modified: Tue, 13 Sep 2022 06:59:13 GMT  
		Size: 220.3 MB (220296011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc15e3be86616ca7da0dcee3866c41e512cc3db88484000d55cc15b194c5b4`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 2.5 MB (2513532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69e7aa750a4c8478c7e63dba1a777a14a00d608706683711ced35910615545`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 449.9 KB (449869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2abdba36a6b1b535554ad4234b99333c91ec73ea7bb7930ef3a5100514d54e1`  
		Last Modified: Tue, 13 Sep 2022 06:59:21 GMT  
		Size: 303.2 MB (303168757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1391fd906b3ad65b2ef8480014aec6e6db9814f08616915ce9ec33f6a62b69a1`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05780b88ded15ca7f26ad55d1e7577d8c58ab7ab00882e8051e19156c26a7f84`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52439d711f43551963deeae77d923287e6c8f67e178ca198ce9ab7bde53d7522`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd51f312699a823b9e7188fe18575bb0016162a05e2524b322dac8412751bc1`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
