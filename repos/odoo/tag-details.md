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
$ docker pull odoo@sha256:991aaec09a2a5879ef0426f9aa6bc71cf7eb7b1cfa1cd218721b70b56ea7bcf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:b2ef1de4321dcd4729f2d80a40ab576caedd5e596b9c215c7bdec2f2946dc4cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540092251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc544ab99bba89efc93fd59c7cc9538e84fc1f0bce6c6bda43056b834a08652`
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
# Tue, 31 May 2022 23:44:44 GMT
ARG ODOO_RELEASE=20220531
# Tue, 31 May 2022 23:44:45 GMT
ARG ODOO_SHA=d3d7e789c2abd43ff5548d7e1ff879393b5689f3
# Tue, 31 May 2022 23:45:57 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=d3d7e789c2abd43ff5548d7e1ff879393b5689f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 May 2022 23:46:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 31 May 2022 23:46:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 May 2022 23:46:01 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=d3d7e789c2abd43ff5548d7e1ff879393b5689f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 May 2022 23:46:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 May 2022 23:46:01 GMT
EXPOSE 8069 8071 8072
# Tue, 31 May 2022 23:46:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 May 2022 23:46:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 May 2022 23:46:01 GMT
USER odoo
# Tue, 31 May 2022 23:46:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 May 2022 23:46:02 GMT
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
	-	`sha256:5fe204d10bc2d360638fb8de1950410c4f21074f0d7e97fdd05595bd8b377d87`  
		Last Modified: Tue, 31 May 2022 23:48:20 GMT  
		Size: 291.9 MB (291882940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f75ee0bbfd27ccec427f346e3a90c644b5fccb69a494c7f73e13a0d56a3df9`  
		Last Modified: Tue, 31 May 2022 23:47:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3230ea41cede602515061163c3a9686e9ef98b1ae550d8b29744cff428e44545`  
		Last Modified: Tue, 31 May 2022 23:47:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea7482b1bc9546ea6ea76d56508339f5fdc3be9683b375bb91510683c679502`  
		Last Modified: Tue, 31 May 2022 23:47:48 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7957a516effab7ee5b6cd6736aa702345c64b2fd41ad844c75761712c567c4b5`  
		Last Modified: Tue, 31 May 2022 23:47:48 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:991aaec09a2a5879ef0426f9aa6bc71cf7eb7b1cfa1cd218721b70b56ea7bcf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:b2ef1de4321dcd4729f2d80a40ab576caedd5e596b9c215c7bdec2f2946dc4cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540092251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc544ab99bba89efc93fd59c7cc9538e84fc1f0bce6c6bda43056b834a08652`
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
# Tue, 31 May 2022 23:44:44 GMT
ARG ODOO_RELEASE=20220531
# Tue, 31 May 2022 23:44:45 GMT
ARG ODOO_SHA=d3d7e789c2abd43ff5548d7e1ff879393b5689f3
# Tue, 31 May 2022 23:45:57 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=d3d7e789c2abd43ff5548d7e1ff879393b5689f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 May 2022 23:46:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 31 May 2022 23:46:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 May 2022 23:46:01 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=d3d7e789c2abd43ff5548d7e1ff879393b5689f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 May 2022 23:46:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 May 2022 23:46:01 GMT
EXPOSE 8069 8071 8072
# Tue, 31 May 2022 23:46:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 May 2022 23:46:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 May 2022 23:46:01 GMT
USER odoo
# Tue, 31 May 2022 23:46:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 May 2022 23:46:02 GMT
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
	-	`sha256:5fe204d10bc2d360638fb8de1950410c4f21074f0d7e97fdd05595bd8b377d87`  
		Last Modified: Tue, 31 May 2022 23:48:20 GMT  
		Size: 291.9 MB (291882940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f75ee0bbfd27ccec427f346e3a90c644b5fccb69a494c7f73e13a0d56a3df9`  
		Last Modified: Tue, 31 May 2022 23:47:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3230ea41cede602515061163c3a9686e9ef98b1ae550d8b29744cff428e44545`  
		Last Modified: Tue, 31 May 2022 23:47:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea7482b1bc9546ea6ea76d56508339f5fdc3be9683b375bb91510683c679502`  
		Last Modified: Tue, 31 May 2022 23:47:48 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7957a516effab7ee5b6cd6736aa702345c64b2fd41ad844c75761712c567c4b5`  
		Last Modified: Tue, 31 May 2022 23:47:48 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:a07da6247bb1f8bc8cadfe40ac303b6514d5be24dcd649473d7cdd66fe912c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:d68188e0794ce89d7a9184338f58fc53d4ea4c3ace68d7d8b9bd0a303a5ad3f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.3 MB (530255743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20129a1433330c94d31e391562ad3334e06da4b13f84f35c941d469453e55fc`
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
# Tue, 31 May 2022 23:43:22 GMT
ARG ODOO_RELEASE=20220531
# Tue, 31 May 2022 23:43:22 GMT
ARG ODOO_SHA=fdf78d37dd9b41a737a6314c8997863b4e5be3a2
# Tue, 31 May 2022 23:44:35 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=fdf78d37dd9b41a737a6314c8997863b4e5be3a2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 May 2022 23:44:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 31 May 2022 23:44:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 May 2022 23:44:40 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=fdf78d37dd9b41a737a6314c8997863b4e5be3a2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 May 2022 23:44:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 May 2022 23:44:40 GMT
EXPOSE 8069 8071 8072
# Tue, 31 May 2022 23:44:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 May 2022 23:44:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 May 2022 23:44:40 GMT
USER odoo
# Tue, 31 May 2022 23:44:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 May 2022 23:44:40 GMT
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
	-	`sha256:22c5ccfac8eafdf56c6bc96cfef5be37533c68afd27dce2f23e166574508b235`  
		Last Modified: Tue, 31 May 2022 23:47:38 GMT  
		Size: 276.0 MB (276005308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d4943b9bf6cf9c8534e5d43afee7fa1db74967422bb153a8c85a927250f8f`  
		Last Modified: Tue, 31 May 2022 23:47:06 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94332791dc7b7dd70516320e58eb63b037774ca86991cf47be973c189e2a77c7`  
		Last Modified: Tue, 31 May 2022 23:47:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a918c0cbf91fbf44e9b4afc96a1da1b88f43bab55297c1b50482fb54715d63bb`  
		Last Modified: Tue, 31 May 2022 23:47:06 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18877d9d28054308a45c0029b60388a2c05784428055ce3315d15ffdf897e1fc`  
		Last Modified: Tue, 31 May 2022 23:47:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:a07da6247bb1f8bc8cadfe40ac303b6514d5be24dcd649473d7cdd66fe912c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:d68188e0794ce89d7a9184338f58fc53d4ea4c3ace68d7d8b9bd0a303a5ad3f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.3 MB (530255743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20129a1433330c94d31e391562ad3334e06da4b13f84f35c941d469453e55fc`
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
# Tue, 31 May 2022 23:43:22 GMT
ARG ODOO_RELEASE=20220531
# Tue, 31 May 2022 23:43:22 GMT
ARG ODOO_SHA=fdf78d37dd9b41a737a6314c8997863b4e5be3a2
# Tue, 31 May 2022 23:44:35 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=fdf78d37dd9b41a737a6314c8997863b4e5be3a2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 May 2022 23:44:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 31 May 2022 23:44:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 May 2022 23:44:40 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=fdf78d37dd9b41a737a6314c8997863b4e5be3a2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 May 2022 23:44:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 May 2022 23:44:40 GMT
EXPOSE 8069 8071 8072
# Tue, 31 May 2022 23:44:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 May 2022 23:44:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 May 2022 23:44:40 GMT
USER odoo
# Tue, 31 May 2022 23:44:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 May 2022 23:44:40 GMT
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
	-	`sha256:22c5ccfac8eafdf56c6bc96cfef5be37533c68afd27dce2f23e166574508b235`  
		Last Modified: Tue, 31 May 2022 23:47:38 GMT  
		Size: 276.0 MB (276005308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d4943b9bf6cf9c8534e5d43afee7fa1db74967422bb153a8c85a927250f8f`  
		Last Modified: Tue, 31 May 2022 23:47:06 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94332791dc7b7dd70516320e58eb63b037774ca86991cf47be973c189e2a77c7`  
		Last Modified: Tue, 31 May 2022 23:47:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a918c0cbf91fbf44e9b4afc96a1da1b88f43bab55297c1b50482fb54715d63bb`  
		Last Modified: Tue, 31 May 2022 23:47:06 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18877d9d28054308a45c0029b60388a2c05784428055ce3315d15ffdf897e1fc`  
		Last Modified: Tue, 31 May 2022 23:47:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:319a8380299d6bfb2c91ab502dd3c5ed1fbd4473ae53cdfa8c6a09d9850a1ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:8e7af29884eca907e9aba2b0708e813ad7122e415c91283f7b07500d15176247
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.5 MB (555505905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efbf7ab8133c1f9075d549c0c1391b903ded05974397edcc081f467d3a9a1f`
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
# Tue, 31 May 2022 23:41:44 GMT
ARG ODOO_RELEASE=20220531
# Tue, 31 May 2022 23:41:44 GMT
ARG ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
# Tue, 31 May 2022 23:43:03 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 May 2022 23:43:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 31 May 2022 23:43:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 May 2022 23:43:08 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 May 2022 23:43:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 May 2022 23:43:08 GMT
EXPOSE 8069 8071 8072
# Tue, 31 May 2022 23:43:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 May 2022 23:43:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 May 2022 23:43:09 GMT
USER odoo
# Tue, 31 May 2022 23:43:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 May 2022 23:43:09 GMT
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
	-	`sha256:5fe67b31b4a5d6e70f802e329f746cc5eb83b5f4d7308f659a275e0d4e95ed98`  
		Last Modified: Tue, 31 May 2022 23:46:53 GMT  
		Size: 300.8 MB (300828310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b92606d73201d0611ce0ab91b00bcb675da44dfe47e6050763807c40a8b4535`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dcb455fed951bc0539d10ae1963ad5d43645245cc0e4924e5c1d3ef03fd588`  
		Last Modified: Tue, 31 May 2022 23:46:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f50b42ae4fae483f6da3a48796adab460af20bb8553f0049b33b6eed11ef06`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe14c42b771b8bb1cf5bc12be1bd5184ce631d417af78b4f056d4f1ca75ad69`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:319a8380299d6bfb2c91ab502dd3c5ed1fbd4473ae53cdfa8c6a09d9850a1ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:8e7af29884eca907e9aba2b0708e813ad7122e415c91283f7b07500d15176247
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.5 MB (555505905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efbf7ab8133c1f9075d549c0c1391b903ded05974397edcc081f467d3a9a1f`
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
# Tue, 31 May 2022 23:41:44 GMT
ARG ODOO_RELEASE=20220531
# Tue, 31 May 2022 23:41:44 GMT
ARG ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
# Tue, 31 May 2022 23:43:03 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 May 2022 23:43:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 31 May 2022 23:43:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 May 2022 23:43:08 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 May 2022 23:43:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 May 2022 23:43:08 GMT
EXPOSE 8069 8071 8072
# Tue, 31 May 2022 23:43:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 May 2022 23:43:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 May 2022 23:43:09 GMT
USER odoo
# Tue, 31 May 2022 23:43:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 May 2022 23:43:09 GMT
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
	-	`sha256:5fe67b31b4a5d6e70f802e329f746cc5eb83b5f4d7308f659a275e0d4e95ed98`  
		Last Modified: Tue, 31 May 2022 23:46:53 GMT  
		Size: 300.8 MB (300828310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b92606d73201d0611ce0ab91b00bcb675da44dfe47e6050763807c40a8b4535`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dcb455fed951bc0539d10ae1963ad5d43645245cc0e4924e5c1d3ef03fd588`  
		Last Modified: Tue, 31 May 2022 23:46:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f50b42ae4fae483f6da3a48796adab460af20bb8553f0049b33b6eed11ef06`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe14c42b771b8bb1cf5bc12be1bd5184ce631d417af78b4f056d4f1ca75ad69`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:319a8380299d6bfb2c91ab502dd3c5ed1fbd4473ae53cdfa8c6a09d9850a1ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:8e7af29884eca907e9aba2b0708e813ad7122e415c91283f7b07500d15176247
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.5 MB (555505905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efbf7ab8133c1f9075d549c0c1391b903ded05974397edcc081f467d3a9a1f`
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
# Tue, 31 May 2022 23:41:44 GMT
ARG ODOO_RELEASE=20220531
# Tue, 31 May 2022 23:41:44 GMT
ARG ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
# Tue, 31 May 2022 23:43:03 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 May 2022 23:43:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 31 May 2022 23:43:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 May 2022 23:43:08 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 May 2022 23:43:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 May 2022 23:43:08 GMT
EXPOSE 8069 8071 8072
# Tue, 31 May 2022 23:43:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 May 2022 23:43:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 May 2022 23:43:09 GMT
USER odoo
# Tue, 31 May 2022 23:43:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 May 2022 23:43:09 GMT
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
	-	`sha256:5fe67b31b4a5d6e70f802e329f746cc5eb83b5f4d7308f659a275e0d4e95ed98`  
		Last Modified: Tue, 31 May 2022 23:46:53 GMT  
		Size: 300.8 MB (300828310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b92606d73201d0611ce0ab91b00bcb675da44dfe47e6050763807c40a8b4535`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dcb455fed951bc0539d10ae1963ad5d43645245cc0e4924e5c1d3ef03fd588`  
		Last Modified: Tue, 31 May 2022 23:46:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f50b42ae4fae483f6da3a48796adab460af20bb8553f0049b33b6eed11ef06`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe14c42b771b8bb1cf5bc12be1bd5184ce631d417af78b4f056d4f1ca75ad69`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
