<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:ae526e1779a736591e9e7ca31ab177e6c7ce490c17e3ffa9c195ed67ed69ae3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:4ee87c2bff891c957437081509f8edd79cc1142a244f267a8858c3655e01b774
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563043964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7974f41b128ec05dcd506cd6857cf30539bad87918f14bab190edb92fe30bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 06:06:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 06:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 06:09:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 06:10:06 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:07 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 06:10:07 GMT
ENV ODOO_VERSION=15.0
# Tue, 28 Nov 2023 23:37:59 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:37:59 GMT
ARG ODOO_SHA=c0e91e4d03ffa8a72db550389f33b7c3577fa829
# Tue, 28 Nov 2023 23:39:10 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=c0e91e4d03ffa8a72db550389f33b7c3577fa829
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:39:14 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:39:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:39:15 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=c0e91e4d03ffa8a72db550389f33b7c3577fa829
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:39:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:39:15 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:39:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:39:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:39:15 GMT
USER odoo
# Tue, 28 Nov 2023 23:39:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:39:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a28800da8ad810dcb3060b9a249d76f10fc059eb9ea15aa7bb1fcfd0755b607`  
		Last Modified: Tue, 21 Nov 2023 06:13:44 GMT  
		Size: 220.3 MB (220297479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd5e822cfaa6f1e0ff1254d563b0f9fae55e9a37a6461f685b61ba68642687e`  
		Last Modified: Tue, 21 Nov 2023 06:13:20 GMT  
		Size: 2.6 MB (2625685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c2fe85ca0f057eeac7b5d2f65043d55dd0192357c143eca092e3fcdb6f1826`  
		Last Modified: Tue, 21 Nov 2023 06:13:20 GMT  
		Size: 459.5 KB (459485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2d62dc7a84225d80e241450ca7f1c3c8352369bab05d6ab9503a472caf32ba`  
		Last Modified: Tue, 28 Nov 2023 23:41:43 GMT  
		Size: 308.2 MB (308241022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc53506b74d5f16bfb8f2f9818f90fcf74f7382e5634f9c6b84990564363a44a`  
		Last Modified: Tue, 28 Nov 2023 23:41:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84884fc611d342bb1c81fdac836a35499c4a8916b6fb07a0104559fff4724586`  
		Last Modified: Tue, 28 Nov 2023 23:41:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee7833223295aa1607a3c5007b9ed6c45822b87a6378964d67c3239943d141`  
		Last Modified: Tue, 28 Nov 2023 23:41:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5afe1ec8c776632dce8a00e55efcbfd0b25bd07093b6dc81802688e197ac2a`  
		Last Modified: Tue, 28 Nov 2023 23:41:10 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:ae526e1779a736591e9e7ca31ab177e6c7ce490c17e3ffa9c195ed67ed69ae3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:4ee87c2bff891c957437081509f8edd79cc1142a244f267a8858c3655e01b774
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563043964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7974f41b128ec05dcd506cd6857cf30539bad87918f14bab190edb92fe30bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 06:06:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 06:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 06:09:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 06:10:06 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:07 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 06:10:07 GMT
ENV ODOO_VERSION=15.0
# Tue, 28 Nov 2023 23:37:59 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:37:59 GMT
ARG ODOO_SHA=c0e91e4d03ffa8a72db550389f33b7c3577fa829
# Tue, 28 Nov 2023 23:39:10 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=c0e91e4d03ffa8a72db550389f33b7c3577fa829
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:39:14 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:39:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:39:15 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=c0e91e4d03ffa8a72db550389f33b7c3577fa829
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:39:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:39:15 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:39:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:39:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:39:15 GMT
USER odoo
# Tue, 28 Nov 2023 23:39:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:39:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a28800da8ad810dcb3060b9a249d76f10fc059eb9ea15aa7bb1fcfd0755b607`  
		Last Modified: Tue, 21 Nov 2023 06:13:44 GMT  
		Size: 220.3 MB (220297479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd5e822cfaa6f1e0ff1254d563b0f9fae55e9a37a6461f685b61ba68642687e`  
		Last Modified: Tue, 21 Nov 2023 06:13:20 GMT  
		Size: 2.6 MB (2625685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c2fe85ca0f057eeac7b5d2f65043d55dd0192357c143eca092e3fcdb6f1826`  
		Last Modified: Tue, 21 Nov 2023 06:13:20 GMT  
		Size: 459.5 KB (459485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2d62dc7a84225d80e241450ca7f1c3c8352369bab05d6ab9503a472caf32ba`  
		Last Modified: Tue, 28 Nov 2023 23:41:43 GMT  
		Size: 308.2 MB (308241022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc53506b74d5f16bfb8f2f9818f90fcf74f7382e5634f9c6b84990564363a44a`  
		Last Modified: Tue, 28 Nov 2023 23:41:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84884fc611d342bb1c81fdac836a35499c4a8916b6fb07a0104559fff4724586`  
		Last Modified: Tue, 28 Nov 2023 23:41:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee7833223295aa1607a3c5007b9ed6c45822b87a6378964d67c3239943d141`  
		Last Modified: Tue, 28 Nov 2023 23:41:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5afe1ec8c776632dce8a00e55efcbfd0b25bd07093b6dc81802688e197ac2a`  
		Last Modified: Tue, 28 Nov 2023 23:41:10 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:4c089245a26ad3db9297c3dcf6d586971ee2c1c3c2f4efac3c256f24f5c4303b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:b5d39be042bf07b6f15bd12211cf4bcf217823636792cf6c459bfeab3746f36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.3 MB (577299005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7d957b83fff0620627dbe7fa94700876bce0bc3c5db97f728a6f6642782803`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 06:06:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 06:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 06:06:00 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 06:07:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 06:07:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:07:25 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 06:07:25 GMT
ENV ODOO_VERSION=16.0
# Tue, 28 Nov 2023 23:36:20 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:36:20 GMT
ARG ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
# Tue, 28 Nov 2023 23:37:40 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:37:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:37:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:37:45 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:37:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:37:45 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:37:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:37:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:37:46 GMT
USER odoo
# Tue, 28 Nov 2023 23:37:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:37:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66dcf73708692fc6d6dee7d004e9c2f7d2fb47f905fbbc62dc61f2daffceb17`  
		Last Modified: Tue, 21 Nov 2023 06:12:58 GMT  
		Size: 219.6 MB (219606563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f096532668b80e067c70ebffa93b9ba9b5efa7080f7cf42b36ccb58a90e3508`  
		Last Modified: Tue, 21 Nov 2023 06:12:34 GMT  
		Size: 2.6 MB (2629834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ce0ca6176cbb017ef1b39cc6364b8f0620ac11996f8f6f959fb01195040a7b`  
		Last Modified: Tue, 21 Nov 2023 06:12:33 GMT  
		Size: 459.5 KB (459472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2802c5ce230e9ccea7da615906364d23deb330209c9e73afcfd021c25c167bf6`  
		Last Modified: Tue, 28 Nov 2023 23:41:00 GMT  
		Size: 323.2 MB (323182849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d03116eb0dc8e1cc72568d9efd2224eb5d8dc0438b9bfc33a07675786f289a`  
		Last Modified: Tue, 28 Nov 2023 23:40:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121a4fca1aeb8664f35503052bb16ba656c3ca322aa944e75a400338c3033ff0`  
		Last Modified: Tue, 28 Nov 2023 23:40:24 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d93a81fba2a56b164c488d207177b6979414161f55dc7d8b05961c3ec5cce2`  
		Last Modified: Tue, 28 Nov 2023 23:40:24 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc9dffbaf1db9065dad5aeab3ff57d7b3b98dc81977e19d2c33c10c1abc1656`  
		Last Modified: Tue, 28 Nov 2023 23:40:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:11ee49f510f40f61a7be75b8221bcde84320ca5d1d2ca943f6010e8ee95e7dc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.9 MB (572915587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6a83d4d02d85f700a89b5af7b2084c26585d6b1d6214974937f028ab33304e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:24:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 10:24:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 10:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 10:24:03 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 10:25:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 10:25:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:25:16 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 10:25:16 GMT
ENV ODOO_VERSION=16.0
# Tue, 28 Nov 2023 23:56:35 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:56:35 GMT
ARG ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
# Tue, 28 Nov 2023 23:57:50 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:57:57 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:57:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:57:57 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:57:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:57:58 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:57:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:57:58 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:57:58 GMT
USER odoo
# Tue, 28 Nov 2023 23:57:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:57:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ab9b0a137551e75078132a976e9e490b4eb1fc07fe87beb915c8f0be0988b`  
		Last Modified: Tue, 21 Nov 2023 10:27:07 GMT  
		Size: 216.9 MB (216908243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451f82e1e1d62729c32c647a135084aeea39e2eecdfab5f468e549adbe642a1`  
		Last Modified: Tue, 21 Nov 2023 10:26:50 GMT  
		Size: 2.6 MB (2634860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006d5b0160b4770a0c5d2bbe136fec01bf9daa283a549aceba5449dcc1b0eb7a`  
		Last Modified: Tue, 21 Nov 2023 10:26:49 GMT  
		Size: 459.5 KB (459492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cbb6e4cc780b8d58b6d67601ffc48c6c4d735b3b63feb3346da17b1e501863`  
		Last Modified: Tue, 28 Nov 2023 23:59:40 GMT  
		Size: 322.8 MB (322846403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa67c5dad3ca8eee6dc993708f0d4bfeb1969a20ab795c6b629ce2b6ec4f246`  
		Last Modified: Tue, 28 Nov 2023 23:59:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f1e168b52fab7401e5ab018f68f464cc34a16afcc79b3f826b8246ccbc4472`  
		Last Modified: Tue, 28 Nov 2023 23:59:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724cd6c49ffcff2bfeb098705d2aec6309c18426a70214bbae7ca177fbb6dfbf`  
		Last Modified: Tue, 28 Nov 2023 23:59:11 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf0c643f2e1b6270c09939dfe5d7fc1b03f7b456e72043b01ae81a56655aa94`  
		Last Modified: Tue, 28 Nov 2023 23:59:11 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:88121765b1a6469f8f0fe6d29d9e7bc24e2242bc751fa1b1f2255dd3b7a57506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591838095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c895fc081d72d2e1ebac2cdf92b23359f4bd0fbebb9c06e512da1f8be9300f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:37:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 04:37:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 04:37:34 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 04:37:34 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 04:40:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 04:40:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 04:40:39 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 04:40:39 GMT
ENV ODOO_VERSION=16.0
# Tue, 28 Nov 2023 23:25:53 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:25:54 GMT
ARG ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
# Tue, 28 Nov 2023 23:28:09 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:28:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:28:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:28:29 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:28:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:28:30 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:28:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:28:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:28:31 GMT
USER odoo
# Tue, 28 Nov 2023 23:28:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:28:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9412e97f56973d23e9dad0c3fcfd85b2446ed64817cf494fd8c0d7e8a361d2b6`  
		Last Modified: Tue, 21 Nov 2023 04:44:49 GMT  
		Size: 228.6 MB (228598187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a33d7cd62e6b8c2d2d1f1384daa821c3fbc171b6a3fb9296592372045d33751`  
		Last Modified: Tue, 21 Nov 2023 04:44:20 GMT  
		Size: 2.9 MB (2875641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d656925877eaa583e8f5dde6fd482750adc09d25cdd8ac87e6345c0b308d1b97`  
		Last Modified: Tue, 21 Nov 2023 04:44:19 GMT  
		Size: 459.5 KB (459505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1bb8e020e98e71023b53e75057a7a2f00d8f9061aedba34eea06d135af55ed`  
		Last Modified: Tue, 28 Nov 2023 23:30:38 GMT  
		Size: 324.6 MB (324608574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab63dc7971c6de9f051218064e755d018d356be99c2e24223a1b75783cc4bd1`  
		Last Modified: Tue, 28 Nov 2023 23:29:54 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a69ff9a7a00031ee77d8f16b56e22dc03cd35f02202510cf1505d22f515306d`  
		Last Modified: Tue, 28 Nov 2023 23:29:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c182ff19ecce1588d7b08e32948a679b77bf6b7cc202f4f5218132d4469c3224`  
		Last Modified: Tue, 28 Nov 2023 23:29:54 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3658e9bbbd117fd6c48ab7c076c4fef6a53b2bfcccaaa2ebe37e0510dc0134c7`  
		Last Modified: Tue, 28 Nov 2023 23:29:54 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:4c089245a26ad3db9297c3dcf6d586971ee2c1c3c2f4efac3c256f24f5c4303b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:b5d39be042bf07b6f15bd12211cf4bcf217823636792cf6c459bfeab3746f36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.3 MB (577299005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7d957b83fff0620627dbe7fa94700876bce0bc3c5db97f728a6f6642782803`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 06:06:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 06:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 06:06:00 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 06:07:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 06:07:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:07:25 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 06:07:25 GMT
ENV ODOO_VERSION=16.0
# Tue, 28 Nov 2023 23:36:20 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:36:20 GMT
ARG ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
# Tue, 28 Nov 2023 23:37:40 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:37:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:37:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:37:45 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:37:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:37:45 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:37:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:37:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:37:46 GMT
USER odoo
# Tue, 28 Nov 2023 23:37:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:37:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66dcf73708692fc6d6dee7d004e9c2f7d2fb47f905fbbc62dc61f2daffceb17`  
		Last Modified: Tue, 21 Nov 2023 06:12:58 GMT  
		Size: 219.6 MB (219606563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f096532668b80e067c70ebffa93b9ba9b5efa7080f7cf42b36ccb58a90e3508`  
		Last Modified: Tue, 21 Nov 2023 06:12:34 GMT  
		Size: 2.6 MB (2629834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ce0ca6176cbb017ef1b39cc6364b8f0620ac11996f8f6f959fb01195040a7b`  
		Last Modified: Tue, 21 Nov 2023 06:12:33 GMT  
		Size: 459.5 KB (459472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2802c5ce230e9ccea7da615906364d23deb330209c9e73afcfd021c25c167bf6`  
		Last Modified: Tue, 28 Nov 2023 23:41:00 GMT  
		Size: 323.2 MB (323182849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d03116eb0dc8e1cc72568d9efd2224eb5d8dc0438b9bfc33a07675786f289a`  
		Last Modified: Tue, 28 Nov 2023 23:40:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121a4fca1aeb8664f35503052bb16ba656c3ca322aa944e75a400338c3033ff0`  
		Last Modified: Tue, 28 Nov 2023 23:40:24 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d93a81fba2a56b164c488d207177b6979414161f55dc7d8b05961c3ec5cce2`  
		Last Modified: Tue, 28 Nov 2023 23:40:24 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc9dffbaf1db9065dad5aeab3ff57d7b3b98dc81977e19d2c33c10c1abc1656`  
		Last Modified: Tue, 28 Nov 2023 23:40:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:11ee49f510f40f61a7be75b8221bcde84320ca5d1d2ca943f6010e8ee95e7dc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.9 MB (572915587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6a83d4d02d85f700a89b5af7b2084c26585d6b1d6214974937f028ab33304e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:24:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 10:24:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 10:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 10:24:03 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 10:25:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 10:25:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:25:16 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 10:25:16 GMT
ENV ODOO_VERSION=16.0
# Tue, 28 Nov 2023 23:56:35 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:56:35 GMT
ARG ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
# Tue, 28 Nov 2023 23:57:50 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:57:57 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:57:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:57:57 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:57:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:57:58 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:57:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:57:58 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:57:58 GMT
USER odoo
# Tue, 28 Nov 2023 23:57:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:57:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ab9b0a137551e75078132a976e9e490b4eb1fc07fe87beb915c8f0be0988b`  
		Last Modified: Tue, 21 Nov 2023 10:27:07 GMT  
		Size: 216.9 MB (216908243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451f82e1e1d62729c32c647a135084aeea39e2eecdfab5f468e549adbe642a1`  
		Last Modified: Tue, 21 Nov 2023 10:26:50 GMT  
		Size: 2.6 MB (2634860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006d5b0160b4770a0c5d2bbe136fec01bf9daa283a549aceba5449dcc1b0eb7a`  
		Last Modified: Tue, 21 Nov 2023 10:26:49 GMT  
		Size: 459.5 KB (459492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cbb6e4cc780b8d58b6d67601ffc48c6c4d735b3b63feb3346da17b1e501863`  
		Last Modified: Tue, 28 Nov 2023 23:59:40 GMT  
		Size: 322.8 MB (322846403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa67c5dad3ca8eee6dc993708f0d4bfeb1969a20ab795c6b629ce2b6ec4f246`  
		Last Modified: Tue, 28 Nov 2023 23:59:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f1e168b52fab7401e5ab018f68f464cc34a16afcc79b3f826b8246ccbc4472`  
		Last Modified: Tue, 28 Nov 2023 23:59:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724cd6c49ffcff2bfeb098705d2aec6309c18426a70214bbae7ca177fbb6dfbf`  
		Last Modified: Tue, 28 Nov 2023 23:59:11 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf0c643f2e1b6270c09939dfe5d7fc1b03f7b456e72043b01ae81a56655aa94`  
		Last Modified: Tue, 28 Nov 2023 23:59:11 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:88121765b1a6469f8f0fe6d29d9e7bc24e2242bc751fa1b1f2255dd3b7a57506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591838095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c895fc081d72d2e1ebac2cdf92b23359f4bd0fbebb9c06e512da1f8be9300f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:37:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 04:37:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 04:37:34 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 04:37:34 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 04:40:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 04:40:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 04:40:39 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 04:40:39 GMT
ENV ODOO_VERSION=16.0
# Tue, 28 Nov 2023 23:25:53 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:25:54 GMT
ARG ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
# Tue, 28 Nov 2023 23:28:09 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:28:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:28:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:28:29 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=cf3fe2729f489476b5a07411a647667ed21e5208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:28:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:28:30 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:28:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:28:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:28:31 GMT
USER odoo
# Tue, 28 Nov 2023 23:28:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:28:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9412e97f56973d23e9dad0c3fcfd85b2446ed64817cf494fd8c0d7e8a361d2b6`  
		Last Modified: Tue, 21 Nov 2023 04:44:49 GMT  
		Size: 228.6 MB (228598187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a33d7cd62e6b8c2d2d1f1384daa821c3fbc171b6a3fb9296592372045d33751`  
		Last Modified: Tue, 21 Nov 2023 04:44:20 GMT  
		Size: 2.9 MB (2875641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d656925877eaa583e8f5dde6fd482750adc09d25cdd8ac87e6345c0b308d1b97`  
		Last Modified: Tue, 21 Nov 2023 04:44:19 GMT  
		Size: 459.5 KB (459505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1bb8e020e98e71023b53e75057a7a2f00d8f9061aedba34eea06d135af55ed`  
		Last Modified: Tue, 28 Nov 2023 23:30:38 GMT  
		Size: 324.6 MB (324608574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab63dc7971c6de9f051218064e755d018d356be99c2e24223a1b75783cc4bd1`  
		Last Modified: Tue, 28 Nov 2023 23:29:54 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a69ff9a7a00031ee77d8f16b56e22dc03cd35f02202510cf1505d22f515306d`  
		Last Modified: Tue, 28 Nov 2023 23:29:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c182ff19ecce1588d7b08e32948a679b77bf6b7cc202f4f5218132d4469c3224`  
		Last Modified: Tue, 28 Nov 2023 23:29:54 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3658e9bbbd117fd6c48ab7c076c4fef6a53b2bfcccaaa2ebe37e0510dc0134c7`  
		Last Modified: Tue, 28 Nov 2023 23:29:54 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:7439fb83eef6aa53adea0998f3bec22d666b122675c2c9c9aeaa3bf5aa5bf8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:140fa657977b1b605390bdf7aca64ebf8937567124600631e20751fc7aca9f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595444044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb591a7d8a95c271d1bbdfdbcfade49852ff05eebeaf067f803981f84e9b813`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:38:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:38:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:38:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:38:22 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:40:32 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:43:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:43:14 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:43:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 28 Nov 2023 23:33:56 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:33:57 GMT
ARG ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
# Tue, 28 Nov 2023 23:36:01 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:36:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:36:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:36:06 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:36:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:36:06 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:36:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:36:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:36:07 GMT
USER odoo
# Tue, 28 Nov 2023 23:36:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:36:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb3c31d88935a4bd21fe72cde4d10cf70f938ed370d1589f5afe78de8e9d5ef`  
		Last Modified: Tue, 14 Nov 2023 01:48:55 GMT  
		Size: 236.0 MB (236000929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635e6cd9216147592a4196f3bd6dbd96074a19264c7ec0d1ebca064d6810ba5`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 2.5 MB (2526404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ce7265beed021294fe7c29a3a1bc47a0ccdcda030d1d53cbc088171441d3a8`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 460.6 KB (460559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b808267e127a9bc3a9b1135627ed168cdcd2ef4867af1c0694215f69b77bca35`  
		Last Modified: Tue, 28 Nov 2023 23:40:09 GMT  
		Size: 326.0 MB (326014578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd43828d3e4181c5fe4cb52c8f0954ddceb4742ec62c4b2bb944ba295cc2aacb`  
		Last Modified: Tue, 28 Nov 2023 23:39:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fcfbf8eff75ad676f2ee47d277dd4f479647601c84311c07a330865daeb1ea`  
		Last Modified: Tue, 28 Nov 2023 23:39:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22adacf81d7ff9cc0c80d0ce4079ef286aa0c0442a3a2ada1de88fda96ee3b27`  
		Last Modified: Tue, 28 Nov 2023 23:39:34 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a0d6c51629ddcb1c78a795f95cd6c71a389a79c72ca3140b46be7c2e4136c0`  
		Last Modified: Tue, 28 Nov 2023 23:39:34 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b3f5f7a6363f8d7e2ca4ff4ca1ebecd991a63f7a7013b153190a11492509de53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590250868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae54c73ecd0eecfbcb59d1cf5abcd0f11c820cb9a31b4ebae13788959d75716f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 28 Nov 2023 23:53:57 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:53:57 GMT
ARG ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
# Tue, 28 Nov 2023 23:56:18 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:56:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:56:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:56:20 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:56:20 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:56:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:56:20 GMT
USER odoo
# Tue, 28 Nov 2023 23:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fde2c83350915390e5e17a879bb997a0f7c2212281f6478832ef6aad828eaa`  
		Last Modified: Tue, 28 Nov 2023 23:59:00 GMT  
		Size: 325.6 MB (325630264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6ecfd1db0d2d7758f1743e0ed6a77a641eab6586eb06bb85c0ad8f77d56399`  
		Last Modified: Tue, 28 Nov 2023 23:58:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d255c6bfabf2d531ce1d85a5d35aeeaf6a0a7967274beab93b7aa14e8f05896`  
		Last Modified: Tue, 28 Nov 2023 23:58:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d33f30c52751e59f692a7e04bf14cf04297d32369def4640b9f92f9072af39a`  
		Last Modified: Tue, 28 Nov 2023 23:58:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526901d9ecf6ec4d566232d762c9d143016ac3e8f84602fe4dd3d94808d8843e`  
		Last Modified: Tue, 28 Nov 2023 23:58:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:10f2922ae979454dd42053e96e0f52ea0d906e83710e6913fef63c3914fdc569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.6 MB (612642323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9a90adaee26cf87570a41430b18a35495f307571907ed430d249448ad5a4b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:16:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:16:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:16:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:16:49 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:21:28 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:21:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:21:53 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:21:54 GMT
ENV ODOO_VERSION=17.0
# Tue, 28 Nov 2023 23:22:14 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:22:14 GMT
ARG ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
# Tue, 28 Nov 2023 23:25:22 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:25:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:25:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:25:36 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:25:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:25:37 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:25:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:25:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:25:38 GMT
USER odoo
# Tue, 28 Nov 2023 23:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:25:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff961ccf5729ac1f3c5d8b7806dd42fa9a9fbc4083f43b7d5bc3b9bbc166edbd`  
		Last Modified: Tue, 14 Nov 2023 01:28:59 GMT  
		Size: 245.9 MB (245927069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6d3d2526a589659b9a531e4540bfd3bd343c49e9845f1409f5d7b12f7cca3`  
		Last Modified: Tue, 14 Nov 2023 01:28:17 GMT  
		Size: 2.8 MB (2803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bc659a5b58234fbb32ee9ced616e815875a88f93489359a4f37bacad64bf54`  
		Last Modified: Tue, 14 Nov 2023 01:28:16 GMT  
		Size: 460.5 KB (460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d497e129cef421d59b66a9057c8ad17dcc2d672a65dbb639971d5346c5196`  
		Last Modified: Tue, 28 Nov 2023 23:29:42 GMT  
		Size: 327.8 MB (327766255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b7b923ce44552ef0c6fc6a26b567c411de49436102fe160be77449cd6a61c`  
		Last Modified: Tue, 28 Nov 2023 23:28:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35953f3d9a8fcaf391e959e774c837246a6620d6b6dfd4354d39f512700a48c7`  
		Last Modified: Tue, 28 Nov 2023 23:28:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608042efc75de4b1500b0e5e17c8eb2f812774a9f703d32ac7433815356e241`  
		Last Modified: Tue, 28 Nov 2023 23:28:58 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19549ecd62c9d0fd23dc6b1bf8c51be5de3e56a58e87eef22fc87cccaf3c3714`  
		Last Modified: Tue, 28 Nov 2023 23:28:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:7439fb83eef6aa53adea0998f3bec22d666b122675c2c9c9aeaa3bf5aa5bf8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:140fa657977b1b605390bdf7aca64ebf8937567124600631e20751fc7aca9f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595444044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb591a7d8a95c271d1bbdfdbcfade49852ff05eebeaf067f803981f84e9b813`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:38:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:38:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:38:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:38:22 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:40:32 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:43:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:43:14 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:43:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 28 Nov 2023 23:33:56 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:33:57 GMT
ARG ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
# Tue, 28 Nov 2023 23:36:01 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:36:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:36:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:36:06 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:36:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:36:06 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:36:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:36:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:36:07 GMT
USER odoo
# Tue, 28 Nov 2023 23:36:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:36:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb3c31d88935a4bd21fe72cde4d10cf70f938ed370d1589f5afe78de8e9d5ef`  
		Last Modified: Tue, 14 Nov 2023 01:48:55 GMT  
		Size: 236.0 MB (236000929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635e6cd9216147592a4196f3bd6dbd96074a19264c7ec0d1ebca064d6810ba5`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 2.5 MB (2526404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ce7265beed021294fe7c29a3a1bc47a0ccdcda030d1d53cbc088171441d3a8`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 460.6 KB (460559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b808267e127a9bc3a9b1135627ed168cdcd2ef4867af1c0694215f69b77bca35`  
		Last Modified: Tue, 28 Nov 2023 23:40:09 GMT  
		Size: 326.0 MB (326014578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd43828d3e4181c5fe4cb52c8f0954ddceb4742ec62c4b2bb944ba295cc2aacb`  
		Last Modified: Tue, 28 Nov 2023 23:39:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fcfbf8eff75ad676f2ee47d277dd4f479647601c84311c07a330865daeb1ea`  
		Last Modified: Tue, 28 Nov 2023 23:39:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22adacf81d7ff9cc0c80d0ce4079ef286aa0c0442a3a2ada1de88fda96ee3b27`  
		Last Modified: Tue, 28 Nov 2023 23:39:34 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a0d6c51629ddcb1c78a795f95cd6c71a389a79c72ca3140b46be7c2e4136c0`  
		Last Modified: Tue, 28 Nov 2023 23:39:34 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b3f5f7a6363f8d7e2ca4ff4ca1ebecd991a63f7a7013b153190a11492509de53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590250868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae54c73ecd0eecfbcb59d1cf5abcd0f11c820cb9a31b4ebae13788959d75716f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 28 Nov 2023 23:53:57 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:53:57 GMT
ARG ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
# Tue, 28 Nov 2023 23:56:18 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:56:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:56:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:56:20 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:56:20 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:56:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:56:20 GMT
USER odoo
# Tue, 28 Nov 2023 23:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fde2c83350915390e5e17a879bb997a0f7c2212281f6478832ef6aad828eaa`  
		Last Modified: Tue, 28 Nov 2023 23:59:00 GMT  
		Size: 325.6 MB (325630264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6ecfd1db0d2d7758f1743e0ed6a77a641eab6586eb06bb85c0ad8f77d56399`  
		Last Modified: Tue, 28 Nov 2023 23:58:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d255c6bfabf2d531ce1d85a5d35aeeaf6a0a7967274beab93b7aa14e8f05896`  
		Last Modified: Tue, 28 Nov 2023 23:58:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d33f30c52751e59f692a7e04bf14cf04297d32369def4640b9f92f9072af39a`  
		Last Modified: Tue, 28 Nov 2023 23:58:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526901d9ecf6ec4d566232d762c9d143016ac3e8f84602fe4dd3d94808d8843e`  
		Last Modified: Tue, 28 Nov 2023 23:58:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:10f2922ae979454dd42053e96e0f52ea0d906e83710e6913fef63c3914fdc569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.6 MB (612642323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9a90adaee26cf87570a41430b18a35495f307571907ed430d249448ad5a4b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:16:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:16:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:16:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:16:49 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:21:28 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:21:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:21:53 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:21:54 GMT
ENV ODOO_VERSION=17.0
# Tue, 28 Nov 2023 23:22:14 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:22:14 GMT
ARG ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
# Tue, 28 Nov 2023 23:25:22 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:25:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:25:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:25:36 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:25:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:25:37 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:25:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:25:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:25:38 GMT
USER odoo
# Tue, 28 Nov 2023 23:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:25:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff961ccf5729ac1f3c5d8b7806dd42fa9a9fbc4083f43b7d5bc3b9bbc166edbd`  
		Last Modified: Tue, 14 Nov 2023 01:28:59 GMT  
		Size: 245.9 MB (245927069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6d3d2526a589659b9a531e4540bfd3bd343c49e9845f1409f5d7b12f7cca3`  
		Last Modified: Tue, 14 Nov 2023 01:28:17 GMT  
		Size: 2.8 MB (2803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bc659a5b58234fbb32ee9ced616e815875a88f93489359a4f37bacad64bf54`  
		Last Modified: Tue, 14 Nov 2023 01:28:16 GMT  
		Size: 460.5 KB (460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d497e129cef421d59b66a9057c8ad17dcc2d672a65dbb639971d5346c5196`  
		Last Modified: Tue, 28 Nov 2023 23:29:42 GMT  
		Size: 327.8 MB (327766255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b7b923ce44552ef0c6fc6a26b567c411de49436102fe160be77449cd6a61c`  
		Last Modified: Tue, 28 Nov 2023 23:28:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35953f3d9a8fcaf391e959e774c837246a6620d6b6dfd4354d39f512700a48c7`  
		Last Modified: Tue, 28 Nov 2023 23:28:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608042efc75de4b1500b0e5e17c8eb2f812774a9f703d32ac7433815356e241`  
		Last Modified: Tue, 28 Nov 2023 23:28:58 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19549ecd62c9d0fd23dc6b1bf8c51be5de3e56a58e87eef22fc87cccaf3c3714`  
		Last Modified: Tue, 28 Nov 2023 23:28:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:7439fb83eef6aa53adea0998f3bec22d666b122675c2c9c9aeaa3bf5aa5bf8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:140fa657977b1b605390bdf7aca64ebf8937567124600631e20751fc7aca9f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595444044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb591a7d8a95c271d1bbdfdbcfade49852ff05eebeaf067f803981f84e9b813`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:38:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:38:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:38:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:38:22 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:40:32 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:43:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:43:14 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:43:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 28 Nov 2023 23:33:56 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:33:57 GMT
ARG ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
# Tue, 28 Nov 2023 23:36:01 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:36:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:36:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:36:06 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:36:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:36:06 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:36:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:36:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:36:07 GMT
USER odoo
# Tue, 28 Nov 2023 23:36:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:36:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb3c31d88935a4bd21fe72cde4d10cf70f938ed370d1589f5afe78de8e9d5ef`  
		Last Modified: Tue, 14 Nov 2023 01:48:55 GMT  
		Size: 236.0 MB (236000929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635e6cd9216147592a4196f3bd6dbd96074a19264c7ec0d1ebca064d6810ba5`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 2.5 MB (2526404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ce7265beed021294fe7c29a3a1bc47a0ccdcda030d1d53cbc088171441d3a8`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 460.6 KB (460559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b808267e127a9bc3a9b1135627ed168cdcd2ef4867af1c0694215f69b77bca35`  
		Last Modified: Tue, 28 Nov 2023 23:40:09 GMT  
		Size: 326.0 MB (326014578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd43828d3e4181c5fe4cb52c8f0954ddceb4742ec62c4b2bb944ba295cc2aacb`  
		Last Modified: Tue, 28 Nov 2023 23:39:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fcfbf8eff75ad676f2ee47d277dd4f479647601c84311c07a330865daeb1ea`  
		Last Modified: Tue, 28 Nov 2023 23:39:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22adacf81d7ff9cc0c80d0ce4079ef286aa0c0442a3a2ada1de88fda96ee3b27`  
		Last Modified: Tue, 28 Nov 2023 23:39:34 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a0d6c51629ddcb1c78a795f95cd6c71a389a79c72ca3140b46be7c2e4136c0`  
		Last Modified: Tue, 28 Nov 2023 23:39:34 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b3f5f7a6363f8d7e2ca4ff4ca1ebecd991a63f7a7013b153190a11492509de53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590250868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae54c73ecd0eecfbcb59d1cf5abcd0f11c820cb9a31b4ebae13788959d75716f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 28 Nov 2023 23:53:57 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:53:57 GMT
ARG ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
# Tue, 28 Nov 2023 23:56:18 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:56:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:56:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:56:20 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:56:20 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:56:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:56:20 GMT
USER odoo
# Tue, 28 Nov 2023 23:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fde2c83350915390e5e17a879bb997a0f7c2212281f6478832ef6aad828eaa`  
		Last Modified: Tue, 28 Nov 2023 23:59:00 GMT  
		Size: 325.6 MB (325630264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6ecfd1db0d2d7758f1743e0ed6a77a641eab6586eb06bb85c0ad8f77d56399`  
		Last Modified: Tue, 28 Nov 2023 23:58:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d255c6bfabf2d531ce1d85a5d35aeeaf6a0a7967274beab93b7aa14e8f05896`  
		Last Modified: Tue, 28 Nov 2023 23:58:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d33f30c52751e59f692a7e04bf14cf04297d32369def4640b9f92f9072af39a`  
		Last Modified: Tue, 28 Nov 2023 23:58:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526901d9ecf6ec4d566232d762c9d143016ac3e8f84602fe4dd3d94808d8843e`  
		Last Modified: Tue, 28 Nov 2023 23:58:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:10f2922ae979454dd42053e96e0f52ea0d906e83710e6913fef63c3914fdc569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.6 MB (612642323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9a90adaee26cf87570a41430b18a35495f307571907ed430d249448ad5a4b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:16:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:16:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:16:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:16:49 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:21:28 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:21:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:21:53 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:21:54 GMT
ENV ODOO_VERSION=17.0
# Tue, 28 Nov 2023 23:22:14 GMT
ARG ODOO_RELEASE=20231127
# Tue, 28 Nov 2023 23:22:14 GMT
ARG ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
# Tue, 28 Nov 2023 23:25:22 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Nov 2023 23:25:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Nov 2023 23:25:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Nov 2023 23:25:36 GMT
# ARGS: ODOO_RELEASE=20231127 ODOO_SHA=b6953cecd2f06a24dc509cef277ffcd03f243a97
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Nov 2023 23:25:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Nov 2023 23:25:37 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Nov 2023 23:25:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Nov 2023 23:25:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Nov 2023 23:25:38 GMT
USER odoo
# Tue, 28 Nov 2023 23:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Nov 2023 23:25:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff961ccf5729ac1f3c5d8b7806dd42fa9a9fbc4083f43b7d5bc3b9bbc166edbd`  
		Last Modified: Tue, 14 Nov 2023 01:28:59 GMT  
		Size: 245.9 MB (245927069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6d3d2526a589659b9a531e4540bfd3bd343c49e9845f1409f5d7b12f7cca3`  
		Last Modified: Tue, 14 Nov 2023 01:28:17 GMT  
		Size: 2.8 MB (2803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bc659a5b58234fbb32ee9ced616e815875a88f93489359a4f37bacad64bf54`  
		Last Modified: Tue, 14 Nov 2023 01:28:16 GMT  
		Size: 460.5 KB (460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d497e129cef421d59b66a9057c8ad17dcc2d672a65dbb639971d5346c5196`  
		Last Modified: Tue, 28 Nov 2023 23:29:42 GMT  
		Size: 327.8 MB (327766255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b7b923ce44552ef0c6fc6a26b567c411de49436102fe160be77449cd6a61c`  
		Last Modified: Tue, 28 Nov 2023 23:28:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35953f3d9a8fcaf391e959e774c837246a6620d6b6dfd4354d39f512700a48c7`  
		Last Modified: Tue, 28 Nov 2023 23:28:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608042efc75de4b1500b0e5e17c8eb2f812774a9f703d32ac7433815356e241`  
		Last Modified: Tue, 28 Nov 2023 23:28:58 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19549ecd62c9d0fd23dc6b1bf8c51be5de3e56a58e87eef22fc87cccaf3c3714`  
		Last Modified: Tue, 28 Nov 2023 23:28:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
