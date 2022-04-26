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
$ docker pull odoo@sha256:af5946762652db6721b7dca165ff7834af668300f7a4e54acae86f6670be2e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:0afe5c801c94fe853ea44caf1a821d06562bc74c3cf69d11691a0bf4aaae5329
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.9 MB (539919393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ecd5d1249fbaf372b399719923a28ca748f5f84c3e898a50376e6f613d2636`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:46:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:46:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:46:25 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:50:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:50:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:50:41 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:50:41 GMT
ENV ODOO_VERSION=13.0
# Tue, 26 Apr 2022 00:56:37 GMT
ARG ODOO_RELEASE=20220425
# Tue, 26 Apr 2022 00:56:37 GMT
ARG ODOO_SHA=3409fcd9d0365e96357ab6fa87d6553f980eb0f5
# Tue, 26 Apr 2022 00:57:48 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=3409fcd9d0365e96357ab6fa87d6553f980eb0f5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 26 Apr 2022 00:57:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 26 Apr 2022 00:57:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 26 Apr 2022 00:57:52 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=3409fcd9d0365e96357ab6fa87d6553f980eb0f5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 26 Apr 2022 00:57:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 26 Apr 2022 00:57:52 GMT
EXPOSE 8069 8071 8072
# Tue, 26 Apr 2022 00:57:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 26 Apr 2022 00:57:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 26 Apr 2022 00:57:53 GMT
USER odoo
# Tue, 26 Apr 2022 00:57:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Apr 2022 00:57:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb5c2f3aa8570028e1481e683ce676526f2f383e1d583fc8fe80151c3d75a46`  
		Last Modified: Wed, 20 Apr 2022 12:54:29 GMT  
		Size: 207.1 MB (207144149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ed24c51a5113dc123abfe7c3ae5947e181a730ec5220f51852ce8b7cb296d9`  
		Last Modified: Wed, 20 Apr 2022 12:54:07 GMT  
		Size: 13.4 MB (13438172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2e9a8cb5ff656fd7d11d44d86b540b5429edfa5d9d2ce063061e5f2a027b2b`  
		Last Modified: Wed, 20 Apr 2022 12:54:05 GMT  
		Size: 458.4 KB (458398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82119da2e98ef9d4a3f6cad41bc0ff7cbbc771550b89643a321fc9b20851eae8`  
		Last Modified: Tue, 26 Apr 2022 01:00:24 GMT  
		Size: 291.7 MB (291735551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cdf56f1ce93339c4cf7bd6a40f209dab52703f7f901ed58633734b28aace4b`  
		Last Modified: Tue, 26 Apr 2022 00:59:53 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1961efd3350a91777f50f4881363af5d27c5374f9c481308bf51364e1de5db27`  
		Last Modified: Tue, 26 Apr 2022 00:59:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4110f2a8ba7ba146eea31de41b20f2edf490331cd2610917341479f9e93104b3`  
		Last Modified: Tue, 26 Apr 2022 00:59:53 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daff9b280075a4cdc9efb46f525a2ea5e11ed53c88d71b9b1d2b06e9b1e52e6c`  
		Last Modified: Tue, 26 Apr 2022 00:59:53 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:af5946762652db6721b7dca165ff7834af668300f7a4e54acae86f6670be2e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:0afe5c801c94fe853ea44caf1a821d06562bc74c3cf69d11691a0bf4aaae5329
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.9 MB (539919393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ecd5d1249fbaf372b399719923a28ca748f5f84c3e898a50376e6f613d2636`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:46:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:46:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:46:25 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:50:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:50:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:50:41 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:50:41 GMT
ENV ODOO_VERSION=13.0
# Tue, 26 Apr 2022 00:56:37 GMT
ARG ODOO_RELEASE=20220425
# Tue, 26 Apr 2022 00:56:37 GMT
ARG ODOO_SHA=3409fcd9d0365e96357ab6fa87d6553f980eb0f5
# Tue, 26 Apr 2022 00:57:48 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=3409fcd9d0365e96357ab6fa87d6553f980eb0f5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 26 Apr 2022 00:57:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 26 Apr 2022 00:57:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 26 Apr 2022 00:57:52 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=3409fcd9d0365e96357ab6fa87d6553f980eb0f5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 26 Apr 2022 00:57:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 26 Apr 2022 00:57:52 GMT
EXPOSE 8069 8071 8072
# Tue, 26 Apr 2022 00:57:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 26 Apr 2022 00:57:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 26 Apr 2022 00:57:53 GMT
USER odoo
# Tue, 26 Apr 2022 00:57:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Apr 2022 00:57:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb5c2f3aa8570028e1481e683ce676526f2f383e1d583fc8fe80151c3d75a46`  
		Last Modified: Wed, 20 Apr 2022 12:54:29 GMT  
		Size: 207.1 MB (207144149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ed24c51a5113dc123abfe7c3ae5947e181a730ec5220f51852ce8b7cb296d9`  
		Last Modified: Wed, 20 Apr 2022 12:54:07 GMT  
		Size: 13.4 MB (13438172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2e9a8cb5ff656fd7d11d44d86b540b5429edfa5d9d2ce063061e5f2a027b2b`  
		Last Modified: Wed, 20 Apr 2022 12:54:05 GMT  
		Size: 458.4 KB (458398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82119da2e98ef9d4a3f6cad41bc0ff7cbbc771550b89643a321fc9b20851eae8`  
		Last Modified: Tue, 26 Apr 2022 01:00:24 GMT  
		Size: 291.7 MB (291735551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cdf56f1ce93339c4cf7bd6a40f209dab52703f7f901ed58633734b28aace4b`  
		Last Modified: Tue, 26 Apr 2022 00:59:53 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1961efd3350a91777f50f4881363af5d27c5374f9c481308bf51364e1de5db27`  
		Last Modified: Tue, 26 Apr 2022 00:59:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4110f2a8ba7ba146eea31de41b20f2edf490331cd2610917341479f9e93104b3`  
		Last Modified: Tue, 26 Apr 2022 00:59:53 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daff9b280075a4cdc9efb46f525a2ea5e11ed53c88d71b9b1d2b06e9b1e52e6c`  
		Last Modified: Tue, 26 Apr 2022 00:59:53 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:3bdbe601a4eb5b3d9a115abe7e3dbf324d997ec95a7cb1e4a30e788e4fe547f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:5175fc236b7424e17b3567536543c0f29971cfd20a2532046b67311bf9b8d5ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.9 MB (529936476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79b078b92340da27c67cfb80aa903e850bbd86e5689b8831e805a928469f872`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:46:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:46:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:46:25 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:47:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:47:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:47:55 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:47:56 GMT
ENV ODOO_VERSION=14.0
# Tue, 26 Apr 2022 00:55:14 GMT
ARG ODOO_RELEASE=20220425
# Tue, 26 Apr 2022 00:55:14 GMT
ARG ODOO_SHA=f291bdf86a35821b96fa6565756585f8d5b353c4
# Tue, 26 Apr 2022 00:56:25 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=f291bdf86a35821b96fa6565756585f8d5b353c4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 26 Apr 2022 00:56:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 26 Apr 2022 00:56:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 26 Apr 2022 00:56:30 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=f291bdf86a35821b96fa6565756585f8d5b353c4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 26 Apr 2022 00:56:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 26 Apr 2022 00:56:30 GMT
EXPOSE 8069 8071 8072
# Tue, 26 Apr 2022 00:56:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 26 Apr 2022 00:56:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 26 Apr 2022 00:56:30 GMT
USER odoo
# Tue, 26 Apr 2022 00:56:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Apr 2022 00:56:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef0b3a5b3ccf6bc33961621c8b4217adc5f5ef26d7b92c47c8c39a8820fd58b`  
		Last Modified: Wed, 20 Apr 2022 12:53:38 GMT  
		Size: 213.2 MB (213177837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b2adc658049f20fffa9059922d790f2cc75e2fc5db14b3c1b77043b486b694`  
		Last Modified: Wed, 20 Apr 2022 12:53:16 GMT  
		Size: 13.4 MB (13440548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafa09d0f12a0ed57ad93fe02efadcc57e517a8c1b2abf6d42c04e6b5031e65`  
		Last Modified: Wed, 20 Apr 2022 12:53:13 GMT  
		Size: 458.5 KB (458493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74cc20e9d78937adf9cbb1a8846467985f8992a35c7a8a62693d7410aac11`  
		Last Modified: Tue, 26 Apr 2022 00:59:39 GMT  
		Size: 275.7 MB (275716469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a19aa306fa6e91e1751cca4437132bed7abeaf8904e427a315c205bd3d330`  
		Last Modified: Tue, 26 Apr 2022 00:59:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b9fe8ea63959ad97b8070c35d41e52fd0614cde3501e61dd02690d3b466a2d`  
		Last Modified: Tue, 26 Apr 2022 00:59:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f722c4785482fd42db98a7d66f903e4f18d6ce386bfadd8b26d3f328b57dc859`  
		Last Modified: Tue, 26 Apr 2022 00:59:06 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d5c524f30f13d717285bfdd4a5029cffee6f76c203667d9bf92f6ed04450d2`  
		Last Modified: Tue, 26 Apr 2022 00:59:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:3bdbe601a4eb5b3d9a115abe7e3dbf324d997ec95a7cb1e4a30e788e4fe547f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:5175fc236b7424e17b3567536543c0f29971cfd20a2532046b67311bf9b8d5ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.9 MB (529936476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79b078b92340da27c67cfb80aa903e850bbd86e5689b8831e805a928469f872`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:46:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:46:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:46:25 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:47:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:47:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:47:55 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:47:56 GMT
ENV ODOO_VERSION=14.0
# Tue, 26 Apr 2022 00:55:14 GMT
ARG ODOO_RELEASE=20220425
# Tue, 26 Apr 2022 00:55:14 GMT
ARG ODOO_SHA=f291bdf86a35821b96fa6565756585f8d5b353c4
# Tue, 26 Apr 2022 00:56:25 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=f291bdf86a35821b96fa6565756585f8d5b353c4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 26 Apr 2022 00:56:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 26 Apr 2022 00:56:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 26 Apr 2022 00:56:30 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=f291bdf86a35821b96fa6565756585f8d5b353c4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 26 Apr 2022 00:56:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 26 Apr 2022 00:56:30 GMT
EXPOSE 8069 8071 8072
# Tue, 26 Apr 2022 00:56:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 26 Apr 2022 00:56:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 26 Apr 2022 00:56:30 GMT
USER odoo
# Tue, 26 Apr 2022 00:56:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Apr 2022 00:56:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef0b3a5b3ccf6bc33961621c8b4217adc5f5ef26d7b92c47c8c39a8820fd58b`  
		Last Modified: Wed, 20 Apr 2022 12:53:38 GMT  
		Size: 213.2 MB (213177837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b2adc658049f20fffa9059922d790f2cc75e2fc5db14b3c1b77043b486b694`  
		Last Modified: Wed, 20 Apr 2022 12:53:16 GMT  
		Size: 13.4 MB (13440548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafa09d0f12a0ed57ad93fe02efadcc57e517a8c1b2abf6d42c04e6b5031e65`  
		Last Modified: Wed, 20 Apr 2022 12:53:13 GMT  
		Size: 458.5 KB (458493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74cc20e9d78937adf9cbb1a8846467985f8992a35c7a8a62693d7410aac11`  
		Last Modified: Tue, 26 Apr 2022 00:59:39 GMT  
		Size: 275.7 MB (275716469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a19aa306fa6e91e1751cca4437132bed7abeaf8904e427a315c205bd3d330`  
		Last Modified: Tue, 26 Apr 2022 00:59:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b9fe8ea63959ad97b8070c35d41e52fd0614cde3501e61dd02690d3b466a2d`  
		Last Modified: Tue, 26 Apr 2022 00:59:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f722c4785482fd42db98a7d66f903e4f18d6ce386bfadd8b26d3f328b57dc859`  
		Last Modified: Tue, 26 Apr 2022 00:59:06 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d5c524f30f13d717285bfdd4a5029cffee6f76c203667d9bf92f6ed04450d2`  
		Last Modified: Tue, 26 Apr 2022 00:59:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:ad78723d061209148592de9075a30e806d3e92c8a0915ece02676624ffe65ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:58e6b5a0813962f8ea295aed4981a68eb339070e7b16e78c45164720bff1ee38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.2 MB (552202977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e614a6c939841878c2c1e3229f94444b27ea3beff6c63dc3a8e5de69bb9c6834`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:43:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:43:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:43:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:44:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:44:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:44:52 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:44:52 GMT
ENV ODOO_VERSION=15.0
# Tue, 26 Apr 2022 00:53:51 GMT
ARG ODOO_RELEASE=20220425
# Tue, 26 Apr 2022 00:53:51 GMT
ARG ODOO_SHA=20dcece1bc2e25cf3950a419074b127dd7ef8c0f
# Tue, 26 Apr 2022 00:55:06 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=20dcece1bc2e25cf3950a419074b127dd7ef8c0f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 26 Apr 2022 00:55:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 26 Apr 2022 00:55:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 26 Apr 2022 00:55:11 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=20dcece1bc2e25cf3950a419074b127dd7ef8c0f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 26 Apr 2022 00:55:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 26 Apr 2022 00:55:11 GMT
EXPOSE 8069 8071 8072
# Tue, 26 Apr 2022 00:55:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 26 Apr 2022 00:55:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 26 Apr 2022 00:55:12 GMT
USER odoo
# Tue, 26 Apr 2022 00:55:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Apr 2022 00:55:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f1aac8f860c1d54f3f94ccc883be166c671639bb052e7754baf4d6032ab4b3`  
		Last Modified: Wed, 20 Apr 2022 12:52:49 GMT  
		Size: 220.3 MB (220300936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875665d357afcc2f5c5593ae40db6baed8f4446ec9b8dca77d5605a49495e0cb`  
		Last Modified: Wed, 20 Apr 2022 12:52:24 GMT  
		Size: 2.5 MB (2510123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af9a5928702128a35bd3b53d8a01c591d7884eda973ecebcd3d765abeab07b8`  
		Last Modified: Wed, 20 Apr 2022 12:52:23 GMT  
		Size: 451.8 KB (451820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb2fa83ad149b9b3da0cd872c5f08ee387758d79da7ba9f90659645c704144c`  
		Last Modified: Tue, 26 Apr 2022 00:58:44 GMT  
		Size: 297.6 MB (297558656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a1b447e4842af9e0c1e0cf1efcf655990578e8d55ed52a71f2fd8df7641540`  
		Last Modified: Tue, 26 Apr 2022 00:58:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c632748b926cbdca55781f43e343cf61d8bd231099b721a9ebd867a9080fda`  
		Last Modified: Tue, 26 Apr 2022 00:58:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe5571a18cfcccaa9de56dfc9bcda7e51b08fd84783e44a12ea66e71d54b11e`  
		Last Modified: Tue, 26 Apr 2022 00:58:10 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d809296c260c6325598fbbd3d15a0207a7256cdd856a8c7f28b5c9605869b160`  
		Last Modified: Tue, 26 Apr 2022 00:58:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:ad78723d061209148592de9075a30e806d3e92c8a0915ece02676624ffe65ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:58e6b5a0813962f8ea295aed4981a68eb339070e7b16e78c45164720bff1ee38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.2 MB (552202977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e614a6c939841878c2c1e3229f94444b27ea3beff6c63dc3a8e5de69bb9c6834`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:43:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:43:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:43:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:44:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:44:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:44:52 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:44:52 GMT
ENV ODOO_VERSION=15.0
# Tue, 26 Apr 2022 00:53:51 GMT
ARG ODOO_RELEASE=20220425
# Tue, 26 Apr 2022 00:53:51 GMT
ARG ODOO_SHA=20dcece1bc2e25cf3950a419074b127dd7ef8c0f
# Tue, 26 Apr 2022 00:55:06 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=20dcece1bc2e25cf3950a419074b127dd7ef8c0f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 26 Apr 2022 00:55:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 26 Apr 2022 00:55:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 26 Apr 2022 00:55:11 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=20dcece1bc2e25cf3950a419074b127dd7ef8c0f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 26 Apr 2022 00:55:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 26 Apr 2022 00:55:11 GMT
EXPOSE 8069 8071 8072
# Tue, 26 Apr 2022 00:55:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 26 Apr 2022 00:55:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 26 Apr 2022 00:55:12 GMT
USER odoo
# Tue, 26 Apr 2022 00:55:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Apr 2022 00:55:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f1aac8f860c1d54f3f94ccc883be166c671639bb052e7754baf4d6032ab4b3`  
		Last Modified: Wed, 20 Apr 2022 12:52:49 GMT  
		Size: 220.3 MB (220300936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875665d357afcc2f5c5593ae40db6baed8f4446ec9b8dca77d5605a49495e0cb`  
		Last Modified: Wed, 20 Apr 2022 12:52:24 GMT  
		Size: 2.5 MB (2510123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af9a5928702128a35bd3b53d8a01c591d7884eda973ecebcd3d765abeab07b8`  
		Last Modified: Wed, 20 Apr 2022 12:52:23 GMT  
		Size: 451.8 KB (451820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb2fa83ad149b9b3da0cd872c5f08ee387758d79da7ba9f90659645c704144c`  
		Last Modified: Tue, 26 Apr 2022 00:58:44 GMT  
		Size: 297.6 MB (297558656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a1b447e4842af9e0c1e0cf1efcf655990578e8d55ed52a71f2fd8df7641540`  
		Last Modified: Tue, 26 Apr 2022 00:58:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c632748b926cbdca55781f43e343cf61d8bd231099b721a9ebd867a9080fda`  
		Last Modified: Tue, 26 Apr 2022 00:58:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe5571a18cfcccaa9de56dfc9bcda7e51b08fd84783e44a12ea66e71d54b11e`  
		Last Modified: Tue, 26 Apr 2022 00:58:10 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d809296c260c6325598fbbd3d15a0207a7256cdd856a8c7f28b5c9605869b160`  
		Last Modified: Tue, 26 Apr 2022 00:58:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:ad78723d061209148592de9075a30e806d3e92c8a0915ece02676624ffe65ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:58e6b5a0813962f8ea295aed4981a68eb339070e7b16e78c45164720bff1ee38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.2 MB (552202977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e614a6c939841878c2c1e3229f94444b27ea3beff6c63dc3a8e5de69bb9c6834`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:43:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:43:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:43:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:44:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:44:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:44:52 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:44:52 GMT
ENV ODOO_VERSION=15.0
# Tue, 26 Apr 2022 00:53:51 GMT
ARG ODOO_RELEASE=20220425
# Tue, 26 Apr 2022 00:53:51 GMT
ARG ODOO_SHA=20dcece1bc2e25cf3950a419074b127dd7ef8c0f
# Tue, 26 Apr 2022 00:55:06 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=20dcece1bc2e25cf3950a419074b127dd7ef8c0f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 26 Apr 2022 00:55:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 26 Apr 2022 00:55:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 26 Apr 2022 00:55:11 GMT
# ARGS: ODOO_RELEASE=20220425 ODOO_SHA=20dcece1bc2e25cf3950a419074b127dd7ef8c0f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 26 Apr 2022 00:55:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 26 Apr 2022 00:55:11 GMT
EXPOSE 8069 8071 8072
# Tue, 26 Apr 2022 00:55:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 26 Apr 2022 00:55:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 26 Apr 2022 00:55:12 GMT
USER odoo
# Tue, 26 Apr 2022 00:55:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Apr 2022 00:55:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f1aac8f860c1d54f3f94ccc883be166c671639bb052e7754baf4d6032ab4b3`  
		Last Modified: Wed, 20 Apr 2022 12:52:49 GMT  
		Size: 220.3 MB (220300936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875665d357afcc2f5c5593ae40db6baed8f4446ec9b8dca77d5605a49495e0cb`  
		Last Modified: Wed, 20 Apr 2022 12:52:24 GMT  
		Size: 2.5 MB (2510123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af9a5928702128a35bd3b53d8a01c591d7884eda973ecebcd3d765abeab07b8`  
		Last Modified: Wed, 20 Apr 2022 12:52:23 GMT  
		Size: 451.8 KB (451820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb2fa83ad149b9b3da0cd872c5f08ee387758d79da7ba9f90659645c704144c`  
		Last Modified: Tue, 26 Apr 2022 00:58:44 GMT  
		Size: 297.6 MB (297558656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a1b447e4842af9e0c1e0cf1efcf655990578e8d55ed52a71f2fd8df7641540`  
		Last Modified: Tue, 26 Apr 2022 00:58:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c632748b926cbdca55781f43e343cf61d8bd231099b721a9ebd867a9080fda`  
		Last Modified: Tue, 26 Apr 2022 00:58:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe5571a18cfcccaa9de56dfc9bcda7e51b08fd84783e44a12ea66e71d54b11e`  
		Last Modified: Tue, 26 Apr 2022 00:58:10 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d809296c260c6325598fbbd3d15a0207a7256cdd856a8c7f28b5c9605869b160`  
		Last Modified: Tue, 26 Apr 2022 00:58:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
