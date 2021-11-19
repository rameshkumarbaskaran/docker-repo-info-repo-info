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
$ docker pull odoo@sha256:9cc241372c319ea2ed33d13111e299c58c502e46114b40d882c702f304dd0dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:f18d7951d81d439a5297e383ff31e02564837a058d00c35b508bd365f82818df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539566819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d62298d732b6f54199db037c750a70eb917713969419a09f5323590e7e80a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:13:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Nov 2021 09:13:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Nov 2021 09:13:18 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:17:15 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Nov 2021 09:17:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:17:29 GMT
RUN npm install -g rtlcss
# Wed, 17 Nov 2021 09:17:30 GMT
ENV ODOO_VERSION=13.0
# Fri, 19 Nov 2021 21:22:51 GMT
ARG ODOO_RELEASE=20211119
# Fri, 19 Nov 2021 21:22:52 GMT
ARG ODOO_SHA=7081390e60485a6caa1ded5d6a092a25ff851888
# Fri, 19 Nov 2021 21:24:06 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=7081390e60485a6caa1ded5d6a092a25ff851888
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Nov 2021 21:24:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Nov 2021 21:24:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Nov 2021 21:24:10 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=7081390e60485a6caa1ded5d6a092a25ff851888
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Nov 2021 21:24:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Nov 2021 21:24:11 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Nov 2021 21:24:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Nov 2021 21:24:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Nov 2021 21:24:11 GMT
USER odoo
# Fri, 19 Nov 2021 21:24:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 21:24:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000d6f871a597077bc945f27930d96427d837fb6bc47a4d8322ba718d61a2a0`  
		Last Modified: Wed, 17 Nov 2021 09:22:41 GMT  
		Size: 207.1 MB (207130893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a4e33b7c38be10d731e5a751ee2bdaf14ec8e15f4fe4a5fb4725a2b0545261`  
		Last Modified: Wed, 17 Nov 2021 09:22:12 GMT  
		Size: 13.4 MB (13434039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eca00fd297b3661881f76fa666c3d23fc8c09d8a29fb17f8ad8a11aa94917c9`  
		Last Modified: Wed, 17 Nov 2021 09:22:07 GMT  
		Size: 731.1 KB (731081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0a1f881b3a74109ff3e86717943764f155bc81533f71c8cc383424a2ad552b`  
		Last Modified: Fri, 19 Nov 2021 21:26:24 GMT  
		Size: 291.1 MB (291114667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da5213886d7d2edab99c14b779b3754023b4b4b807641acf2cab70ad05a2afa`  
		Last Modified: Fri, 19 Nov 2021 21:25:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d72f443e613d2b7c6556c064e6c0569f0a5fb3cfb46624e9aa77231ee680e8`  
		Last Modified: Fri, 19 Nov 2021 21:25:54 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b93289401a43a5b3a21a03b2a934efec9d971098ef122a8a2348e30ece3ea8`  
		Last Modified: Fri, 19 Nov 2021 21:25:54 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848d401d1c27df749dff6a45c6745fb560ecbeb795a8569ee0d907775ec3d95a`  
		Last Modified: Fri, 19 Nov 2021 21:25:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:9cc241372c319ea2ed33d13111e299c58c502e46114b40d882c702f304dd0dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:f18d7951d81d439a5297e383ff31e02564837a058d00c35b508bd365f82818df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539566819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d62298d732b6f54199db037c750a70eb917713969419a09f5323590e7e80a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:13:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Nov 2021 09:13:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Nov 2021 09:13:18 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:17:15 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Nov 2021 09:17:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:17:29 GMT
RUN npm install -g rtlcss
# Wed, 17 Nov 2021 09:17:30 GMT
ENV ODOO_VERSION=13.0
# Fri, 19 Nov 2021 21:22:51 GMT
ARG ODOO_RELEASE=20211119
# Fri, 19 Nov 2021 21:22:52 GMT
ARG ODOO_SHA=7081390e60485a6caa1ded5d6a092a25ff851888
# Fri, 19 Nov 2021 21:24:06 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=7081390e60485a6caa1ded5d6a092a25ff851888
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Nov 2021 21:24:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Nov 2021 21:24:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Nov 2021 21:24:10 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=7081390e60485a6caa1ded5d6a092a25ff851888
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Nov 2021 21:24:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Nov 2021 21:24:11 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Nov 2021 21:24:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Nov 2021 21:24:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Nov 2021 21:24:11 GMT
USER odoo
# Fri, 19 Nov 2021 21:24:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 21:24:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000d6f871a597077bc945f27930d96427d837fb6bc47a4d8322ba718d61a2a0`  
		Last Modified: Wed, 17 Nov 2021 09:22:41 GMT  
		Size: 207.1 MB (207130893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a4e33b7c38be10d731e5a751ee2bdaf14ec8e15f4fe4a5fb4725a2b0545261`  
		Last Modified: Wed, 17 Nov 2021 09:22:12 GMT  
		Size: 13.4 MB (13434039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eca00fd297b3661881f76fa666c3d23fc8c09d8a29fb17f8ad8a11aa94917c9`  
		Last Modified: Wed, 17 Nov 2021 09:22:07 GMT  
		Size: 731.1 KB (731081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0a1f881b3a74109ff3e86717943764f155bc81533f71c8cc383424a2ad552b`  
		Last Modified: Fri, 19 Nov 2021 21:26:24 GMT  
		Size: 291.1 MB (291114667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da5213886d7d2edab99c14b779b3754023b4b4b807641acf2cab70ad05a2afa`  
		Last Modified: Fri, 19 Nov 2021 21:25:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d72f443e613d2b7c6556c064e6c0569f0a5fb3cfb46624e9aa77231ee680e8`  
		Last Modified: Fri, 19 Nov 2021 21:25:54 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b93289401a43a5b3a21a03b2a934efec9d971098ef122a8a2348e30ece3ea8`  
		Last Modified: Fri, 19 Nov 2021 21:25:54 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848d401d1c27df749dff6a45c6745fb560ecbeb795a8569ee0d907775ec3d95a`  
		Last Modified: Fri, 19 Nov 2021 21:25:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:00a392fe72660b53414db4f38a9757e98842f3b4f4f006ba1a368ce7a7bf2816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:1d2acb5e45b9c68d6299e954611da23a786ca1be6297374f5b098de1c753eeb9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528476353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838a12c11c3af3fb7a88b62ab57ddc7b0a038d1a1607e91a06757715aacee090`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:13:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Nov 2021 09:13:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Nov 2021 09:13:18 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:14:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Nov 2021 09:14:41 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:14:45 GMT
RUN npm install -g rtlcss
# Wed, 17 Nov 2021 09:14:45 GMT
ENV ODOO_VERSION=14.0
# Fri, 19 Nov 2021 21:21:29 GMT
ARG ODOO_RELEASE=20211119
# Fri, 19 Nov 2021 21:21:29 GMT
ARG ODOO_SHA=815580db210a2250b1c2b4f80a22c279892030d9
# Fri, 19 Nov 2021 21:22:41 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=815580db210a2250b1c2b4f80a22c279892030d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Nov 2021 21:22:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Nov 2021 21:22:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Nov 2021 21:22:46 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=815580db210a2250b1c2b4f80a22c279892030d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Nov 2021 21:22:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Nov 2021 21:22:47 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Nov 2021 21:22:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Nov 2021 21:22:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Nov 2021 21:22:47 GMT
USER odoo
# Fri, 19 Nov 2021 21:22:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 21:22:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9050a25a2e7fc15bfb237c584e249e35ad1a86ce1d54a161a0ff988ac8a05b`  
		Last Modified: Wed, 17 Nov 2021 09:21:44 GMT  
		Size: 213.2 MB (213173458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35caad2bee1ae3832c799d895b217edd464b38ab7eab3b3bd4112a0ac8023dfa`  
		Last Modified: Wed, 17 Nov 2021 09:21:06 GMT  
		Size: 13.4 MB (13436595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827e676672899dc5c1f50f0b67069ce37431c5177ff11d52b931dbac889f0792`  
		Last Modified: Wed, 17 Nov 2021 09:21:00 GMT  
		Size: 730.9 KB (730870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5f4eb92977b1eb12ec3bb115a343dd2eaddf33107d71f73156f5161bf2537c`  
		Last Modified: Fri, 19 Nov 2021 21:25:43 GMT  
		Size: 274.0 MB (273979295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9655513fec818ba01c0e4313b8540289ea11eaaddc3a357995f152617fb2ab`  
		Last Modified: Fri, 19 Nov 2021 21:25:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd2b62b0ddfdbd71f471f64863f9d05d5c6c382b5dc1ad7b60d39b38708d7de`  
		Last Modified: Fri, 19 Nov 2021 21:25:12 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a9a9ba731c27b698889aae55a48d00a6a9d8d4b72befa6ed72c62ff4480c4`  
		Last Modified: Fri, 19 Nov 2021 21:25:12 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b90ffd7cb4933f40f0361b36c000446e8fedc9efd08ca5067829eca457872b1`  
		Last Modified: Fri, 19 Nov 2021 21:25:12 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:00a392fe72660b53414db4f38a9757e98842f3b4f4f006ba1a368ce7a7bf2816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:1d2acb5e45b9c68d6299e954611da23a786ca1be6297374f5b098de1c753eeb9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528476353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838a12c11c3af3fb7a88b62ab57ddc7b0a038d1a1607e91a06757715aacee090`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:13:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Nov 2021 09:13:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Nov 2021 09:13:18 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:14:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Nov 2021 09:14:41 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:14:45 GMT
RUN npm install -g rtlcss
# Wed, 17 Nov 2021 09:14:45 GMT
ENV ODOO_VERSION=14.0
# Fri, 19 Nov 2021 21:21:29 GMT
ARG ODOO_RELEASE=20211119
# Fri, 19 Nov 2021 21:21:29 GMT
ARG ODOO_SHA=815580db210a2250b1c2b4f80a22c279892030d9
# Fri, 19 Nov 2021 21:22:41 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=815580db210a2250b1c2b4f80a22c279892030d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Nov 2021 21:22:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Nov 2021 21:22:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Nov 2021 21:22:46 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=815580db210a2250b1c2b4f80a22c279892030d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Nov 2021 21:22:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Nov 2021 21:22:47 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Nov 2021 21:22:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Nov 2021 21:22:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Nov 2021 21:22:47 GMT
USER odoo
# Fri, 19 Nov 2021 21:22:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 21:22:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9050a25a2e7fc15bfb237c584e249e35ad1a86ce1d54a161a0ff988ac8a05b`  
		Last Modified: Wed, 17 Nov 2021 09:21:44 GMT  
		Size: 213.2 MB (213173458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35caad2bee1ae3832c799d895b217edd464b38ab7eab3b3bd4112a0ac8023dfa`  
		Last Modified: Wed, 17 Nov 2021 09:21:06 GMT  
		Size: 13.4 MB (13436595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827e676672899dc5c1f50f0b67069ce37431c5177ff11d52b931dbac889f0792`  
		Last Modified: Wed, 17 Nov 2021 09:21:00 GMT  
		Size: 730.9 KB (730870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5f4eb92977b1eb12ec3bb115a343dd2eaddf33107d71f73156f5161bf2537c`  
		Last Modified: Fri, 19 Nov 2021 21:25:43 GMT  
		Size: 274.0 MB (273979295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9655513fec818ba01c0e4313b8540289ea11eaaddc3a357995f152617fb2ab`  
		Last Modified: Fri, 19 Nov 2021 21:25:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd2b62b0ddfdbd71f471f64863f9d05d5c6c382b5dc1ad7b60d39b38708d7de`  
		Last Modified: Fri, 19 Nov 2021 21:25:12 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a9a9ba731c27b698889aae55a48d00a6a9d8d4b72befa6ed72c62ff4480c4`  
		Last Modified: Fri, 19 Nov 2021 21:25:12 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b90ffd7cb4933f40f0361b36c000446e8fedc9efd08ca5067829eca457872b1`  
		Last Modified: Fri, 19 Nov 2021 21:25:12 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:736d410197cb100640b709a3058076fe7ac699c5a1594229c4079437736c4da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:66206450e7e099006be4654c11f7221215a0f2f58752970e5ff5a9ff875c77e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.6 MB (543620513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd1d3fdb0cb60b575c5151166e3707e773436922677c3d169a61fee0eba853a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:10:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Nov 2021 09:10:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Nov 2021 09:10:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:11:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Nov 2021 09:11:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:11:39 GMT
RUN npm install -g rtlcss
# Wed, 17 Nov 2021 09:11:39 GMT
ENV ODOO_VERSION=15.0
# Fri, 19 Nov 2021 21:19:51 GMT
ARG ODOO_RELEASE=20211119
# Fri, 19 Nov 2021 21:19:51 GMT
ARG ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
# Fri, 19 Nov 2021 21:21:07 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Nov 2021 21:21:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Nov 2021 21:21:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Nov 2021 21:21:12 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Nov 2021 21:21:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Nov 2021 21:21:13 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Nov 2021 21:21:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Nov 2021 21:21:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Nov 2021 21:21:13 GMT
USER odoo
# Fri, 19 Nov 2021 21:21:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 21:21:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9400c757421e2063937e8b190c956fdda2687c92c013b5eff83fe1c61c0c2c8f`  
		Last Modified: Wed, 17 Nov 2021 09:20:38 GMT  
		Size: 220.3 MB (220291328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d1a3d79ceb0d2f1f442648da0e6ece72782b8656e052f0867231839dd0b0`  
		Last Modified: Wed, 17 Nov 2021 09:19:52 GMT  
		Size: 2.5 MB (2506093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9605eabe13664e4a62ea8056b48e7547ab78dad77c977652bc44a6e8e1e30d0`  
		Last Modified: Wed, 17 Nov 2021 09:19:51 GMT  
		Size: 724.5 KB (724479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b2a2b4cb7c943436d010061509f9e829f1d2b3a126693a51d6278e8c9e6a09`  
		Last Modified: Fri, 19 Nov 2021 21:24:58 GMT  
		Size: 288.7 MB (288725881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a504116b95e7a61b0655c01aa36fe96f4fa88fc75405158f0f93a7fbbdb2ac1`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7082a4e0e2488274559e0217b2fbe37407bf2fd954ef036385a0317c5dfb2691`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d675b10459be646feabe781878354971c3e484d3c0786c1abbd9104a834abc3f`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9128e3ab01360f00ee5f7d9ae23339f7a9e2330af685b34c94430189ec992bc2`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:736d410197cb100640b709a3058076fe7ac699c5a1594229c4079437736c4da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:66206450e7e099006be4654c11f7221215a0f2f58752970e5ff5a9ff875c77e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.6 MB (543620513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd1d3fdb0cb60b575c5151166e3707e773436922677c3d169a61fee0eba853a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:10:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Nov 2021 09:10:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Nov 2021 09:10:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:11:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Nov 2021 09:11:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:11:39 GMT
RUN npm install -g rtlcss
# Wed, 17 Nov 2021 09:11:39 GMT
ENV ODOO_VERSION=15.0
# Fri, 19 Nov 2021 21:19:51 GMT
ARG ODOO_RELEASE=20211119
# Fri, 19 Nov 2021 21:19:51 GMT
ARG ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
# Fri, 19 Nov 2021 21:21:07 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Nov 2021 21:21:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Nov 2021 21:21:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Nov 2021 21:21:12 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Nov 2021 21:21:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Nov 2021 21:21:13 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Nov 2021 21:21:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Nov 2021 21:21:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Nov 2021 21:21:13 GMT
USER odoo
# Fri, 19 Nov 2021 21:21:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 21:21:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9400c757421e2063937e8b190c956fdda2687c92c013b5eff83fe1c61c0c2c8f`  
		Last Modified: Wed, 17 Nov 2021 09:20:38 GMT  
		Size: 220.3 MB (220291328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d1a3d79ceb0d2f1f442648da0e6ece72782b8656e052f0867231839dd0b0`  
		Last Modified: Wed, 17 Nov 2021 09:19:52 GMT  
		Size: 2.5 MB (2506093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9605eabe13664e4a62ea8056b48e7547ab78dad77c977652bc44a6e8e1e30d0`  
		Last Modified: Wed, 17 Nov 2021 09:19:51 GMT  
		Size: 724.5 KB (724479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b2a2b4cb7c943436d010061509f9e829f1d2b3a126693a51d6278e8c9e6a09`  
		Last Modified: Fri, 19 Nov 2021 21:24:58 GMT  
		Size: 288.7 MB (288725881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a504116b95e7a61b0655c01aa36fe96f4fa88fc75405158f0f93a7fbbdb2ac1`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7082a4e0e2488274559e0217b2fbe37407bf2fd954ef036385a0317c5dfb2691`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d675b10459be646feabe781878354971c3e484d3c0786c1abbd9104a834abc3f`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9128e3ab01360f00ee5f7d9ae23339f7a9e2330af685b34c94430189ec992bc2`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:736d410197cb100640b709a3058076fe7ac699c5a1594229c4079437736c4da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:66206450e7e099006be4654c11f7221215a0f2f58752970e5ff5a9ff875c77e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.6 MB (543620513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd1d3fdb0cb60b575c5151166e3707e773436922677c3d169a61fee0eba853a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:10:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Nov 2021 09:10:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Nov 2021 09:10:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:11:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Nov 2021 09:11:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:11:39 GMT
RUN npm install -g rtlcss
# Wed, 17 Nov 2021 09:11:39 GMT
ENV ODOO_VERSION=15.0
# Fri, 19 Nov 2021 21:19:51 GMT
ARG ODOO_RELEASE=20211119
# Fri, 19 Nov 2021 21:19:51 GMT
ARG ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
# Fri, 19 Nov 2021 21:21:07 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Nov 2021 21:21:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Nov 2021 21:21:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Nov 2021 21:21:12 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Nov 2021 21:21:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Nov 2021 21:21:13 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Nov 2021 21:21:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Nov 2021 21:21:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Nov 2021 21:21:13 GMT
USER odoo
# Fri, 19 Nov 2021 21:21:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 21:21:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9400c757421e2063937e8b190c956fdda2687c92c013b5eff83fe1c61c0c2c8f`  
		Last Modified: Wed, 17 Nov 2021 09:20:38 GMT  
		Size: 220.3 MB (220291328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d1a3d79ceb0d2f1f442648da0e6ece72782b8656e052f0867231839dd0b0`  
		Last Modified: Wed, 17 Nov 2021 09:19:52 GMT  
		Size: 2.5 MB (2506093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9605eabe13664e4a62ea8056b48e7547ab78dad77c977652bc44a6e8e1e30d0`  
		Last Modified: Wed, 17 Nov 2021 09:19:51 GMT  
		Size: 724.5 KB (724479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b2a2b4cb7c943436d010061509f9e829f1d2b3a126693a51d6278e8c9e6a09`  
		Last Modified: Fri, 19 Nov 2021 21:24:58 GMT  
		Size: 288.7 MB (288725881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a504116b95e7a61b0655c01aa36fe96f4fa88fc75405158f0f93a7fbbdb2ac1`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7082a4e0e2488274559e0217b2fbe37407bf2fd954ef036385a0317c5dfb2691`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d675b10459be646feabe781878354971c3e484d3c0786c1abbd9104a834abc3f`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9128e3ab01360f00ee5f7d9ae23339f7a9e2330af685b34c94430189ec992bc2`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
