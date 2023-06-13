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
$ docker pull odoo@sha256:0bd261c7b059f8ca6e449c1ae4217de1cc339d414007311903da26c22f72c005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:3019bc51bc9eccfa950d2f01d6d436503b6db032d97aabd272f860e3aba3218d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.5 MB (532483852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706bd585378342d7714c39d2cf24982991ad4309bb51b3318c82e9b5ab1dca95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:31:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Jun 2023 07:31:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Jun 2023 07:31:42 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 07:33:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Jun 2023 07:33:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:33:50 GMT
RUN npm install -g rtlcss
# Tue, 13 Jun 2023 07:33:50 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Jun 2023 07:33:50 GMT
ARG ODOO_RELEASE=20230530
# Tue, 13 Jun 2023 07:33:50 GMT
ARG ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
# Tue, 13 Jun 2023 07:35:15 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jun 2023 07:35:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Jun 2023 07:35:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jun 2023 07:35:19 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jun 2023 07:35:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jun 2023 07:35:20 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jun 2023 07:35:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jun 2023 07:35:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jun 2023 07:35:20 GMT
USER odoo
# Tue, 13 Jun 2023 07:35:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 07:35:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8b91b88d557765cd8c6802668755a3f6dc4337b6ce15a17e4857139e5fc964f3`  
		Last Modified: Mon, 12 Jun 2023 23:27:09 GMT  
		Size: 27.1 MB (27138450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e5002b5ea775e66bb8ed13a29d4cb4211ed8997ba6bdc303fd9a85fe503599`  
		Last Modified: Tue, 13 Jun 2023 07:37:35 GMT  
		Size: 213.2 MB (213199216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3b8791ab67afd61cac80a3091c7249ff248213ce957875bef3f0b1b1590263`  
		Last Modified: Tue, 13 Jun 2023 07:37:15 GMT  
		Size: 13.5 MB (13520946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9871a097e610176015bafb017a7f44fec2052f3d38de96814509597f53e2448`  
		Last Modified: Tue, 13 Jun 2023 07:37:12 GMT  
		Size: 458.8 KB (458750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb32724f5df8f3a71ef21c8f988c25f4a88cf7e38c058456b6b33cfb809c9e89`  
		Last Modified: Tue, 13 Jun 2023 07:37:42 GMT  
		Size: 278.2 MB (278164027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231b9e9039b48197e51badcd9c09fbdf904590630406c2912878c5a1e08adbaf`  
		Last Modified: Tue, 13 Jun 2023 07:37:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35f7cfcec0fc88156f31f2758a4718c8783d73e34684ef0e1695fdfe3cf7774`  
		Last Modified: Tue, 13 Jun 2023 07:37:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3d9d5bef2ea561d51d0ff13eb92eb4a4d3ea73a21986294ba853bc5bdf1ace`  
		Last Modified: Tue, 13 Jun 2023 07:37:10 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366db0a1bf900f1a904abaf29a0f8f858529ea6a5206eecfee15703076c3faa9`  
		Last Modified: Tue, 13 Jun 2023 07:37:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:0bd261c7b059f8ca6e449c1ae4217de1cc339d414007311903da26c22f72c005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:3019bc51bc9eccfa950d2f01d6d436503b6db032d97aabd272f860e3aba3218d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.5 MB (532483852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706bd585378342d7714c39d2cf24982991ad4309bb51b3318c82e9b5ab1dca95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:31:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Jun 2023 07:31:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Jun 2023 07:31:42 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 07:33:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Jun 2023 07:33:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:33:50 GMT
RUN npm install -g rtlcss
# Tue, 13 Jun 2023 07:33:50 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Jun 2023 07:33:50 GMT
ARG ODOO_RELEASE=20230530
# Tue, 13 Jun 2023 07:33:50 GMT
ARG ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
# Tue, 13 Jun 2023 07:35:15 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jun 2023 07:35:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Jun 2023 07:35:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jun 2023 07:35:19 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=307f5ebc95342d3114091fbe1d9d00ab684507c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jun 2023 07:35:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jun 2023 07:35:20 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jun 2023 07:35:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jun 2023 07:35:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jun 2023 07:35:20 GMT
USER odoo
# Tue, 13 Jun 2023 07:35:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 07:35:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8b91b88d557765cd8c6802668755a3f6dc4337b6ce15a17e4857139e5fc964f3`  
		Last Modified: Mon, 12 Jun 2023 23:27:09 GMT  
		Size: 27.1 MB (27138450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e5002b5ea775e66bb8ed13a29d4cb4211ed8997ba6bdc303fd9a85fe503599`  
		Last Modified: Tue, 13 Jun 2023 07:37:35 GMT  
		Size: 213.2 MB (213199216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3b8791ab67afd61cac80a3091c7249ff248213ce957875bef3f0b1b1590263`  
		Last Modified: Tue, 13 Jun 2023 07:37:15 GMT  
		Size: 13.5 MB (13520946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9871a097e610176015bafb017a7f44fec2052f3d38de96814509597f53e2448`  
		Last Modified: Tue, 13 Jun 2023 07:37:12 GMT  
		Size: 458.8 KB (458750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb32724f5df8f3a71ef21c8f988c25f4a88cf7e38c058456b6b33cfb809c9e89`  
		Last Modified: Tue, 13 Jun 2023 07:37:42 GMT  
		Size: 278.2 MB (278164027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231b9e9039b48197e51badcd9c09fbdf904590630406c2912878c5a1e08adbaf`  
		Last Modified: Tue, 13 Jun 2023 07:37:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35f7cfcec0fc88156f31f2758a4718c8783d73e34684ef0e1695fdfe3cf7774`  
		Last Modified: Tue, 13 Jun 2023 07:37:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3d9d5bef2ea561d51d0ff13eb92eb4a4d3ea73a21986294ba853bc5bdf1ace`  
		Last Modified: Tue, 13 Jun 2023 07:37:10 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366db0a1bf900f1a904abaf29a0f8f858529ea6a5206eecfee15703076c3faa9`  
		Last Modified: Tue, 13 Jun 2023 07:37:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:7fd140361d0b42e0c136a03ac5d0ef3f9ee7d2b8cda393f1628577b34f2c8145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:6212f74133ca89f529c4df1947e0a606d8fae83ccb26b2debf8a42881f42f3a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.0 MB (561036256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277a4f0dfe3f39f14b51ba9761250404983c5a379de03e0f8c7669bcf5bd0af5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:26:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Jun 2023 07:26:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Jun 2023 07:26:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 07:28:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Jun 2023 07:28:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:28:38 GMT
RUN npm install -g rtlcss
# Tue, 13 Jun 2023 07:30:19 GMT
ENV ODOO_VERSION=15.0
# Tue, 13 Jun 2023 07:30:19 GMT
ARG ODOO_RELEASE=20230530
# Tue, 13 Jun 2023 07:30:19 GMT
ARG ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
# Tue, 13 Jun 2023 07:31:30 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jun 2023 07:31:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Jun 2023 07:31:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jun 2023 07:31:35 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jun 2023 07:31:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jun 2023 07:31:35 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jun 2023 07:31:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jun 2023 07:31:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jun 2023 07:31:36 GMT
USER odoo
# Tue, 13 Jun 2023 07:31:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 07:31:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd64d7ca73c2e93c76513d56030613b9b9cf0e27efdb3a253d1591507005e0cd`  
		Last Modified: Tue, 13 Jun 2023 07:36:08 GMT  
		Size: 220.3 MB (220302623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e8b4bd092ea25a9ae903dc284787bd0503e212e6d227300943cb1f2e8fe9b`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 2.6 MB (2576153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c886eafab424bce7b46782d3222cd1432beb940d583b9b559df7de7dfc41943`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 454.3 KB (454307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d2b4d1b2cdfdc88fa5e390efad3fd0cd5914c57b59079cc3815df4206e41c4`  
		Last Modified: Tue, 13 Jun 2023 07:37:02 GMT  
		Size: 306.3 MB (306283299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a795401e24fb5df533201f3f0d5569a6b77cbb5acb51619f1ca0f2a42c0bc890`  
		Last Modified: Tue, 13 Jun 2023 07:36:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac55854886732e9194577386cfd003932333a3b993c164de7f8ab7322ff1ed`  
		Last Modified: Tue, 13 Jun 2023 07:36:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3f70261d6a0cc2ec20dfcb011a4c8da20c4c044dd515097b095ff8ad50abef`  
		Last Modified: Tue, 13 Jun 2023 07:36:29 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9412bd586c756bdf3b162f823efa80286bbaafce590083dba3118690af3ac0`  
		Last Modified: Tue, 13 Jun 2023 07:36:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:7fd140361d0b42e0c136a03ac5d0ef3f9ee7d2b8cda393f1628577b34f2c8145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:6212f74133ca89f529c4df1947e0a606d8fae83ccb26b2debf8a42881f42f3a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.0 MB (561036256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277a4f0dfe3f39f14b51ba9761250404983c5a379de03e0f8c7669bcf5bd0af5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:26:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Jun 2023 07:26:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Jun 2023 07:26:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 07:28:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Jun 2023 07:28:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:28:38 GMT
RUN npm install -g rtlcss
# Tue, 13 Jun 2023 07:30:19 GMT
ENV ODOO_VERSION=15.0
# Tue, 13 Jun 2023 07:30:19 GMT
ARG ODOO_RELEASE=20230530
# Tue, 13 Jun 2023 07:30:19 GMT
ARG ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
# Tue, 13 Jun 2023 07:31:30 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jun 2023 07:31:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Jun 2023 07:31:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jun 2023 07:31:35 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=b7017cc3f757c1ecb1545f784c558ef5c0387030
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jun 2023 07:31:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jun 2023 07:31:35 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jun 2023 07:31:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jun 2023 07:31:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jun 2023 07:31:36 GMT
USER odoo
# Tue, 13 Jun 2023 07:31:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 07:31:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd64d7ca73c2e93c76513d56030613b9b9cf0e27efdb3a253d1591507005e0cd`  
		Last Modified: Tue, 13 Jun 2023 07:36:08 GMT  
		Size: 220.3 MB (220302623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e8b4bd092ea25a9ae903dc284787bd0503e212e6d227300943cb1f2e8fe9b`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 2.6 MB (2576153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c886eafab424bce7b46782d3222cd1432beb940d583b9b559df7de7dfc41943`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 454.3 KB (454307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d2b4d1b2cdfdc88fa5e390efad3fd0cd5914c57b59079cc3815df4206e41c4`  
		Last Modified: Tue, 13 Jun 2023 07:37:02 GMT  
		Size: 306.3 MB (306283299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a795401e24fb5df533201f3f0d5569a6b77cbb5acb51619f1ca0f2a42c0bc890`  
		Last Modified: Tue, 13 Jun 2023 07:36:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac55854886732e9194577386cfd003932333a3b993c164de7f8ab7322ff1ed`  
		Last Modified: Tue, 13 Jun 2023 07:36:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3f70261d6a0cc2ec20dfcb011a4c8da20c4c044dd515097b095ff8ad50abef`  
		Last Modified: Tue, 13 Jun 2023 07:36:29 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9412bd586c756bdf3b162f823efa80286bbaafce590083dba3118690af3ac0`  
		Last Modified: Tue, 13 Jun 2023 07:36:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:51bf4b1f20e92ba0a13567f7dcaa5a90f72ca2f6ceaeece005277658a1cf224e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:7c0ec57ab99163c7e7e2f7689e4d11f1d717b44a1365af40d987fe601793c363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.5 MB (570497048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8da56afcd0a73fbe0aaae2097094b608b190544b6e47e11d08bec20023d25d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:26:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Jun 2023 07:26:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Jun 2023 07:26:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 07:28:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Jun 2023 07:28:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:28:38 GMT
RUN npm install -g rtlcss
# Tue, 13 Jun 2023 07:28:38 GMT
ENV ODOO_VERSION=16.0
# Tue, 13 Jun 2023 07:28:38 GMT
ARG ODOO_RELEASE=20230530
# Tue, 13 Jun 2023 07:28:38 GMT
ARG ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
# Tue, 13 Jun 2023 07:30:10 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jun 2023 07:30:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Jun 2023 07:30:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jun 2023 07:30:15 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jun 2023 07:30:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jun 2023 07:30:16 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jun 2023 07:30:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jun 2023 07:30:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jun 2023 07:30:16 GMT
USER odoo
# Tue, 13 Jun 2023 07:30:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 07:30:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd64d7ca73c2e93c76513d56030613b9b9cf0e27efdb3a253d1591507005e0cd`  
		Last Modified: Tue, 13 Jun 2023 07:36:08 GMT  
		Size: 220.3 MB (220302623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e8b4bd092ea25a9ae903dc284787bd0503e212e6d227300943cb1f2e8fe9b`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 2.6 MB (2576153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c886eafab424bce7b46782d3222cd1432beb940d583b9b559df7de7dfc41943`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 454.3 KB (454307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6402790c2b3280dc0a9bf2bbb0e816eaede5387bbdbf110fb35b42825dd2de1`  
		Last Modified: Tue, 13 Jun 2023 07:36:18 GMT  
		Size: 315.7 MB (315744099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b553b4af84e37a16e68e972d85f4be96276226f301987aab7c6336220c04314e`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff46e30e82119d54e6b6dec509b78dcc6d8cc2d3c7848d6c5f8f31afd05e45e`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa91477b38c828e4796a3a6d387e62ab051629c86fa2c511b76d197e717f297e`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103bfe9e2b4527d7ee7f81e467757ba8dd8828c0a7880251c96a8eda2cf5402`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:51bf4b1f20e92ba0a13567f7dcaa5a90f72ca2f6ceaeece005277658a1cf224e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:7c0ec57ab99163c7e7e2f7689e4d11f1d717b44a1365af40d987fe601793c363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.5 MB (570497048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8da56afcd0a73fbe0aaae2097094b608b190544b6e47e11d08bec20023d25d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:26:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Jun 2023 07:26:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Jun 2023 07:26:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 07:28:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Jun 2023 07:28:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:28:38 GMT
RUN npm install -g rtlcss
# Tue, 13 Jun 2023 07:28:38 GMT
ENV ODOO_VERSION=16.0
# Tue, 13 Jun 2023 07:28:38 GMT
ARG ODOO_RELEASE=20230530
# Tue, 13 Jun 2023 07:28:38 GMT
ARG ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
# Tue, 13 Jun 2023 07:30:10 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jun 2023 07:30:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Jun 2023 07:30:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jun 2023 07:30:15 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jun 2023 07:30:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jun 2023 07:30:16 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jun 2023 07:30:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jun 2023 07:30:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jun 2023 07:30:16 GMT
USER odoo
# Tue, 13 Jun 2023 07:30:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 07:30:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd64d7ca73c2e93c76513d56030613b9b9cf0e27efdb3a253d1591507005e0cd`  
		Last Modified: Tue, 13 Jun 2023 07:36:08 GMT  
		Size: 220.3 MB (220302623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e8b4bd092ea25a9ae903dc284787bd0503e212e6d227300943cb1f2e8fe9b`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 2.6 MB (2576153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c886eafab424bce7b46782d3222cd1432beb940d583b9b559df7de7dfc41943`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 454.3 KB (454307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6402790c2b3280dc0a9bf2bbb0e816eaede5387bbdbf110fb35b42825dd2de1`  
		Last Modified: Tue, 13 Jun 2023 07:36:18 GMT  
		Size: 315.7 MB (315744099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b553b4af84e37a16e68e972d85f4be96276226f301987aab7c6336220c04314e`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff46e30e82119d54e6b6dec509b78dcc6d8cc2d3c7848d6c5f8f31afd05e45e`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa91477b38c828e4796a3a6d387e62ab051629c86fa2c511b76d197e717f297e`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103bfe9e2b4527d7ee7f81e467757ba8dd8828c0a7880251c96a8eda2cf5402`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:51bf4b1f20e92ba0a13567f7dcaa5a90f72ca2f6ceaeece005277658a1cf224e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:7c0ec57ab99163c7e7e2f7689e4d11f1d717b44a1365af40d987fe601793c363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.5 MB (570497048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8da56afcd0a73fbe0aaae2097094b608b190544b6e47e11d08bec20023d25d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:26:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Jun 2023 07:26:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Jun 2023 07:26:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 07:28:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Jun 2023 07:28:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:28:38 GMT
RUN npm install -g rtlcss
# Tue, 13 Jun 2023 07:28:38 GMT
ENV ODOO_VERSION=16.0
# Tue, 13 Jun 2023 07:28:38 GMT
ARG ODOO_RELEASE=20230530
# Tue, 13 Jun 2023 07:28:38 GMT
ARG ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
# Tue, 13 Jun 2023 07:30:10 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jun 2023 07:30:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Jun 2023 07:30:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jun 2023 07:30:15 GMT
# ARGS: ODOO_RELEASE=20230530 ODOO_SHA=e7ddf8de9873c66ef887c5bf23b3698673a1ba35
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jun 2023 07:30:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jun 2023 07:30:16 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jun 2023 07:30:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jun 2023 07:30:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jun 2023 07:30:16 GMT
USER odoo
# Tue, 13 Jun 2023 07:30:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 07:30:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd64d7ca73c2e93c76513d56030613b9b9cf0e27efdb3a253d1591507005e0cd`  
		Last Modified: Tue, 13 Jun 2023 07:36:08 GMT  
		Size: 220.3 MB (220302623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e8b4bd092ea25a9ae903dc284787bd0503e212e6d227300943cb1f2e8fe9b`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 2.6 MB (2576153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c886eafab424bce7b46782d3222cd1432beb940d583b9b559df7de7dfc41943`  
		Last Modified: Tue, 13 Jun 2023 07:35:44 GMT  
		Size: 454.3 KB (454307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6402790c2b3280dc0a9bf2bbb0e816eaede5387bbdbf110fb35b42825dd2de1`  
		Last Modified: Tue, 13 Jun 2023 07:36:18 GMT  
		Size: 315.7 MB (315744099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b553b4af84e37a16e68e972d85f4be96276226f301987aab7c6336220c04314e`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff46e30e82119d54e6b6dec509b78dcc6d8cc2d3c7848d6c5f8f31afd05e45e`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa91477b38c828e4796a3a6d387e62ab051629c86fa2c511b76d197e717f297e`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103bfe9e2b4527d7ee7f81e467757ba8dd8828c0a7880251c96a8eda2cf5402`  
		Last Modified: Tue, 13 Jun 2023 07:35:42 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
