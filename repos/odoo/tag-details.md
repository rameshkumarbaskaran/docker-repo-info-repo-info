<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:latest`](#odoolatest)

## `odoo:14`

```console
$ docker pull odoo@sha256:5dc582040f17f5199b9b0636cb53a9c7d7c8bfecb563ba86f1a8141ca8644bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:3c1bb2652b522b1477bdc2df80ad00b7aa947159beb72271771c61a4d5815e5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.5 MB (532495233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43db0a091ef8387b7a38b7f229da1de5eafad02ecc5cb85dedb52a3deda8c471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:30:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 May 2023 04:30:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 May 2023 04:30:10 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 04:31:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 May 2023 04:32:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:32:13 GMT
RUN npm install -g rtlcss
# Tue, 23 May 2023 04:32:13 GMT
ENV ODOO_VERSION=14.0
# Tue, 30 May 2023 22:24:44 GMT
ARG ODOO_RELEASE=20230530
# Tue, 30 May 2023 22:24:44 GMT
ARG ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
# Tue, 30 May 2023 22:26:12 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 May 2023 22:26:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 May 2023 22:26:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 May 2023 22:26:16 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 May 2023 22:26:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 May 2023 22:26:16 GMT
EXPOSE 8069 8071 8072
# Tue, 30 May 2023 22:26:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 May 2023 22:26:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 May 2023 22:26:16 GMT
USER odoo
# Tue, 30 May 2023 22:26:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 May 2023 22:26:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aca9b3ba696a60bb5aefda89b215fb65bea612b9473c5bb7742a12d457b43c8`  
		Last Modified: Tue, 23 May 2023 04:35:47 GMT  
		Size: 213.2 MB (213200599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867a72128df6cf291a48f4eac739e1141e8731a8f7bd8ff82010ed2f2b912b15`  
		Last Modified: Tue, 23 May 2023 04:35:27 GMT  
		Size: 13.5 MB (13520105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33611cbfda398265d43bf6f537232ff1dfb60c7079746976ee090dbec1ddbf30`  
		Last Modified: Tue, 23 May 2023 04:35:25 GMT  
		Size: 456.7 KB (456694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5330adb7de797b313f9d8a363e788d42784bc4f9dd67c2ae20901621e6529a85`  
		Last Modified: Tue, 30 May 2023 22:28:27 GMT  
		Size: 278.2 MB (278176792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac21bdc37c43a7f92a44eb82922f3c31bed55d0e371a9a5207768fcabc3c2fc3`  
		Last Modified: Tue, 30 May 2023 22:27:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44bbc7e5a9b1df88a8de49f86851f6573b17fb959d1d57275ace205047fbeae`  
		Last Modified: Tue, 30 May 2023 22:27:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36557955c4f0ec40898ecd67b90922d334bc691983b771808934d055ae233c4`  
		Last Modified: Tue, 30 May 2023 22:27:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3137df83def1ca1ef745defc9b1cd34a7c9d2c90d24cdccc8f994e43d65d488d`  
		Last Modified: Tue, 30 May 2023 22:27:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:5dc582040f17f5199b9b0636cb53a9c7d7c8bfecb563ba86f1a8141ca8644bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:3c1bb2652b522b1477bdc2df80ad00b7aa947159beb72271771c61a4d5815e5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.5 MB (532495233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43db0a091ef8387b7a38b7f229da1de5eafad02ecc5cb85dedb52a3deda8c471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:30:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 May 2023 04:30:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 May 2023 04:30:10 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 04:31:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 May 2023 04:32:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:32:13 GMT
RUN npm install -g rtlcss
# Tue, 23 May 2023 04:32:13 GMT
ENV ODOO_VERSION=14.0
# Tue, 30 May 2023 22:24:44 GMT
ARG ODOO_RELEASE=20230530
# Tue, 30 May 2023 22:24:44 GMT
ARG ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
# Tue, 30 May 2023 22:26:12 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 May 2023 22:26:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 May 2023 22:26:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 May 2023 22:26:16 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 May 2023 22:26:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 May 2023 22:26:16 GMT
EXPOSE 8069 8071 8072
# Tue, 30 May 2023 22:26:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 May 2023 22:26:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 May 2023 22:26:16 GMT
USER odoo
# Tue, 30 May 2023 22:26:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 May 2023 22:26:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aca9b3ba696a60bb5aefda89b215fb65bea612b9473c5bb7742a12d457b43c8`  
		Last Modified: Tue, 23 May 2023 04:35:47 GMT  
		Size: 213.2 MB (213200599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867a72128df6cf291a48f4eac739e1141e8731a8f7bd8ff82010ed2f2b912b15`  
		Last Modified: Tue, 23 May 2023 04:35:27 GMT  
		Size: 13.5 MB (13520105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33611cbfda398265d43bf6f537232ff1dfb60c7079746976ee090dbec1ddbf30`  
		Last Modified: Tue, 23 May 2023 04:35:25 GMT  
		Size: 456.7 KB (456694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5330adb7de797b313f9d8a363e788d42784bc4f9dd67c2ae20901621e6529a85`  
		Last Modified: Tue, 30 May 2023 22:28:27 GMT  
		Size: 278.2 MB (278176792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac21bdc37c43a7f92a44eb82922f3c31bed55d0e371a9a5207768fcabc3c2fc3`  
		Last Modified: Tue, 30 May 2023 22:27:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44bbc7e5a9b1df88a8de49f86851f6573b17fb959d1d57275ace205047fbeae`  
		Last Modified: Tue, 30 May 2023 22:27:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36557955c4f0ec40898ecd67b90922d334bc691983b771808934d055ae233c4`  
		Last Modified: Tue, 30 May 2023 22:27:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3137df83def1ca1ef745defc9b1cd34a7c9d2c90d24cdccc8f994e43d65d488d`  
		Last Modified: Tue, 30 May 2023 22:27:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:44694a76a4e7ead7522e2b908627e9535bc941cef1897206fd1d08cf49560706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:97854f803a066904ea0ddc5125597c9e4d57587d797e49fbc7590fdfa6d52f85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.0 MB (561017411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cbf688ff58861a9454a835492588f43fe842a736c4e185906d970ea0f705ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:25:09 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 May 2023 04:25:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 May 2023 04:25:09 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 04:26:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 May 2023 04:26:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:26:56 GMT
RUN npm install -g rtlcss
# Tue, 23 May 2023 04:28:47 GMT
ENV ODOO_VERSION=15.0
# Tue, 30 May 2023 22:23:20 GMT
ARG ODOO_RELEASE=20230530
# Tue, 30 May 2023 22:23:20 GMT
ARG ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
# Tue, 30 May 2023 22:24:34 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 May 2023 22:24:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 May 2023 22:24:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 May 2023 22:24:39 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 May 2023 22:24:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 May 2023 22:24:39 GMT
EXPOSE 8069 8071 8072
# Tue, 30 May 2023 22:24:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 May 2023 22:24:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 May 2023 22:24:39 GMT
USER odoo
# Tue, 30 May 2023 22:24:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 May 2023 22:24:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1e9686d13cba605592a655c33e96fc273869f0b8c2767aea698575f4a1b0f8`  
		Last Modified: Tue, 23 May 2023 04:34:21 GMT  
		Size: 220.3 MB (220298635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7e1c3238f65b74dbec3b8f1d37c83ba05c91cdc1519bc296572d0344d0bcc2`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 2.6 MB (2576158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28ae768ba0baf0ccb8a34bf4c776dfd95d57e763b4152c3bd0f4125ef41c0dc`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 452.2 KB (452212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430449cedded94386a47b5044fc66396665bd73979db00cad189285264610091`  
		Last Modified: Tue, 30 May 2023 22:27:48 GMT  
		Size: 306.3 MB (306284360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c15983d891c695c556d4be0c54e9c93cacd423926c7247d14b996ea854fae5`  
		Last Modified: Tue, 30 May 2023 22:27:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e1c30bf2a516510cb3ee9bb8a65afcaa87f40cfd18e7be81984007361e5ce4`  
		Last Modified: Tue, 30 May 2023 22:27:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2dea3f8ed6512f1245c0d4c6c0302d9a35e632aa9f600932f774c6c2b35537`  
		Last Modified: Tue, 30 May 2023 22:27:16 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13af44807e5b35db6069fd8ba59e9693d5ada02e547b25598b441dbe2558ae4d`  
		Last Modified: Tue, 30 May 2023 22:27:16 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:44694a76a4e7ead7522e2b908627e9535bc941cef1897206fd1d08cf49560706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:97854f803a066904ea0ddc5125597c9e4d57587d797e49fbc7590fdfa6d52f85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.0 MB (561017411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cbf688ff58861a9454a835492588f43fe842a736c4e185906d970ea0f705ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:25:09 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 May 2023 04:25:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 May 2023 04:25:09 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 04:26:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 May 2023 04:26:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:26:56 GMT
RUN npm install -g rtlcss
# Tue, 23 May 2023 04:28:47 GMT
ENV ODOO_VERSION=15.0
# Tue, 30 May 2023 22:23:20 GMT
ARG ODOO_RELEASE=20230530
# Tue, 30 May 2023 22:23:20 GMT
ARG ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
# Tue, 30 May 2023 22:24:34 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 May 2023 22:24:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 May 2023 22:24:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 May 2023 22:24:39 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 May 2023 22:24:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 May 2023 22:24:39 GMT
EXPOSE 8069 8071 8072
# Tue, 30 May 2023 22:24:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 May 2023 22:24:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 May 2023 22:24:39 GMT
USER odoo
# Tue, 30 May 2023 22:24:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 May 2023 22:24:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1e9686d13cba605592a655c33e96fc273869f0b8c2767aea698575f4a1b0f8`  
		Last Modified: Tue, 23 May 2023 04:34:21 GMT  
		Size: 220.3 MB (220298635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7e1c3238f65b74dbec3b8f1d37c83ba05c91cdc1519bc296572d0344d0bcc2`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 2.6 MB (2576158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28ae768ba0baf0ccb8a34bf4c776dfd95d57e763b4152c3bd0f4125ef41c0dc`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 452.2 KB (452212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430449cedded94386a47b5044fc66396665bd73979db00cad189285264610091`  
		Last Modified: Tue, 30 May 2023 22:27:48 GMT  
		Size: 306.3 MB (306284360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c15983d891c695c556d4be0c54e9c93cacd423926c7247d14b996ea854fae5`  
		Last Modified: Tue, 30 May 2023 22:27:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e1c30bf2a516510cb3ee9bb8a65afcaa87f40cfd18e7be81984007361e5ce4`  
		Last Modified: Tue, 30 May 2023 22:27:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2dea3f8ed6512f1245c0d4c6c0302d9a35e632aa9f600932f774c6c2b35537`  
		Last Modified: Tue, 30 May 2023 22:27:16 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13af44807e5b35db6069fd8ba59e9693d5ada02e547b25598b441dbe2558ae4d`  
		Last Modified: Tue, 30 May 2023 22:27:16 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:6d2ce40a3f1c0f97ec87a3ce863b54cf161bd7a35133606f70da3271aaa43e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:9fa2ba18f412c9db7bb0662e8e2bf619f2ff087290a408fc75109759c5491707
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.5 MB (570475734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fe439d8cfc71750bbea1c6c2e64ac086ce3d8ccaa37c5f07a4122298d80d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:25:09 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 May 2023 04:25:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 May 2023 04:25:09 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 04:26:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 May 2023 04:26:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:26:56 GMT
RUN npm install -g rtlcss
# Tue, 23 May 2023 04:26:56 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 May 2023 22:21:27 GMT
ARG ODOO_RELEASE=20230530
# Tue, 30 May 2023 22:21:27 GMT
ARG ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
# Tue, 30 May 2023 22:23:04 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 May 2023 22:23:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 May 2023 22:23:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 May 2023 22:23:09 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 May 2023 22:23:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 May 2023 22:23:09 GMT
EXPOSE 8069 8071 8072
# Tue, 30 May 2023 22:23:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 May 2023 22:23:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 May 2023 22:23:10 GMT
USER odoo
# Tue, 30 May 2023 22:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 May 2023 22:23:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1e9686d13cba605592a655c33e96fc273869f0b8c2767aea698575f4a1b0f8`  
		Last Modified: Tue, 23 May 2023 04:34:21 GMT  
		Size: 220.3 MB (220298635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7e1c3238f65b74dbec3b8f1d37c83ba05c91cdc1519bc296572d0344d0bcc2`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 2.6 MB (2576158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28ae768ba0baf0ccb8a34bf4c776dfd95d57e763b4152c3bd0f4125ef41c0dc`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 452.2 KB (452212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6150d95afe7d506a4c7223441daf03b349bb0314aa46d47a23f54d0567a11f`  
		Last Modified: Tue, 30 May 2023 22:27:05 GMT  
		Size: 315.7 MB (315742679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce71b52cd625e5982111700383dc98040f3b77c476e875a579f8b85171c5294b`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7e57af2d47a67fb3ef9b04dd913aace0981abe529272f6ae52c6477011313b`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840837a3c8c998309f1165b48b52995aee13097bcaf032cd199d85154233418a`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4666c0234210bc294a74c80d821e1ff3100c2f6fa88ea4feee53fdc3dd784e`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:6d2ce40a3f1c0f97ec87a3ce863b54cf161bd7a35133606f70da3271aaa43e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:9fa2ba18f412c9db7bb0662e8e2bf619f2ff087290a408fc75109759c5491707
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.5 MB (570475734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fe439d8cfc71750bbea1c6c2e64ac086ce3d8ccaa37c5f07a4122298d80d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:25:09 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 May 2023 04:25:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 May 2023 04:25:09 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 04:26:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 May 2023 04:26:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:26:56 GMT
RUN npm install -g rtlcss
# Tue, 23 May 2023 04:26:56 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 May 2023 22:21:27 GMT
ARG ODOO_RELEASE=20230530
# Tue, 30 May 2023 22:21:27 GMT
ARG ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
# Tue, 30 May 2023 22:23:04 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 May 2023 22:23:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 May 2023 22:23:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 May 2023 22:23:09 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 May 2023 22:23:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 May 2023 22:23:09 GMT
EXPOSE 8069 8071 8072
# Tue, 30 May 2023 22:23:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 May 2023 22:23:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 May 2023 22:23:10 GMT
USER odoo
# Tue, 30 May 2023 22:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 May 2023 22:23:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1e9686d13cba605592a655c33e96fc273869f0b8c2767aea698575f4a1b0f8`  
		Last Modified: Tue, 23 May 2023 04:34:21 GMT  
		Size: 220.3 MB (220298635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7e1c3238f65b74dbec3b8f1d37c83ba05c91cdc1519bc296572d0344d0bcc2`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 2.6 MB (2576158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28ae768ba0baf0ccb8a34bf4c776dfd95d57e763b4152c3bd0f4125ef41c0dc`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 452.2 KB (452212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6150d95afe7d506a4c7223441daf03b349bb0314aa46d47a23f54d0567a11f`  
		Last Modified: Tue, 30 May 2023 22:27:05 GMT  
		Size: 315.7 MB (315742679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce71b52cd625e5982111700383dc98040f3b77c476e875a579f8b85171c5294b`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7e57af2d47a67fb3ef9b04dd913aace0981abe529272f6ae52c6477011313b`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840837a3c8c998309f1165b48b52995aee13097bcaf032cd199d85154233418a`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4666c0234210bc294a74c80d821e1ff3100c2f6fa88ea4feee53fdc3dd784e`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:6d2ce40a3f1c0f97ec87a3ce863b54cf161bd7a35133606f70da3271aaa43e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:9fa2ba18f412c9db7bb0662e8e2bf619f2ff087290a408fc75109759c5491707
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.5 MB (570475734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fe439d8cfc71750bbea1c6c2e64ac086ce3d8ccaa37c5f07a4122298d80d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:25:09 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 May 2023 04:25:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 May 2023 04:25:09 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 04:26:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 May 2023 04:26:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:26:56 GMT
RUN npm install -g rtlcss
# Tue, 23 May 2023 04:26:56 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 May 2023 22:21:27 GMT
ARG ODOO_RELEASE=20230530
# Tue, 30 May 2023 22:21:27 GMT
ARG ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
# Tue, 30 May 2023 22:23:04 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 May 2023 22:23:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 May 2023 22:23:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 May 2023 22:23:09 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 May 2023 22:23:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 May 2023 22:23:09 GMT
EXPOSE 8069 8071 8072
# Tue, 30 May 2023 22:23:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 May 2023 22:23:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 May 2023 22:23:10 GMT
USER odoo
# Tue, 30 May 2023 22:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 May 2023 22:23:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1e9686d13cba605592a655c33e96fc273869f0b8c2767aea698575f4a1b0f8`  
		Last Modified: Tue, 23 May 2023 04:34:21 GMT  
		Size: 220.3 MB (220298635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7e1c3238f65b74dbec3b8f1d37c83ba05c91cdc1519bc296572d0344d0bcc2`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 2.6 MB (2576158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28ae768ba0baf0ccb8a34bf4c776dfd95d57e763b4152c3bd0f4125ef41c0dc`  
		Last Modified: Tue, 23 May 2023 04:33:57 GMT  
		Size: 452.2 KB (452212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6150d95afe7d506a4c7223441daf03b349bb0314aa46d47a23f54d0567a11f`  
		Last Modified: Tue, 30 May 2023 22:27:05 GMT  
		Size: 315.7 MB (315742679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce71b52cd625e5982111700383dc98040f3b77c476e875a579f8b85171c5294b`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7e57af2d47a67fb3ef9b04dd913aace0981abe529272f6ae52c6477011313b`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840837a3c8c998309f1165b48b52995aee13097bcaf032cd199d85154233418a`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4666c0234210bc294a74c80d821e1ff3100c2f6fa88ea4feee53fdc3dd784e`  
		Last Modified: Tue, 30 May 2023 22:26:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
