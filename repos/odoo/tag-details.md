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
$ docker pull odoo@sha256:bd1ec7b26190e6597444e220fab1b51ce3ce7021cca716ab8627db78deb054e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:3802771b68ccc065e46a1c8346cb063cad5e6b0f9668ea0c4b5e9d93e2a7bee0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539638393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905e559f9b460677a8054077ca89db6641bb08782dfd0875fd48a67398db27dd`
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
# Thu, 02 Dec 2021 02:03:11 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 02:03:11 GMT
ARG ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
# Thu, 02 Dec 2021 02:04:32 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 02:04:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 02:04:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 02:04:36 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 02:04:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 02:04:37 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 02:04:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 02:04:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 02:04:38 GMT
USER odoo
# Thu, 02 Dec 2021 02:04:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 02:04:38 GMT
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
	-	`sha256:8dd95cf864b3917c4a1421a01cfeb5949d3beabc509c328e0692f95689bcec68`  
		Last Modified: Thu, 02 Dec 2021 02:07:03 GMT  
		Size: 291.2 MB (291186239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83048ff6aa1d1b35a78bd0ee1118720e2630224db53478264ac3d8a08a0cd5dc`  
		Last Modified: Thu, 02 Dec 2021 02:06:32 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d72790d0160bf88b678e34934add970b927cee2850e70b4b99281abd93fd465`  
		Last Modified: Thu, 02 Dec 2021 02:06:32 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abde5a6a66c9fb8beccfbc36654551ad64c4cb0b64c1a2fae1c1ba7f969e74e`  
		Last Modified: Thu, 02 Dec 2021 02:06:32 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0b7e088c249b25272474ed612be0ee2ac204b52ca5cce94646d2d14c96e0f3`  
		Last Modified: Thu, 02 Dec 2021 02:06:32 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:bd1ec7b26190e6597444e220fab1b51ce3ce7021cca716ab8627db78deb054e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:3802771b68ccc065e46a1c8346cb063cad5e6b0f9668ea0c4b5e9d93e2a7bee0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539638393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905e559f9b460677a8054077ca89db6641bb08782dfd0875fd48a67398db27dd`
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
# Thu, 02 Dec 2021 02:03:11 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 02:03:11 GMT
ARG ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
# Thu, 02 Dec 2021 02:04:32 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 02:04:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 02:04:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 02:04:36 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 02:04:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 02:04:37 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 02:04:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 02:04:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 02:04:38 GMT
USER odoo
# Thu, 02 Dec 2021 02:04:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 02:04:38 GMT
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
	-	`sha256:8dd95cf864b3917c4a1421a01cfeb5949d3beabc509c328e0692f95689bcec68`  
		Last Modified: Thu, 02 Dec 2021 02:07:03 GMT  
		Size: 291.2 MB (291186239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83048ff6aa1d1b35a78bd0ee1118720e2630224db53478264ac3d8a08a0cd5dc`  
		Last Modified: Thu, 02 Dec 2021 02:06:32 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d72790d0160bf88b678e34934add970b927cee2850e70b4b99281abd93fd465`  
		Last Modified: Thu, 02 Dec 2021 02:06:32 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abde5a6a66c9fb8beccfbc36654551ad64c4cb0b64c1a2fae1c1ba7f969e74e`  
		Last Modified: Thu, 02 Dec 2021 02:06:32 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0b7e088c249b25272474ed612be0ee2ac204b52ca5cce94646d2d14c96e0f3`  
		Last Modified: Thu, 02 Dec 2021 02:06:32 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:7014c2a40aa749c872a2a3d120f050d3f5c889b6b1eea7fc82582e1c4c324bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:019578f0cf85dab750aa0fc71d4bab08968c610e249bd21af7f733f4cb6ee728
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529274436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1977f3ec38042808ea5500aac576f70c78be681749e0ba0238113ed8b9ca8b6a`
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
# Thu, 02 Dec 2021 02:01:33 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 02:01:34 GMT
ARG ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
# Thu, 02 Dec 2021 02:02:58 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 02:03:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 02:03:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 02:03:03 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 02:03:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 02:03:04 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 02:03:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 02:03:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 02:03:04 GMT
USER odoo
# Thu, 02 Dec 2021 02:03:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 02:03:05 GMT
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
	-	`sha256:dd48c5b4aa35312d79d8f5d283948d7e1e23c1c2e78244c82ad569a59122c83d`  
		Last Modified: Thu, 02 Dec 2021 02:06:22 GMT  
		Size: 274.8 MB (274777378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebce0fa72812dba5b5a411e10e069f8b1bf3b9d6bdc6017e6db175882340633e`  
		Last Modified: Thu, 02 Dec 2021 02:05:50 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f088ba011e58558059b14d289605fbf0fd231154a85cfe938b9d603135e23555`  
		Last Modified: Thu, 02 Dec 2021 02:05:50 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2166d9d944b491c22ee053a173549ead1157f3f7707141f724cf96ba58c6754a`  
		Last Modified: Thu, 02 Dec 2021 02:05:50 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20213171a139f589ec4ee0b01457955fb7c90ec53972fdacf724369d2c2d0bd`  
		Last Modified: Thu, 02 Dec 2021 02:05:50 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:7014c2a40aa749c872a2a3d120f050d3f5c889b6b1eea7fc82582e1c4c324bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:019578f0cf85dab750aa0fc71d4bab08968c610e249bd21af7f733f4cb6ee728
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529274436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1977f3ec38042808ea5500aac576f70c78be681749e0ba0238113ed8b9ca8b6a`
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
# Thu, 02 Dec 2021 02:01:33 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 02:01:34 GMT
ARG ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
# Thu, 02 Dec 2021 02:02:58 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 02:03:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 02:03:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 02:03:03 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 02:03:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 02:03:04 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 02:03:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 02:03:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 02:03:04 GMT
USER odoo
# Thu, 02 Dec 2021 02:03:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 02:03:05 GMT
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
	-	`sha256:dd48c5b4aa35312d79d8f5d283948d7e1e23c1c2e78244c82ad569a59122c83d`  
		Last Modified: Thu, 02 Dec 2021 02:06:22 GMT  
		Size: 274.8 MB (274777378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebce0fa72812dba5b5a411e10e069f8b1bf3b9d6bdc6017e6db175882340633e`  
		Last Modified: Thu, 02 Dec 2021 02:05:50 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f088ba011e58558059b14d289605fbf0fd231154a85cfe938b9d603135e23555`  
		Last Modified: Thu, 02 Dec 2021 02:05:50 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2166d9d944b491c22ee053a173549ead1157f3f7707141f724cf96ba58c6754a`  
		Last Modified: Thu, 02 Dec 2021 02:05:50 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20213171a139f589ec4ee0b01457955fb7c90ec53972fdacf724369d2c2d0bd`  
		Last Modified: Thu, 02 Dec 2021 02:05:50 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:8ec96bd8559e83fe003a216b4dd6ef49546a85b2c78d2dad9e92f850d34b80bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:fa320f11b5924cfcecc58226639a43b8ffcbb8a00ae448ffa5b0ecceb43dffba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546324416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5646c5d94d0de3107c5e321ba30631e3287291ece61f1558d93a24cfd41af10c`
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
# Thu, 02 Dec 2021 01:59:55 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 01:59:56 GMT
ARG ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
# Thu, 02 Dec 2021 02:01:16 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 02:01:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 02:01:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 02:01:22 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 02:01:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 02:01:22 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 02:01:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 02:01:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 02:01:23 GMT
USER odoo
# Thu, 02 Dec 2021 02:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 02:01:23 GMT
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
	-	`sha256:7ee0b1bd513bbc9b878db73bd012250e519cda964c8a1749cf3360a9347b44a7`  
		Last Modified: Thu, 02 Dec 2021 02:05:37 GMT  
		Size: 291.4 MB (291429788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace20f6a532415956863a4a803f8a562f907d26547a9a98acfaeb9b551871cec`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa763ba23682a745126c6dcafecfa139e435fce23a668ae8bb23d30e6b05e1`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246c8348bd558ab323038bbf240e76b7566f2336a212864fd4b6a6934d95e943`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d9ed61e4d29eb64d7f0be5941c9c2abebdcccf6ccf3097f016b3b59ab5e59`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:8ec96bd8559e83fe003a216b4dd6ef49546a85b2c78d2dad9e92f850d34b80bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:fa320f11b5924cfcecc58226639a43b8ffcbb8a00ae448ffa5b0ecceb43dffba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546324416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5646c5d94d0de3107c5e321ba30631e3287291ece61f1558d93a24cfd41af10c`
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
# Thu, 02 Dec 2021 01:59:55 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 01:59:56 GMT
ARG ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
# Thu, 02 Dec 2021 02:01:16 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 02:01:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 02:01:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 02:01:22 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 02:01:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 02:01:22 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 02:01:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 02:01:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 02:01:23 GMT
USER odoo
# Thu, 02 Dec 2021 02:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 02:01:23 GMT
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
	-	`sha256:7ee0b1bd513bbc9b878db73bd012250e519cda964c8a1749cf3360a9347b44a7`  
		Last Modified: Thu, 02 Dec 2021 02:05:37 GMT  
		Size: 291.4 MB (291429788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace20f6a532415956863a4a803f8a562f907d26547a9a98acfaeb9b551871cec`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa763ba23682a745126c6dcafecfa139e435fce23a668ae8bb23d30e6b05e1`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246c8348bd558ab323038bbf240e76b7566f2336a212864fd4b6a6934d95e943`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d9ed61e4d29eb64d7f0be5941c9c2abebdcccf6ccf3097f016b3b59ab5e59`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:8ec96bd8559e83fe003a216b4dd6ef49546a85b2c78d2dad9e92f850d34b80bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:fa320f11b5924cfcecc58226639a43b8ffcbb8a00ae448ffa5b0ecceb43dffba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546324416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5646c5d94d0de3107c5e321ba30631e3287291ece61f1558d93a24cfd41af10c`
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
# Thu, 02 Dec 2021 01:59:55 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 01:59:56 GMT
ARG ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
# Thu, 02 Dec 2021 02:01:16 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 02:01:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 02:01:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 02:01:22 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 02:01:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 02:01:22 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 02:01:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 02:01:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 02:01:23 GMT
USER odoo
# Thu, 02 Dec 2021 02:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 02:01:23 GMT
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
	-	`sha256:7ee0b1bd513bbc9b878db73bd012250e519cda964c8a1749cf3360a9347b44a7`  
		Last Modified: Thu, 02 Dec 2021 02:05:37 GMT  
		Size: 291.4 MB (291429788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace20f6a532415956863a4a803f8a562f907d26547a9a98acfaeb9b551871cec`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa763ba23682a745126c6dcafecfa139e435fce23a668ae8bb23d30e6b05e1`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246c8348bd558ab323038bbf240e76b7566f2336a212864fd4b6a6934d95e943`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d9ed61e4d29eb64d7f0be5941c9c2abebdcccf6ccf3097f016b3b59ab5e59`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
