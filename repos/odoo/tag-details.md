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
$ docker pull odoo@sha256:a10f02515ca701cb2f1b4e659ddfedff288aa142c0c1891ee0a121857f3c35b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:2ec7e16f3e4435d7c7dd189dfd446fd33ffe9933986f5443ca24d3b15a9353ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533090220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41cfbd52add22d545943875f1f2cd8a924751c2154f55b3d4fbf42c507301fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:35 GMT
ADD file:9c8b7c79fbbb19d308d151785d178e19bfa7b83257f38d03fa7f30cd41d58530 in / 
# Thu, 07 Sep 2023 00:21:35 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:26:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Sep 2023 02:26:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Sep 2023 02:26:18 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:27:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 07 Sep 2023 02:27:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:27:48 GMT
RUN npm install -g rtlcss
# Thu, 07 Sep 2023 02:27:48 GMT
ENV ODOO_VERSION=14.0
# Thu, 07 Sep 2023 02:27:49 GMT
ARG ODOO_RELEASE=20230901
# Thu, 07 Sep 2023 02:27:49 GMT
ARG ODOO_SHA=0777c849049f346bb6f3f0eb7d544e9d2960d8d8
# Thu, 07 Sep 2023 02:29:05 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=0777c849049f346bb6f3f0eb7d544e9d2960d8d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 07 Sep 2023 02:29:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 07 Sep 2023 02:29:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 07 Sep 2023 02:29:09 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=0777c849049f346bb6f3f0eb7d544e9d2960d8d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 07 Sep 2023 02:29:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Sep 2023 02:29:09 GMT
EXPOSE 8069 8071 8072
# Thu, 07 Sep 2023 02:29:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Sep 2023 02:29:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 07 Sep 2023 02:29:09 GMT
USER odoo
# Thu, 07 Sep 2023 02:29:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Sep 2023 02:29:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:91f01557fe0da558070d4f24631c94e91a80877a24621b52b8b13009b62d8d96`  
		Last Modified: Thu, 07 Sep 2023 00:26:44 GMT  
		Size: 27.2 MB (27187385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940672322c8453d8f08692d07ca2e5e4ebb1320e1c84350aaabdd24bafce6cb0`  
		Last Modified: Thu, 07 Sep 2023 02:31:20 GMT  
		Size: 213.2 MB (213181707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a05543a28635818dba1cc0ab4d4098637423c0741a6e782b784820618d6d9`  
		Last Modified: Thu, 07 Sep 2023 02:31:00 GMT  
		Size: 13.5 MB (13522728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938de5b6d3ea80d4eac894fafbab9f362a2a851997bf684bf68b776a5062d37a`  
		Last Modified: Thu, 07 Sep 2023 02:30:57 GMT  
		Size: 460.1 KB (460142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4dbd046fd6a8c4693e04acd90aab1f8bc4fa446278a00e8befbed5e192dc51`  
		Last Modified: Thu, 07 Sep 2023 02:31:27 GMT  
		Size: 278.7 MB (278735793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccca2c79a17f53329fea36740ef027d06b3d103851a5765b400f64b75bc1d7aa`  
		Last Modified: Thu, 07 Sep 2023 02:30:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575a239b3408ece9317338a234423e8e5f1ef77c4cbfc48623246134c775e79f`  
		Last Modified: Thu, 07 Sep 2023 02:30:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f99033ec632ea96efea6c9e5dee564f1a6644c830d3594aaef9b9e729c0ab7`  
		Last Modified: Thu, 07 Sep 2023 02:30:55 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59a53944e7cbf53bc28fea470995888dfd7cd816240834bb42ef0d2ea63e1bc`  
		Last Modified: Thu, 07 Sep 2023 02:30:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:a10f02515ca701cb2f1b4e659ddfedff288aa142c0c1891ee0a121857f3c35b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:2ec7e16f3e4435d7c7dd189dfd446fd33ffe9933986f5443ca24d3b15a9353ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533090220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41cfbd52add22d545943875f1f2cd8a924751c2154f55b3d4fbf42c507301fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:35 GMT
ADD file:9c8b7c79fbbb19d308d151785d178e19bfa7b83257f38d03fa7f30cd41d58530 in / 
# Thu, 07 Sep 2023 00:21:35 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:26:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Sep 2023 02:26:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Sep 2023 02:26:18 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:27:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 07 Sep 2023 02:27:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:27:48 GMT
RUN npm install -g rtlcss
# Thu, 07 Sep 2023 02:27:48 GMT
ENV ODOO_VERSION=14.0
# Thu, 07 Sep 2023 02:27:49 GMT
ARG ODOO_RELEASE=20230901
# Thu, 07 Sep 2023 02:27:49 GMT
ARG ODOO_SHA=0777c849049f346bb6f3f0eb7d544e9d2960d8d8
# Thu, 07 Sep 2023 02:29:05 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=0777c849049f346bb6f3f0eb7d544e9d2960d8d8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 07 Sep 2023 02:29:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 07 Sep 2023 02:29:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 07 Sep 2023 02:29:09 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=0777c849049f346bb6f3f0eb7d544e9d2960d8d8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 07 Sep 2023 02:29:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Sep 2023 02:29:09 GMT
EXPOSE 8069 8071 8072
# Thu, 07 Sep 2023 02:29:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Sep 2023 02:29:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 07 Sep 2023 02:29:09 GMT
USER odoo
# Thu, 07 Sep 2023 02:29:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Sep 2023 02:29:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:91f01557fe0da558070d4f24631c94e91a80877a24621b52b8b13009b62d8d96`  
		Last Modified: Thu, 07 Sep 2023 00:26:44 GMT  
		Size: 27.2 MB (27187385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940672322c8453d8f08692d07ca2e5e4ebb1320e1c84350aaabdd24bafce6cb0`  
		Last Modified: Thu, 07 Sep 2023 02:31:20 GMT  
		Size: 213.2 MB (213181707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a05543a28635818dba1cc0ab4d4098637423c0741a6e782b784820618d6d9`  
		Last Modified: Thu, 07 Sep 2023 02:31:00 GMT  
		Size: 13.5 MB (13522728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938de5b6d3ea80d4eac894fafbab9f362a2a851997bf684bf68b776a5062d37a`  
		Last Modified: Thu, 07 Sep 2023 02:30:57 GMT  
		Size: 460.1 KB (460142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4dbd046fd6a8c4693e04acd90aab1f8bc4fa446278a00e8befbed5e192dc51`  
		Last Modified: Thu, 07 Sep 2023 02:31:27 GMT  
		Size: 278.7 MB (278735793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccca2c79a17f53329fea36740ef027d06b3d103851a5765b400f64b75bc1d7aa`  
		Last Modified: Thu, 07 Sep 2023 02:30:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575a239b3408ece9317338a234423e8e5f1ef77c4cbfc48623246134c775e79f`  
		Last Modified: Thu, 07 Sep 2023 02:30:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f99033ec632ea96efea6c9e5dee564f1a6644c830d3594aaef9b9e729c0ab7`  
		Last Modified: Thu, 07 Sep 2023 02:30:55 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59a53944e7cbf53bc28fea470995888dfd7cd816240834bb42ef0d2ea63e1bc`  
		Last Modified: Thu, 07 Sep 2023 02:30:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:06b9335d90e19b4e7460b54feb1ed3f8fadf350d7fe2fbe2c31d71d59728e913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:f070e2d23997bc820f322fd21e05f616e4d1e32e40011cf343fc6e097d2eaf48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.2 MB (562177251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdccb9502d65795a0e26ad9837a4aac8667184b4d595a61136069930408a4d06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:21:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Sep 2023 02:21:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Sep 2023 02:21:01 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:24:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 07 Sep 2023 02:24:51 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:24:53 GMT
RUN npm install -g rtlcss
# Thu, 07 Sep 2023 02:24:53 GMT
ENV ODOO_VERSION=15.0
# Thu, 07 Sep 2023 02:24:53 GMT
ARG ODOO_RELEASE=20230901
# Thu, 07 Sep 2023 02:24:53 GMT
ARG ODOO_SHA=22553b2cb576c94801b6b1180c55e6d6d29de338
# Thu, 07 Sep 2023 02:26:07 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=22553b2cb576c94801b6b1180c55e6d6d29de338
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 07 Sep 2023 02:26:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 07 Sep 2023 02:26:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 07 Sep 2023 02:26:11 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=22553b2cb576c94801b6b1180c55e6d6d29de338
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 07 Sep 2023 02:26:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Sep 2023 02:26:12 GMT
EXPOSE 8069 8071 8072
# Thu, 07 Sep 2023 02:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Sep 2023 02:26:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 07 Sep 2023 02:26:12 GMT
USER odoo
# Thu, 07 Sep 2023 02:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Sep 2023 02:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5d5974a7fe984f9ed75a81bee2adca298a731040afb6f935a1665727b14bec`  
		Last Modified: Thu, 07 Sep 2023 02:30:37 GMT  
		Size: 220.3 MB (220302684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb58d10540b49101750bab050b9d3f58734d7593f35dad8ab4ae9101580de4e`  
		Last Modified: Thu, 07 Sep 2023 02:30:13 GMT  
		Size: 2.6 MB (2576464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7235349850c57657a3c2e0191b357dbebb26946868008648786cb479cd300d00`  
		Last Modified: Thu, 07 Sep 2023 02:30:13 GMT  
		Size: 455.8 KB (455771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e46d5b22e54b77e9c3968fb9743f4ef9b25bc7f63a6defd1cd595793aef3aa`  
		Last Modified: Thu, 07 Sep 2023 02:30:45 GMT  
		Size: 307.4 MB (307422369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6237c485e98396f08982832f38c9748b2722116fea3389cd5b995226cca61958`  
		Last Modified: Thu, 07 Sep 2023 02:30:10 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fc1876afe50e2e9d3f0fb274f80812f9b7b13e334156ac6805c50b0b460f7e`  
		Last Modified: Thu, 07 Sep 2023 02:30:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87a01d2fdba4e00bb12caa0447e4e1c40a2268c1d980f71ac2133c45d7b2555`  
		Last Modified: Thu, 07 Sep 2023 02:30:10 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9af21e5733aa1f18410cd5c1d7f925d6b7dc0161f0248857d65b433a59b06a`  
		Last Modified: Thu, 07 Sep 2023 02:30:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:06b9335d90e19b4e7460b54feb1ed3f8fadf350d7fe2fbe2c31d71d59728e913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:f070e2d23997bc820f322fd21e05f616e4d1e32e40011cf343fc6e097d2eaf48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.2 MB (562177251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdccb9502d65795a0e26ad9837a4aac8667184b4d595a61136069930408a4d06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:21:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Sep 2023 02:21:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Sep 2023 02:21:01 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:24:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 07 Sep 2023 02:24:51 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:24:53 GMT
RUN npm install -g rtlcss
# Thu, 07 Sep 2023 02:24:53 GMT
ENV ODOO_VERSION=15.0
# Thu, 07 Sep 2023 02:24:53 GMT
ARG ODOO_RELEASE=20230901
# Thu, 07 Sep 2023 02:24:53 GMT
ARG ODOO_SHA=22553b2cb576c94801b6b1180c55e6d6d29de338
# Thu, 07 Sep 2023 02:26:07 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=22553b2cb576c94801b6b1180c55e6d6d29de338
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 07 Sep 2023 02:26:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 07 Sep 2023 02:26:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 07 Sep 2023 02:26:11 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=22553b2cb576c94801b6b1180c55e6d6d29de338
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 07 Sep 2023 02:26:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Sep 2023 02:26:12 GMT
EXPOSE 8069 8071 8072
# Thu, 07 Sep 2023 02:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Sep 2023 02:26:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 07 Sep 2023 02:26:12 GMT
USER odoo
# Thu, 07 Sep 2023 02:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Sep 2023 02:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5d5974a7fe984f9ed75a81bee2adca298a731040afb6f935a1665727b14bec`  
		Last Modified: Thu, 07 Sep 2023 02:30:37 GMT  
		Size: 220.3 MB (220302684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb58d10540b49101750bab050b9d3f58734d7593f35dad8ab4ae9101580de4e`  
		Last Modified: Thu, 07 Sep 2023 02:30:13 GMT  
		Size: 2.6 MB (2576464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7235349850c57657a3c2e0191b357dbebb26946868008648786cb479cd300d00`  
		Last Modified: Thu, 07 Sep 2023 02:30:13 GMT  
		Size: 455.8 KB (455771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e46d5b22e54b77e9c3968fb9743f4ef9b25bc7f63a6defd1cd595793aef3aa`  
		Last Modified: Thu, 07 Sep 2023 02:30:45 GMT  
		Size: 307.4 MB (307422369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6237c485e98396f08982832f38c9748b2722116fea3389cd5b995226cca61958`  
		Last Modified: Thu, 07 Sep 2023 02:30:10 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fc1876afe50e2e9d3f0fb274f80812f9b7b13e334156ac6805c50b0b460f7e`  
		Last Modified: Thu, 07 Sep 2023 02:30:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87a01d2fdba4e00bb12caa0447e4e1c40a2268c1d980f71ac2133c45d7b2555`  
		Last Modified: Thu, 07 Sep 2023 02:30:10 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9af21e5733aa1f18410cd5c1d7f925d6b7dc0161f0248857d65b433a59b06a`  
		Last Modified: Thu, 07 Sep 2023 02:30:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:31e089bb7cb5e249ce5b78eb29ab15a14ed32aabef1dc7d8fe14ec85f636d026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:f76d4c4e165b21257b04f392f61a76111f7b3aa9826a2bee2275068683352d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.3 MB (576263613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6800c65be4d3733b1aeb75089fcc8ff8502727aa13f7be93490446f3f0d0502a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:21:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Sep 2023 02:21:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Sep 2023 02:21:01 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:22:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 07 Sep 2023 02:22:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:22:19 GMT
RUN npm install -g rtlcss
# Thu, 07 Sep 2023 02:22:19 GMT
ENV ODOO_VERSION=16.0
# Thu, 07 Sep 2023 02:22:20 GMT
ARG ODOO_RELEASE=20230901
# Thu, 07 Sep 2023 02:22:20 GMT
ARG ODOO_SHA=2287a32457f8d26405b7203820c54dc112a4537d
# Thu, 07 Sep 2023 02:23:41 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=2287a32457f8d26405b7203820c54dc112a4537d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 07 Sep 2023 02:23:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 07 Sep 2023 02:23:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 07 Sep 2023 02:23:46 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=2287a32457f8d26405b7203820c54dc112a4537d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 07 Sep 2023 02:23:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Sep 2023 02:23:46 GMT
EXPOSE 8069 8071 8072
# Thu, 07 Sep 2023 02:23:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Sep 2023 02:23:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 07 Sep 2023 02:23:47 GMT
USER odoo
# Thu, 07 Sep 2023 02:23:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Sep 2023 02:23:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aee24f7779098be746c2ccfd465a71089f8fabdd3871b79af9060fc44a2911b`  
		Last Modified: Thu, 07 Sep 2023 02:29:47 GMT  
		Size: 221.0 MB (220992957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bb15e16ded7af3729af7fcb014075bc7146c328b39adade6d7a98d491b1b28`  
		Last Modified: Thu, 07 Sep 2023 02:29:22 GMT  
		Size: 2.6 MB (2579967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9358b870e15ee771e762346a77778b643846ade6027dab02e21d6024a92eff6`  
		Last Modified: Thu, 07 Sep 2023 02:29:22 GMT  
		Size: 455.7 KB (455729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551234f68e71be923c2c4bc655c255fa6ce8cc730164d6a09ca97ae73170ca45`  
		Last Modified: Thu, 07 Sep 2023 02:29:58 GMT  
		Size: 320.8 MB (320814992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72c7ed9df09ad4eab969b8aa7bc02a47533aed439fcebefbff1f4c1c571a96f`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5260cd37150ba2ec9d2a415e8a0220c168eefe2bcc5d69a13d7f024baecd2ec3`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d63f28df435ef28ec0648a37571f83f2eaa27e8a01604242d99551427940188`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4b5979b281dc33f6d7f9603f4d35323a811f2e45ad08f0b7240238c67b8944`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:31e089bb7cb5e249ce5b78eb29ab15a14ed32aabef1dc7d8fe14ec85f636d026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:f76d4c4e165b21257b04f392f61a76111f7b3aa9826a2bee2275068683352d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.3 MB (576263613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6800c65be4d3733b1aeb75089fcc8ff8502727aa13f7be93490446f3f0d0502a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:21:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Sep 2023 02:21:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Sep 2023 02:21:01 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:22:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 07 Sep 2023 02:22:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:22:19 GMT
RUN npm install -g rtlcss
# Thu, 07 Sep 2023 02:22:19 GMT
ENV ODOO_VERSION=16.0
# Thu, 07 Sep 2023 02:22:20 GMT
ARG ODOO_RELEASE=20230901
# Thu, 07 Sep 2023 02:22:20 GMT
ARG ODOO_SHA=2287a32457f8d26405b7203820c54dc112a4537d
# Thu, 07 Sep 2023 02:23:41 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=2287a32457f8d26405b7203820c54dc112a4537d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 07 Sep 2023 02:23:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 07 Sep 2023 02:23:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 07 Sep 2023 02:23:46 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=2287a32457f8d26405b7203820c54dc112a4537d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 07 Sep 2023 02:23:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Sep 2023 02:23:46 GMT
EXPOSE 8069 8071 8072
# Thu, 07 Sep 2023 02:23:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Sep 2023 02:23:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 07 Sep 2023 02:23:47 GMT
USER odoo
# Thu, 07 Sep 2023 02:23:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Sep 2023 02:23:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aee24f7779098be746c2ccfd465a71089f8fabdd3871b79af9060fc44a2911b`  
		Last Modified: Thu, 07 Sep 2023 02:29:47 GMT  
		Size: 221.0 MB (220992957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bb15e16ded7af3729af7fcb014075bc7146c328b39adade6d7a98d491b1b28`  
		Last Modified: Thu, 07 Sep 2023 02:29:22 GMT  
		Size: 2.6 MB (2579967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9358b870e15ee771e762346a77778b643846ade6027dab02e21d6024a92eff6`  
		Last Modified: Thu, 07 Sep 2023 02:29:22 GMT  
		Size: 455.7 KB (455729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551234f68e71be923c2c4bc655c255fa6ce8cc730164d6a09ca97ae73170ca45`  
		Last Modified: Thu, 07 Sep 2023 02:29:58 GMT  
		Size: 320.8 MB (320814992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72c7ed9df09ad4eab969b8aa7bc02a47533aed439fcebefbff1f4c1c571a96f`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5260cd37150ba2ec9d2a415e8a0220c168eefe2bcc5d69a13d7f024baecd2ec3`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d63f28df435ef28ec0648a37571f83f2eaa27e8a01604242d99551427940188`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4b5979b281dc33f6d7f9603f4d35323a811f2e45ad08f0b7240238c67b8944`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:31e089bb7cb5e249ce5b78eb29ab15a14ed32aabef1dc7d8fe14ec85f636d026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f76d4c4e165b21257b04f392f61a76111f7b3aa9826a2bee2275068683352d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.3 MB (576263613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6800c65be4d3733b1aeb75089fcc8ff8502727aa13f7be93490446f3f0d0502a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:21:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Sep 2023 02:21:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Sep 2023 02:21:01 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:22:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 07 Sep 2023 02:22:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:22:19 GMT
RUN npm install -g rtlcss
# Thu, 07 Sep 2023 02:22:19 GMT
ENV ODOO_VERSION=16.0
# Thu, 07 Sep 2023 02:22:20 GMT
ARG ODOO_RELEASE=20230901
# Thu, 07 Sep 2023 02:22:20 GMT
ARG ODOO_SHA=2287a32457f8d26405b7203820c54dc112a4537d
# Thu, 07 Sep 2023 02:23:41 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=2287a32457f8d26405b7203820c54dc112a4537d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 07 Sep 2023 02:23:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 07 Sep 2023 02:23:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 07 Sep 2023 02:23:46 GMT
# ARGS: ODOO_RELEASE=20230901 ODOO_SHA=2287a32457f8d26405b7203820c54dc112a4537d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 07 Sep 2023 02:23:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Sep 2023 02:23:46 GMT
EXPOSE 8069 8071 8072
# Thu, 07 Sep 2023 02:23:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Sep 2023 02:23:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 07 Sep 2023 02:23:47 GMT
USER odoo
# Thu, 07 Sep 2023 02:23:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Sep 2023 02:23:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aee24f7779098be746c2ccfd465a71089f8fabdd3871b79af9060fc44a2911b`  
		Last Modified: Thu, 07 Sep 2023 02:29:47 GMT  
		Size: 221.0 MB (220992957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bb15e16ded7af3729af7fcb014075bc7146c328b39adade6d7a98d491b1b28`  
		Last Modified: Thu, 07 Sep 2023 02:29:22 GMT  
		Size: 2.6 MB (2579967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9358b870e15ee771e762346a77778b643846ade6027dab02e21d6024a92eff6`  
		Last Modified: Thu, 07 Sep 2023 02:29:22 GMT  
		Size: 455.7 KB (455729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551234f68e71be923c2c4bc655c255fa6ce8cc730164d6a09ca97ae73170ca45`  
		Last Modified: Thu, 07 Sep 2023 02:29:58 GMT  
		Size: 320.8 MB (320814992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72c7ed9df09ad4eab969b8aa7bc02a47533aed439fcebefbff1f4c1c571a96f`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5260cd37150ba2ec9d2a415e8a0220c168eefe2bcc5d69a13d7f024baecd2ec3`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d63f28df435ef28ec0648a37571f83f2eaa27e8a01604242d99551427940188`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4b5979b281dc33f6d7f9603f4d35323a811f2e45ad08f0b7240238c67b8944`  
		Last Modified: Thu, 07 Sep 2023 02:29:20 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
