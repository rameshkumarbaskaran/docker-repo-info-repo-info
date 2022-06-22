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
$ docker pull odoo@sha256:986d56b4544b6997c8879467560a6f728613c916c1ff59a330ea5dbba6e2ab3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:dd7110af910cc60c728e01749e5339cb723848f5d0bd3c274d790722aeb5aec1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540167442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c451a125ec6a1fc1f852f698e63b7890ff8d1deb76be856076bc1642a5835385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:05:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:05:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:05:50 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:05:51 GMT
ENV ODOO_VERSION=13.0
# Tue, 21 Jun 2022 22:26:16 GMT
ARG ODOO_RELEASE=20220620
# Tue, 21 Jun 2022 22:26:16 GMT
ARG ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
# Tue, 21 Jun 2022 22:27:27 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Jun 2022 22:27:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Jun 2022 22:27:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Jun 2022 22:27:31 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Jun 2022 22:27:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Jun 2022 22:27:31 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Jun 2022 22:27:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Jun 2022 22:27:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Jun 2022 22:27:31 GMT
USER odoo
# Tue, 21 Jun 2022 22:27:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 22:27:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c79567322b70756577efd1f8dcfa0263c984e263011e9803a7cda6aba5173a5`  
		Last Modified: Sat, 28 May 2022 12:09:33 GMT  
		Size: 207.1 MB (207143382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a85e75296e74df756190aea4b584b8e8697311966131e1f25a32ab750c6a6c`  
		Last Modified: Sat, 28 May 2022 12:09:11 GMT  
		Size: 13.4 MB (13442815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3489e5884bd67ef88e775a66acb08289f084239dc3fc159caa11154b5f40f2`  
		Last Modified: Sat, 28 May 2022 12:09:08 GMT  
		Size: 480.5 KB (480504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf4014651ec2ce234df61676732267cdf1fc38cfca8ff5a92f9b544ff3150cf`  
		Last Modified: Tue, 21 Jun 2022 22:29:51 GMT  
		Size: 292.0 MB (291958130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01533c5551a535cec12f5c3c8ac504c6d1bd191d468bf2b6aca7cf55392f68b3`  
		Last Modified: Tue, 21 Jun 2022 22:29:19 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d2995556ad71d5422eb55ac105cba33fcd0efa99d08ed55d7d7bd3c8c7b38`  
		Last Modified: Tue, 21 Jun 2022 22:29:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e507bbe82237c036bec9170ad5951c15bae31047102c91ef7d11e370a5cea136`  
		Last Modified: Tue, 21 Jun 2022 22:29:20 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba377406a140b2009fa535deccb918a71f9fd4a8daa24ad7dfc4b5e3596927fc`  
		Last Modified: Tue, 21 Jun 2022 22:29:20 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:986d56b4544b6997c8879467560a6f728613c916c1ff59a330ea5dbba6e2ab3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:dd7110af910cc60c728e01749e5339cb723848f5d0bd3c274d790722aeb5aec1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540167442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c451a125ec6a1fc1f852f698e63b7890ff8d1deb76be856076bc1642a5835385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:05:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:05:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:05:50 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:05:51 GMT
ENV ODOO_VERSION=13.0
# Tue, 21 Jun 2022 22:26:16 GMT
ARG ODOO_RELEASE=20220620
# Tue, 21 Jun 2022 22:26:16 GMT
ARG ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
# Tue, 21 Jun 2022 22:27:27 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Jun 2022 22:27:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Jun 2022 22:27:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Jun 2022 22:27:31 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Jun 2022 22:27:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Jun 2022 22:27:31 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Jun 2022 22:27:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Jun 2022 22:27:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Jun 2022 22:27:31 GMT
USER odoo
# Tue, 21 Jun 2022 22:27:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 22:27:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c79567322b70756577efd1f8dcfa0263c984e263011e9803a7cda6aba5173a5`  
		Last Modified: Sat, 28 May 2022 12:09:33 GMT  
		Size: 207.1 MB (207143382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a85e75296e74df756190aea4b584b8e8697311966131e1f25a32ab750c6a6c`  
		Last Modified: Sat, 28 May 2022 12:09:11 GMT  
		Size: 13.4 MB (13442815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3489e5884bd67ef88e775a66acb08289f084239dc3fc159caa11154b5f40f2`  
		Last Modified: Sat, 28 May 2022 12:09:08 GMT  
		Size: 480.5 KB (480504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf4014651ec2ce234df61676732267cdf1fc38cfca8ff5a92f9b544ff3150cf`  
		Last Modified: Tue, 21 Jun 2022 22:29:51 GMT  
		Size: 292.0 MB (291958130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01533c5551a535cec12f5c3c8ac504c6d1bd191d468bf2b6aca7cf55392f68b3`  
		Last Modified: Tue, 21 Jun 2022 22:29:19 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d2995556ad71d5422eb55ac105cba33fcd0efa99d08ed55d7d7bd3c8c7b38`  
		Last Modified: Tue, 21 Jun 2022 22:29:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e507bbe82237c036bec9170ad5951c15bae31047102c91ef7d11e370a5cea136`  
		Last Modified: Tue, 21 Jun 2022 22:29:20 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba377406a140b2009fa535deccb918a71f9fd4a8daa24ad7dfc4b5e3596927fc`  
		Last Modified: Tue, 21 Jun 2022 22:29:20 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:9a75f4b1c6fca11fe12965402731d9149157e254a18ee06a8a9477224ed23841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:0330c3c5b5120edbf47732b279c1ebadd425f60be18184164aad6235d825f851
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.5 MB (530456769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b181205b79f276478abf2bdf18b5f0ec306d7c5fa8c50e71ed1f2981343ed64c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:02:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:03:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:03:12 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:03:12 GMT
ENV ODOO_VERSION=14.0
# Tue, 21 Jun 2022 22:24:53 GMT
ARG ODOO_RELEASE=20220620
# Tue, 21 Jun 2022 22:24:53 GMT
ARG ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
# Tue, 21 Jun 2022 22:26:05 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Jun 2022 22:26:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Jun 2022 22:26:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Jun 2022 22:26:10 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Jun 2022 22:26:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Jun 2022 22:26:10 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Jun 2022 22:26:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Jun 2022 22:26:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Jun 2022 22:26:10 GMT
USER odoo
# Tue, 21 Jun 2022 22:26:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 22:26:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608dd6a1d283847f2f81e849d0bc623071e8222593eee6db00992e4b10b89700`  
		Last Modified: Sat, 28 May 2022 12:08:49 GMT  
		Size: 213.2 MB (213182131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca95c4836277ec91a64f63d069fe261f1155cd52d36b779818dc11814d993346`  
		Last Modified: Sat, 28 May 2022 12:08:27 GMT  
		Size: 13.4 MB (13445276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee21d359e137fb4b2d1a88d7964e3d51382ec95d462e59aea10e50328972a92`  
		Last Modified: Sat, 28 May 2022 12:08:24 GMT  
		Size: 480.4 KB (480424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9320cdc477539a281ae914b9b349dbb246cad218964154ff3770441a77f85b`  
		Last Modified: Tue, 21 Jun 2022 22:29:09 GMT  
		Size: 276.2 MB (276206332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdd9d4bec158338fa2526c5c369b504a23f28ac33e1cc8648eda88a0d605ffd`  
		Last Modified: Tue, 21 Jun 2022 22:28:37 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec06a0c58a6e65ecc524806c4c777b09bcb9d399a5714696e34f3e68eb77171`  
		Last Modified: Tue, 21 Jun 2022 22:28:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fe74be1a8ae62ccfba568641d29391779afe3c4aadc41e1ef863d8bf81afc4`  
		Last Modified: Tue, 21 Jun 2022 22:28:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbf494b0d96c2cd9668673fd0bf60fb31f73a878d6e494f881d56113b9e26b2`  
		Last Modified: Tue, 21 Jun 2022 22:28:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:9a75f4b1c6fca11fe12965402731d9149157e254a18ee06a8a9477224ed23841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:0330c3c5b5120edbf47732b279c1ebadd425f60be18184164aad6235d825f851
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.5 MB (530456769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b181205b79f276478abf2bdf18b5f0ec306d7c5fa8c50e71ed1f2981343ed64c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:02:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:03:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:03:12 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:03:12 GMT
ENV ODOO_VERSION=14.0
# Tue, 21 Jun 2022 22:24:53 GMT
ARG ODOO_RELEASE=20220620
# Tue, 21 Jun 2022 22:24:53 GMT
ARG ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
# Tue, 21 Jun 2022 22:26:05 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Jun 2022 22:26:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Jun 2022 22:26:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Jun 2022 22:26:10 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Jun 2022 22:26:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Jun 2022 22:26:10 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Jun 2022 22:26:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Jun 2022 22:26:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Jun 2022 22:26:10 GMT
USER odoo
# Tue, 21 Jun 2022 22:26:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 22:26:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608dd6a1d283847f2f81e849d0bc623071e8222593eee6db00992e4b10b89700`  
		Last Modified: Sat, 28 May 2022 12:08:49 GMT  
		Size: 213.2 MB (213182131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca95c4836277ec91a64f63d069fe261f1155cd52d36b779818dc11814d993346`  
		Last Modified: Sat, 28 May 2022 12:08:27 GMT  
		Size: 13.4 MB (13445276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee21d359e137fb4b2d1a88d7964e3d51382ec95d462e59aea10e50328972a92`  
		Last Modified: Sat, 28 May 2022 12:08:24 GMT  
		Size: 480.4 KB (480424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9320cdc477539a281ae914b9b349dbb246cad218964154ff3770441a77f85b`  
		Last Modified: Tue, 21 Jun 2022 22:29:09 GMT  
		Size: 276.2 MB (276206332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdd9d4bec158338fa2526c5c369b504a23f28ac33e1cc8648eda88a0d605ffd`  
		Last Modified: Tue, 21 Jun 2022 22:28:37 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec06a0c58a6e65ecc524806c4c777b09bcb9d399a5714696e34f3e68eb77171`  
		Last Modified: Tue, 21 Jun 2022 22:28:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fe74be1a8ae62ccfba568641d29391779afe3c4aadc41e1ef863d8bf81afc4`  
		Last Modified: Tue, 21 Jun 2022 22:28:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbf494b0d96c2cd9668673fd0bf60fb31f73a878d6e494f881d56113b9e26b2`  
		Last Modified: Tue, 21 Jun 2022 22:28:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:63b938e2d430536497e58ebd641d9a58a4a9bfd4d1aa61fcab21481d1b2fba4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:980a1bc18645b513be9be4b85936e888ed636de082da7f23da25a1f1e0069d4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.8 MB (555774804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628b44140659fa98452395b914b94e983cbbd38283b85e0a62d143dc70c35ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Tue, 21 Jun 2022 22:23:29 GMT
ARG ODOO_RELEASE=20220620
# Tue, 21 Jun 2022 22:23:30 GMT
ARG ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
# Tue, 21 Jun 2022 22:24:45 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Jun 2022 22:24:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Jun 2022 22:24:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Jun 2022 22:24:50 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Jun 2022 22:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Jun 2022 22:24:50 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Jun 2022 22:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Jun 2022 22:24:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Jun 2022 22:24:50 GMT
USER odoo
# Tue, 21 Jun 2022 22:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 22:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0b37a0090e55e8801c2b55f1491a5ee2cd6e91a18a4adae391b07038fbbbc`  
		Last Modified: Tue, 21 Jun 2022 22:28:24 GMT  
		Size: 301.1 MB (301097212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc62c4ff4e0778783d58dfa1bc05b1da4dc6a62fa75e19db76b4b5b4a044184`  
		Last Modified: Tue, 21 Jun 2022 22:27:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40527aa67e84d4fa3c3794f4f3b193644a3753b964ceb1ebdf4f54c06a70e165`  
		Last Modified: Tue, 21 Jun 2022 22:27:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c97390c59564f9c609739c056eba5c4c3eab24c70cb6c998f2d8f1176f4cbbc`  
		Last Modified: Tue, 21 Jun 2022 22:27:50 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d806865330671b54a0fc4d22eff116e6bb6ea86e8b14d7157329178aa90f3b`  
		Last Modified: Tue, 21 Jun 2022 22:27:50 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:63b938e2d430536497e58ebd641d9a58a4a9bfd4d1aa61fcab21481d1b2fba4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:980a1bc18645b513be9be4b85936e888ed636de082da7f23da25a1f1e0069d4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.8 MB (555774804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628b44140659fa98452395b914b94e983cbbd38283b85e0a62d143dc70c35ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Tue, 21 Jun 2022 22:23:29 GMT
ARG ODOO_RELEASE=20220620
# Tue, 21 Jun 2022 22:23:30 GMT
ARG ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
# Tue, 21 Jun 2022 22:24:45 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Jun 2022 22:24:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Jun 2022 22:24:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Jun 2022 22:24:50 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Jun 2022 22:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Jun 2022 22:24:50 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Jun 2022 22:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Jun 2022 22:24:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Jun 2022 22:24:50 GMT
USER odoo
# Tue, 21 Jun 2022 22:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 22:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0b37a0090e55e8801c2b55f1491a5ee2cd6e91a18a4adae391b07038fbbbc`  
		Last Modified: Tue, 21 Jun 2022 22:28:24 GMT  
		Size: 301.1 MB (301097212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc62c4ff4e0778783d58dfa1bc05b1da4dc6a62fa75e19db76b4b5b4a044184`  
		Last Modified: Tue, 21 Jun 2022 22:27:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40527aa67e84d4fa3c3794f4f3b193644a3753b964ceb1ebdf4f54c06a70e165`  
		Last Modified: Tue, 21 Jun 2022 22:27:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c97390c59564f9c609739c056eba5c4c3eab24c70cb6c998f2d8f1176f4cbbc`  
		Last Modified: Tue, 21 Jun 2022 22:27:50 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d806865330671b54a0fc4d22eff116e6bb6ea86e8b14d7157329178aa90f3b`  
		Last Modified: Tue, 21 Jun 2022 22:27:50 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:63b938e2d430536497e58ebd641d9a58a4a9bfd4d1aa61fcab21481d1b2fba4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:980a1bc18645b513be9be4b85936e888ed636de082da7f23da25a1f1e0069d4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.8 MB (555774804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628b44140659fa98452395b914b94e983cbbd38283b85e0a62d143dc70c35ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Tue, 21 Jun 2022 22:23:29 GMT
ARG ODOO_RELEASE=20220620
# Tue, 21 Jun 2022 22:23:30 GMT
ARG ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
# Tue, 21 Jun 2022 22:24:45 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Jun 2022 22:24:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Jun 2022 22:24:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Jun 2022 22:24:50 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Jun 2022 22:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Jun 2022 22:24:50 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Jun 2022 22:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Jun 2022 22:24:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Jun 2022 22:24:50 GMT
USER odoo
# Tue, 21 Jun 2022 22:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 22:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0b37a0090e55e8801c2b55f1491a5ee2cd6e91a18a4adae391b07038fbbbc`  
		Last Modified: Tue, 21 Jun 2022 22:28:24 GMT  
		Size: 301.1 MB (301097212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc62c4ff4e0778783d58dfa1bc05b1da4dc6a62fa75e19db76b4b5b4a044184`  
		Last Modified: Tue, 21 Jun 2022 22:27:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40527aa67e84d4fa3c3794f4f3b193644a3753b964ceb1ebdf4f54c06a70e165`  
		Last Modified: Tue, 21 Jun 2022 22:27:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c97390c59564f9c609739c056eba5c4c3eab24c70cb6c998f2d8f1176f4cbbc`  
		Last Modified: Tue, 21 Jun 2022 22:27:50 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d806865330671b54a0fc4d22eff116e6bb6ea86e8b14d7157329178aa90f3b`  
		Last Modified: Tue, 21 Jun 2022 22:27:50 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
