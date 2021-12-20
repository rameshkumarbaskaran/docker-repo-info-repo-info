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
$ docker pull odoo@sha256:3547a8f7f7f3d2cbd5aedcb4accd4a0aff23493266754d8f358a984d53b7e128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:c8da4a85cb4c11db2d7cf328c7f13fcd73056e621253455c5ed07cc98d4791b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.4 MB (539398252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29ee44761b6af1b2a810ff82eebd24137d4cc7f7e12f2d8fe517341026a93e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:24:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:24:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:24:45 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:29:05 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:29:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:29:34 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:29:34 GMT
ENV ODOO_VERSION=13.0
# Mon, 20 Dec 2021 18:44:39 GMT
ARG ODOO_RELEASE=20211220
# Mon, 20 Dec 2021 18:44:39 GMT
ARG ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
# Mon, 20 Dec 2021 18:45:56 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 20 Dec 2021 18:46:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 20 Dec 2021 18:46:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 20 Dec 2021 18:46:01 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 20 Dec 2021 18:46:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 20 Dec 2021 18:46:02 GMT
EXPOSE 8069 8071 8072
# Mon, 20 Dec 2021 18:46:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 20 Dec 2021 18:46:02 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 20 Dec 2021 18:46:02 GMT
USER odoo
# Mon, 20 Dec 2021 18:46:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 18:46:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8988f86f949d08f5ea393c3cb9d4016acd45699f4fb9c3b6a78c8b107d9be55`  
		Last Modified: Thu, 02 Dec 2021 03:34:31 GMT  
		Size: 207.1 MB (207130653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78dd91afcfb205b31d583947328c09101f9c1a292ee4ab5357b9cc5c12a691c`  
		Last Modified: Thu, 02 Dec 2021 03:33:57 GMT  
		Size: 13.4 MB (13434259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875e5005d33be86db39c7b664080d0b957d3d88521bd5d30b592382eddeea0e`  
		Last Modified: Thu, 02 Dec 2021 03:33:52 GMT  
		Size: 425.0 KB (424962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306cbcc17abae5ee19cb26194c3ff0d38d66bde1486d87094944d108e6728cf3`  
		Last Modified: Mon, 20 Dec 2021 18:48:27 GMT  
		Size: 291.3 MB (291252185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb5a1020a66555ae93e758e7a5281a6736b2511d3f25901bb89b030a6ff2b6f`  
		Last Modified: Mon, 20 Dec 2021 18:47:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9450bee4c1751a3d8787ec5f615dc30e8f3659b3d5b433c03ca462f0e6f250`  
		Last Modified: Mon, 20 Dec 2021 18:47:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a0b76420a1e50dbe34616fbcaf6123959e5a94749c9f26c57a918a38976434`  
		Last Modified: Mon, 20 Dec 2021 18:47:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1fe5078118e3dcbc8ebe248f3b13d4e996a7fdad83a97e098ac1cf6c4d554d`  
		Last Modified: Mon, 20 Dec 2021 18:47:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:3547a8f7f7f3d2cbd5aedcb4accd4a0aff23493266754d8f358a984d53b7e128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:c8da4a85cb4c11db2d7cf328c7f13fcd73056e621253455c5ed07cc98d4791b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.4 MB (539398252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29ee44761b6af1b2a810ff82eebd24137d4cc7f7e12f2d8fe517341026a93e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:24:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:24:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:24:45 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:29:05 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:29:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:29:34 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:29:34 GMT
ENV ODOO_VERSION=13.0
# Mon, 20 Dec 2021 18:44:39 GMT
ARG ODOO_RELEASE=20211220
# Mon, 20 Dec 2021 18:44:39 GMT
ARG ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
# Mon, 20 Dec 2021 18:45:56 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 20 Dec 2021 18:46:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 20 Dec 2021 18:46:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 20 Dec 2021 18:46:01 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 20 Dec 2021 18:46:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 20 Dec 2021 18:46:02 GMT
EXPOSE 8069 8071 8072
# Mon, 20 Dec 2021 18:46:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 20 Dec 2021 18:46:02 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 20 Dec 2021 18:46:02 GMT
USER odoo
# Mon, 20 Dec 2021 18:46:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 18:46:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8988f86f949d08f5ea393c3cb9d4016acd45699f4fb9c3b6a78c8b107d9be55`  
		Last Modified: Thu, 02 Dec 2021 03:34:31 GMT  
		Size: 207.1 MB (207130653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78dd91afcfb205b31d583947328c09101f9c1a292ee4ab5357b9cc5c12a691c`  
		Last Modified: Thu, 02 Dec 2021 03:33:57 GMT  
		Size: 13.4 MB (13434259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875e5005d33be86db39c7b664080d0b957d3d88521bd5d30b592382eddeea0e`  
		Last Modified: Thu, 02 Dec 2021 03:33:52 GMT  
		Size: 425.0 KB (424962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306cbcc17abae5ee19cb26194c3ff0d38d66bde1486d87094944d108e6728cf3`  
		Last Modified: Mon, 20 Dec 2021 18:48:27 GMT  
		Size: 291.3 MB (291252185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb5a1020a66555ae93e758e7a5281a6736b2511d3f25901bb89b030a6ff2b6f`  
		Last Modified: Mon, 20 Dec 2021 18:47:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9450bee4c1751a3d8787ec5f615dc30e8f3659b3d5b433c03ca462f0e6f250`  
		Last Modified: Mon, 20 Dec 2021 18:47:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a0b76420a1e50dbe34616fbcaf6123959e5a94749c9f26c57a918a38976434`  
		Last Modified: Mon, 20 Dec 2021 18:47:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1fe5078118e3dcbc8ebe248f3b13d4e996a7fdad83a97e098ac1cf6c4d554d`  
		Last Modified: Mon, 20 Dec 2021 18:47:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:5e7c876b0085deaf26c18aecefd1b9c7db03b3f5bec125fb8ab90c6c3f450163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:f646f3976c1c51857a83e04a38960faf823da710c52a20e0d7dcd0c1ba8c90dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.1 MB (529135118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a372eac7bf79507a684afa96fe2f16ae23901ff378db4d2e31f3a0001bcbbcf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:24:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:24:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:24:45 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:26:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:26:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:26:27 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:26:27 GMT
ENV ODOO_VERSION=14.0
# Mon, 20 Dec 2021 18:43:16 GMT
ARG ODOO_RELEASE=20211220
# Mon, 20 Dec 2021 18:43:17 GMT
ARG ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
# Mon, 20 Dec 2021 18:44:29 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 20 Dec 2021 18:44:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 20 Dec 2021 18:44:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 20 Dec 2021 18:44:34 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 20 Dec 2021 18:44:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 20 Dec 2021 18:44:34 GMT
EXPOSE 8069 8071 8072
# Mon, 20 Dec 2021 18:44:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 20 Dec 2021 18:44:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 20 Dec 2021 18:44:35 GMT
USER odoo
# Mon, 20 Dec 2021 18:44:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 18:44:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc20adace522abb201c7423e22fd72bcb79776eea50c16f27d7304e0ef69a17`  
		Last Modified: Thu, 02 Dec 2021 03:33:31 GMT  
		Size: 213.2 MB (213172687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1864e4021f806774779a9ca1a51ef676584c0ebfe979b016930caa5019dbebe2`  
		Last Modified: Thu, 02 Dec 2021 03:32:56 GMT  
		Size: 13.4 MB (13436533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c504b4f0face0abb0105469a79f865565c73340c11e0eb38cf2f615bd7f3ff60`  
		Last Modified: Thu, 02 Dec 2021 03:32:52 GMT  
		Size: 424.9 KB (424854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc57b4a5e6880068eee09971b3b520d5bafe04d58df6e3c6668620581a311`  
		Last Modified: Mon, 20 Dec 2021 18:47:46 GMT  
		Size: 274.9 MB (274944850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d070e0a87bd0e55e6a4930fab12c291f3b6992f6ab540bb54979d890f054641`  
		Last Modified: Mon, 20 Dec 2021 18:47:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43f629cb74053204ef2c575b79fd7967a8c67538b9beb895e7c9c03ded42398`  
		Last Modified: Mon, 20 Dec 2021 18:47:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b92047de3f592ccd6a2a27a59e1d1f3ef6231e5e6681646cfea9e715be2e17`  
		Last Modified: Mon, 20 Dec 2021 18:47:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35430b16ff4267af3ffcf80af757b479eb2f7a294c04e68e50aad264ffc3ad16`  
		Last Modified: Mon, 20 Dec 2021 18:47:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:5e7c876b0085deaf26c18aecefd1b9c7db03b3f5bec125fb8ab90c6c3f450163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:f646f3976c1c51857a83e04a38960faf823da710c52a20e0d7dcd0c1ba8c90dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.1 MB (529135118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a372eac7bf79507a684afa96fe2f16ae23901ff378db4d2e31f3a0001bcbbcf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:24:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:24:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:24:45 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:26:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:26:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:26:27 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:26:27 GMT
ENV ODOO_VERSION=14.0
# Mon, 20 Dec 2021 18:43:16 GMT
ARG ODOO_RELEASE=20211220
# Mon, 20 Dec 2021 18:43:17 GMT
ARG ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
# Mon, 20 Dec 2021 18:44:29 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 20 Dec 2021 18:44:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 20 Dec 2021 18:44:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 20 Dec 2021 18:44:34 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 20 Dec 2021 18:44:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 20 Dec 2021 18:44:34 GMT
EXPOSE 8069 8071 8072
# Mon, 20 Dec 2021 18:44:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 20 Dec 2021 18:44:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 20 Dec 2021 18:44:35 GMT
USER odoo
# Mon, 20 Dec 2021 18:44:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 18:44:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc20adace522abb201c7423e22fd72bcb79776eea50c16f27d7304e0ef69a17`  
		Last Modified: Thu, 02 Dec 2021 03:33:31 GMT  
		Size: 213.2 MB (213172687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1864e4021f806774779a9ca1a51ef676584c0ebfe979b016930caa5019dbebe2`  
		Last Modified: Thu, 02 Dec 2021 03:32:56 GMT  
		Size: 13.4 MB (13436533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c504b4f0face0abb0105469a79f865565c73340c11e0eb38cf2f615bd7f3ff60`  
		Last Modified: Thu, 02 Dec 2021 03:32:52 GMT  
		Size: 424.9 KB (424854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc57b4a5e6880068eee09971b3b520d5bafe04d58df6e3c6668620581a311`  
		Last Modified: Mon, 20 Dec 2021 18:47:46 GMT  
		Size: 274.9 MB (274944850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d070e0a87bd0e55e6a4930fab12c291f3b6992f6ab540bb54979d890f054641`  
		Last Modified: Mon, 20 Dec 2021 18:47:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43f629cb74053204ef2c575b79fd7967a8c67538b9beb895e7c9c03ded42398`  
		Last Modified: Mon, 20 Dec 2021 18:47:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b92047de3f592ccd6a2a27a59e1d1f3ef6231e5e6681646cfea9e715be2e17`  
		Last Modified: Mon, 20 Dec 2021 18:47:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35430b16ff4267af3ffcf80af757b479eb2f7a294c04e68e50aad264ffc3ad16`  
		Last Modified: Mon, 20 Dec 2021 18:47:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:fdeb9c908208a5264a63b3a10af81cfa3f72846d3d66e09bb408ca5a0c5e823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:b130f5076d19102ac6145d1f4ee592808ba321243b0f6dd6cd7162e663040ae3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.4 MB (546374022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd776d1a62ba310bce6f9a2e641bf0c39ce5e3d707e9f0ebb2a0ec7e40f3cd54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:21:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:21:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:21:37 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:22:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:23:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:23:04 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:23:04 GMT
ENV ODOO_VERSION=15.0
# Mon, 20 Dec 2021 18:41:39 GMT
ARG ODOO_RELEASE=20211220
# Mon, 20 Dec 2021 18:41:39 GMT
ARG ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
# Mon, 20 Dec 2021 18:42:57 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 20 Dec 2021 18:43:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 20 Dec 2021 18:43:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 20 Dec 2021 18:43:02 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 20 Dec 2021 18:43:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 20 Dec 2021 18:43:02 GMT
EXPOSE 8069 8071 8072
# Mon, 20 Dec 2021 18:43:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 20 Dec 2021 18:43:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 20 Dec 2021 18:43:03 GMT
USER odoo
# Mon, 20 Dec 2021 18:43:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 18:43:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8928362baaf188d2d35b07907f7df5a83838f416511d7c90d1001f0f69b22d`  
		Last Modified: Thu, 02 Dec 2021 03:32:31 GMT  
		Size: 220.3 MB (220290298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1196c36b7759c2bc3f823f01785a679ef74915d5281b24e23220cfac4fb643c`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 2.5 MB (2506050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014833e3ecaf723c362d63385e2ff1ece9d0f33f6818690c2ffb8acbbc320186`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 417.8 KB (417795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d94b7f799abd1e6ed0a3b0187568e9e71a1649e8ceaa290d3615370b537012`  
		Last Modified: Mon, 20 Dec 2021 18:47:01 GMT  
		Size: 291.8 MB (291787192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f63b88d6c03cd8dd557f401530f4caac4919b47e19e96cc9260c0fc06ac246b`  
		Last Modified: Mon, 20 Dec 2021 18:46:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e15b3c19fd3b76b1766d90eafa4a9efd07fdacd839387d06b969a6ee7e495`  
		Last Modified: Mon, 20 Dec 2021 18:46:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3402a091a99587b86e7e5f1b0354bc3fdfc7e8dfc72be93f07024f7a35b6f69`  
		Last Modified: Mon, 20 Dec 2021 18:46:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efd8836eb2b0b837c81d2ec615ad9e14e771b71a526e04958113a6726684a5`  
		Last Modified: Mon, 20 Dec 2021 18:46:29 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:fdeb9c908208a5264a63b3a10af81cfa3f72846d3d66e09bb408ca5a0c5e823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:b130f5076d19102ac6145d1f4ee592808ba321243b0f6dd6cd7162e663040ae3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.4 MB (546374022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd776d1a62ba310bce6f9a2e641bf0c39ce5e3d707e9f0ebb2a0ec7e40f3cd54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:21:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:21:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:21:37 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:22:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:23:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:23:04 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:23:04 GMT
ENV ODOO_VERSION=15.0
# Mon, 20 Dec 2021 18:41:39 GMT
ARG ODOO_RELEASE=20211220
# Mon, 20 Dec 2021 18:41:39 GMT
ARG ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
# Mon, 20 Dec 2021 18:42:57 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 20 Dec 2021 18:43:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 20 Dec 2021 18:43:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 20 Dec 2021 18:43:02 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 20 Dec 2021 18:43:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 20 Dec 2021 18:43:02 GMT
EXPOSE 8069 8071 8072
# Mon, 20 Dec 2021 18:43:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 20 Dec 2021 18:43:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 20 Dec 2021 18:43:03 GMT
USER odoo
# Mon, 20 Dec 2021 18:43:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 18:43:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8928362baaf188d2d35b07907f7df5a83838f416511d7c90d1001f0f69b22d`  
		Last Modified: Thu, 02 Dec 2021 03:32:31 GMT  
		Size: 220.3 MB (220290298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1196c36b7759c2bc3f823f01785a679ef74915d5281b24e23220cfac4fb643c`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 2.5 MB (2506050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014833e3ecaf723c362d63385e2ff1ece9d0f33f6818690c2ffb8acbbc320186`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 417.8 KB (417795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d94b7f799abd1e6ed0a3b0187568e9e71a1649e8ceaa290d3615370b537012`  
		Last Modified: Mon, 20 Dec 2021 18:47:01 GMT  
		Size: 291.8 MB (291787192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f63b88d6c03cd8dd557f401530f4caac4919b47e19e96cc9260c0fc06ac246b`  
		Last Modified: Mon, 20 Dec 2021 18:46:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e15b3c19fd3b76b1766d90eafa4a9efd07fdacd839387d06b969a6ee7e495`  
		Last Modified: Mon, 20 Dec 2021 18:46:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3402a091a99587b86e7e5f1b0354bc3fdfc7e8dfc72be93f07024f7a35b6f69`  
		Last Modified: Mon, 20 Dec 2021 18:46:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efd8836eb2b0b837c81d2ec615ad9e14e771b71a526e04958113a6726684a5`  
		Last Modified: Mon, 20 Dec 2021 18:46:29 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:fdeb9c908208a5264a63b3a10af81cfa3f72846d3d66e09bb408ca5a0c5e823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b130f5076d19102ac6145d1f4ee592808ba321243b0f6dd6cd7162e663040ae3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.4 MB (546374022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd776d1a62ba310bce6f9a2e641bf0c39ce5e3d707e9f0ebb2a0ec7e40f3cd54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:21:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:21:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:21:37 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:22:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:23:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:23:04 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:23:04 GMT
ENV ODOO_VERSION=15.0
# Mon, 20 Dec 2021 18:41:39 GMT
ARG ODOO_RELEASE=20211220
# Mon, 20 Dec 2021 18:41:39 GMT
ARG ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
# Mon, 20 Dec 2021 18:42:57 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 20 Dec 2021 18:43:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 20 Dec 2021 18:43:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 20 Dec 2021 18:43:02 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 20 Dec 2021 18:43:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 20 Dec 2021 18:43:02 GMT
EXPOSE 8069 8071 8072
# Mon, 20 Dec 2021 18:43:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 20 Dec 2021 18:43:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 20 Dec 2021 18:43:03 GMT
USER odoo
# Mon, 20 Dec 2021 18:43:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 18:43:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8928362baaf188d2d35b07907f7df5a83838f416511d7c90d1001f0f69b22d`  
		Last Modified: Thu, 02 Dec 2021 03:32:31 GMT  
		Size: 220.3 MB (220290298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1196c36b7759c2bc3f823f01785a679ef74915d5281b24e23220cfac4fb643c`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 2.5 MB (2506050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014833e3ecaf723c362d63385e2ff1ece9d0f33f6818690c2ffb8acbbc320186`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 417.8 KB (417795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d94b7f799abd1e6ed0a3b0187568e9e71a1649e8ceaa290d3615370b537012`  
		Last Modified: Mon, 20 Dec 2021 18:47:01 GMT  
		Size: 291.8 MB (291787192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f63b88d6c03cd8dd557f401530f4caac4919b47e19e96cc9260c0fc06ac246b`  
		Last Modified: Mon, 20 Dec 2021 18:46:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e15b3c19fd3b76b1766d90eafa4a9efd07fdacd839387d06b969a6ee7e495`  
		Last Modified: Mon, 20 Dec 2021 18:46:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3402a091a99587b86e7e5f1b0354bc3fdfc7e8dfc72be93f07024f7a35b6f69`  
		Last Modified: Mon, 20 Dec 2021 18:46:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efd8836eb2b0b837c81d2ec615ad9e14e771b71a526e04958113a6726684a5`  
		Last Modified: Mon, 20 Dec 2021 18:46:29 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
