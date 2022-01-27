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
$ docker pull odoo@sha256:377b92bf67b064f71514e280e5fc9ec2bdd244cb7d86e009b156fd5d487ad227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:ba1271c5a159968ba77d6067e14e539b240189f1d598ce494e5862ec5589931e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.5 MB (539499256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb777c2926e0d05243eef3a03070a68a8d82dc50368eaa8d56ee5ad4be9673d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:06:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:06:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:06:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:10:31 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:11:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:11:19 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:11:19 GMT
ENV ODOO_VERSION=13.0
# Thu, 27 Jan 2022 22:34:13 GMT
ARG ODOO_RELEASE=20220126
# Thu, 27 Jan 2022 22:34:13 GMT
ARG ODOO_SHA=b9ab34152fff8027ed2622cbbdc7b3387b2ab270
# Thu, 27 Jan 2022 22:35:28 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=b9ab34152fff8027ed2622cbbdc7b3387b2ab270
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 27 Jan 2022 22:35:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 27 Jan 2022 22:35:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 27 Jan 2022 22:35:32 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=b9ab34152fff8027ed2622cbbdc7b3387b2ab270
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 27 Jan 2022 22:35:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 27 Jan 2022 22:35:33 GMT
EXPOSE 8069 8071 8072
# Thu, 27 Jan 2022 22:35:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 27 Jan 2022 22:35:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 27 Jan 2022 22:35:34 GMT
USER odoo
# Thu, 27 Jan 2022 22:35:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 22:35:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1643683a10820c31ffd26f415c4c5a3d8da779af7f087d7c33939c40597425a`  
		Last Modified: Wed, 26 Jan 2022 09:16:15 GMT  
		Size: 207.1 MB (207131191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebec2e1c27f1ac41a1fde98e797a9891f5dc8db95df82fc8e43e3717d5bcb7f8`  
		Last Modified: Wed, 26 Jan 2022 09:15:39 GMT  
		Size: 13.4 MB (13433899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426af2fe5b1c6cfebdb4e8ec73348b9d2c5b12fc783ac4d7daa8e515c42f80f8`  
		Last Modified: Wed, 26 Jan 2022 09:15:35 GMT  
		Size: 447.0 KB (447023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e2d03750a1dbbdb7548298fe13b6d25c5b75868c5adc5feb13a48dfc624d64`  
		Last Modified: Thu, 27 Jan 2022 22:37:47 GMT  
		Size: 291.3 MB (291330954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62490a10f235a1bb4aa62fe116734b557fa2c2ec775f5823cf10640ce5b0deb`  
		Last Modified: Thu, 27 Jan 2022 22:37:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d31cb297afcee06a694a5ec66275ce9f6fcd15179097bd0ecd99437a1439c12`  
		Last Modified: Thu, 27 Jan 2022 22:37:16 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0830ee1f3c14cd6e84d8d8d639755e7879bcb7be3ff563079e7bdba19de252dd`  
		Last Modified: Thu, 27 Jan 2022 22:37:16 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e786d743d50ce0bb24227b79295684567c3cb43b238fdee2ed31b44428f8dd9d`  
		Last Modified: Thu, 27 Jan 2022 22:37:16 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:377b92bf67b064f71514e280e5fc9ec2bdd244cb7d86e009b156fd5d487ad227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:ba1271c5a159968ba77d6067e14e539b240189f1d598ce494e5862ec5589931e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.5 MB (539499256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb777c2926e0d05243eef3a03070a68a8d82dc50368eaa8d56ee5ad4be9673d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:06:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:06:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:06:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:10:31 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:11:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:11:19 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:11:19 GMT
ENV ODOO_VERSION=13.0
# Thu, 27 Jan 2022 22:34:13 GMT
ARG ODOO_RELEASE=20220126
# Thu, 27 Jan 2022 22:34:13 GMT
ARG ODOO_SHA=b9ab34152fff8027ed2622cbbdc7b3387b2ab270
# Thu, 27 Jan 2022 22:35:28 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=b9ab34152fff8027ed2622cbbdc7b3387b2ab270
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 27 Jan 2022 22:35:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 27 Jan 2022 22:35:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 27 Jan 2022 22:35:32 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=b9ab34152fff8027ed2622cbbdc7b3387b2ab270
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 27 Jan 2022 22:35:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 27 Jan 2022 22:35:33 GMT
EXPOSE 8069 8071 8072
# Thu, 27 Jan 2022 22:35:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 27 Jan 2022 22:35:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 27 Jan 2022 22:35:34 GMT
USER odoo
# Thu, 27 Jan 2022 22:35:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 22:35:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1643683a10820c31ffd26f415c4c5a3d8da779af7f087d7c33939c40597425a`  
		Last Modified: Wed, 26 Jan 2022 09:16:15 GMT  
		Size: 207.1 MB (207131191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebec2e1c27f1ac41a1fde98e797a9891f5dc8db95df82fc8e43e3717d5bcb7f8`  
		Last Modified: Wed, 26 Jan 2022 09:15:39 GMT  
		Size: 13.4 MB (13433899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426af2fe5b1c6cfebdb4e8ec73348b9d2c5b12fc783ac4d7daa8e515c42f80f8`  
		Last Modified: Wed, 26 Jan 2022 09:15:35 GMT  
		Size: 447.0 KB (447023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e2d03750a1dbbdb7548298fe13b6d25c5b75868c5adc5feb13a48dfc624d64`  
		Last Modified: Thu, 27 Jan 2022 22:37:47 GMT  
		Size: 291.3 MB (291330954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62490a10f235a1bb4aa62fe116734b557fa2c2ec775f5823cf10640ce5b0deb`  
		Last Modified: Thu, 27 Jan 2022 22:37:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d31cb297afcee06a694a5ec66275ce9f6fcd15179097bd0ecd99437a1439c12`  
		Last Modified: Thu, 27 Jan 2022 22:37:16 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0830ee1f3c14cd6e84d8d8d639755e7879bcb7be3ff563079e7bdba19de252dd`  
		Last Modified: Thu, 27 Jan 2022 22:37:16 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e786d743d50ce0bb24227b79295684567c3cb43b238fdee2ed31b44428f8dd9d`  
		Last Modified: Thu, 27 Jan 2022 22:37:16 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:c1d74ac7e76e6896aa80ab74a8d68a945ca308931eb7eb7082c27a35126a0b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:82554bc10bd32c62484d77ae17b4eea5bc85637d20a6d7917d5ff9f932b04be7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529290104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78426a5b447caddac499952ae6e16bf501c5b27faa64afe9fc2cc238660c19d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:06:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:06:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:06:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:07:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:07:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:07:52 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:07:52 GMT
ENV ODOO_VERSION=14.0
# Thu, 27 Jan 2022 22:32:35 GMT
ARG ODOO_RELEASE=20220126
# Thu, 27 Jan 2022 22:32:36 GMT
ARG ODOO_SHA=44e94c2e87735991d7adffa07067a6b46dd25c1f
# Thu, 27 Jan 2022 22:33:52 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=44e94c2e87735991d7adffa07067a6b46dd25c1f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 27 Jan 2022 22:33:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 27 Jan 2022 22:33:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 27 Jan 2022 22:33:57 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=44e94c2e87735991d7adffa07067a6b46dd25c1f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 27 Jan 2022 22:33:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 27 Jan 2022 22:33:57 GMT
EXPOSE 8069 8071 8072
# Thu, 27 Jan 2022 22:33:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 27 Jan 2022 22:33:58 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 27 Jan 2022 22:33:58 GMT
USER odoo
# Thu, 27 Jan 2022 22:33:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 22:33:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158787f79b5bbd45592d744836bf9bab3a8f9ffc1fc9d765e0a69828fba80f7a`  
		Last Modified: Wed, 26 Jan 2022 09:15:11 GMT  
		Size: 213.2 MB (213173094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c04dc7402806cf6edd8c86d43be59a3f35cc2abdeb069509b0b8089ff88d8c`  
		Last Modified: Wed, 26 Jan 2022 09:14:42 GMT  
		Size: 13.4 MB (13436578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b98a5866acaabb48e508494ade5b4cd13f3c3225e581cd1ea045e283d0602c`  
		Last Modified: Wed, 26 Jan 2022 09:14:38 GMT  
		Size: 447.0 KB (446976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0195b2c2b83463b7c33ee9296b57cf89408d28ce5a55565b1a3ed9d338e23aef`  
		Last Modified: Thu, 27 Jan 2022 22:37:05 GMT  
		Size: 275.1 MB (275077260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c5cea0f0fb47bbf6b07e167d3c9ed590d7394c63ac2249f658c25a9a4bc6d0`  
		Last Modified: Thu, 27 Jan 2022 22:36:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a187b73b872ca3f7ef4b7ee3ae1f41ad1343d7777a4bc77426a9fdcc88591e`  
		Last Modified: Thu, 27 Jan 2022 22:36:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba50cb6327813dd3eaafdbc2e37956b6cbd88f6d82c124af930236acaf444254`  
		Last Modified: Thu, 27 Jan 2022 22:36:34 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc49ac749e91644f151f7243fe546437bace78f2b43a598b7607d96ee6ead6ff`  
		Last Modified: Thu, 27 Jan 2022 22:36:34 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:c1d74ac7e76e6896aa80ab74a8d68a945ca308931eb7eb7082c27a35126a0b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:82554bc10bd32c62484d77ae17b4eea5bc85637d20a6d7917d5ff9f932b04be7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529290104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78426a5b447caddac499952ae6e16bf501c5b27faa64afe9fc2cc238660c19d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:06:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:06:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:06:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:07:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:07:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:07:52 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:07:52 GMT
ENV ODOO_VERSION=14.0
# Thu, 27 Jan 2022 22:32:35 GMT
ARG ODOO_RELEASE=20220126
# Thu, 27 Jan 2022 22:32:36 GMT
ARG ODOO_SHA=44e94c2e87735991d7adffa07067a6b46dd25c1f
# Thu, 27 Jan 2022 22:33:52 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=44e94c2e87735991d7adffa07067a6b46dd25c1f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 27 Jan 2022 22:33:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 27 Jan 2022 22:33:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 27 Jan 2022 22:33:57 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=44e94c2e87735991d7adffa07067a6b46dd25c1f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 27 Jan 2022 22:33:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 27 Jan 2022 22:33:57 GMT
EXPOSE 8069 8071 8072
# Thu, 27 Jan 2022 22:33:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 27 Jan 2022 22:33:58 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 27 Jan 2022 22:33:58 GMT
USER odoo
# Thu, 27 Jan 2022 22:33:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 22:33:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158787f79b5bbd45592d744836bf9bab3a8f9ffc1fc9d765e0a69828fba80f7a`  
		Last Modified: Wed, 26 Jan 2022 09:15:11 GMT  
		Size: 213.2 MB (213173094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c04dc7402806cf6edd8c86d43be59a3f35cc2abdeb069509b0b8089ff88d8c`  
		Last Modified: Wed, 26 Jan 2022 09:14:42 GMT  
		Size: 13.4 MB (13436578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b98a5866acaabb48e508494ade5b4cd13f3c3225e581cd1ea045e283d0602c`  
		Last Modified: Wed, 26 Jan 2022 09:14:38 GMT  
		Size: 447.0 KB (446976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0195b2c2b83463b7c33ee9296b57cf89408d28ce5a55565b1a3ed9d338e23aef`  
		Last Modified: Thu, 27 Jan 2022 22:37:05 GMT  
		Size: 275.1 MB (275077260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c5cea0f0fb47bbf6b07e167d3c9ed590d7394c63ac2249f658c25a9a4bc6d0`  
		Last Modified: Thu, 27 Jan 2022 22:36:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a187b73b872ca3f7ef4b7ee3ae1f41ad1343d7777a4bc77426a9fdcc88591e`  
		Last Modified: Thu, 27 Jan 2022 22:36:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba50cb6327813dd3eaafdbc2e37956b6cbd88f6d82c124af930236acaf444254`  
		Last Modified: Thu, 27 Jan 2022 22:36:34 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc49ac749e91644f151f7243fe546437bace78f2b43a598b7607d96ee6ead6ff`  
		Last Modified: Thu, 27 Jan 2022 22:36:34 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:5134db0309f9c770e0f7e008db968b20bfb4bb579f23045ab0fe4a3718437397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:3c722e63526c5e965b26f9332bab440a36d3761cef6becab731ad1e3218d6f50
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548538837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54dbfd87063bbedbba8a02f2c4b03ee68139a76033e0eff013f1a21fe453a094`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:02:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:02:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:02:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:04:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:04:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:04:46 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:04:46 GMT
ENV ODOO_VERSION=15.0
# Thu, 27 Jan 2022 22:30:58 GMT
ARG ODOO_RELEASE=20220126
# Thu, 27 Jan 2022 22:30:58 GMT
ARG ODOO_SHA=06fd2afdaa200f8a59a8e9682fcdba1f8f525ca7
# Thu, 27 Jan 2022 22:32:19 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=06fd2afdaa200f8a59a8e9682fcdba1f8f525ca7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 27 Jan 2022 22:32:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 27 Jan 2022 22:32:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 27 Jan 2022 22:32:24 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=06fd2afdaa200f8a59a8e9682fcdba1f8f525ca7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 27 Jan 2022 22:32:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 27 Jan 2022 22:32:25 GMT
EXPOSE 8069 8071 8072
# Thu, 27 Jan 2022 22:32:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 27 Jan 2022 22:32:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 27 Jan 2022 22:32:25 GMT
USER odoo
# Thu, 27 Jan 2022 22:32:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 22:32:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9293b96c918352418f9470373a3ccf1788a2b957d28fcb51b99beab26e73f974`  
		Last Modified: Wed, 26 Jan 2022 09:14:12 GMT  
		Size: 220.3 MB (220291077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb4ef07b63f082d87ab75156c6ae62bcaf11e1ac37595986d8fd97b5dd5c80`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 2.5 MB (2506147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2f8d17d4fa74bd599ba34671d44d6da384f629a1bda0e322208540e26ae8ee`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 440.2 KB (440201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084eca7ff9de292c120c5b583459aef1ae0ffb457eb688858edaf8004cd69050`  
		Last Modified: Thu, 27 Jan 2022 22:36:21 GMT  
		Size: 293.9 MB (293932692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3976793283215b264be9ae1c43dd9c3eb803c1336fc75723731dd72f8a55f175`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e519e7fce90c6029c6c42669b486a184d4a4cd76024bffa362339247a3a61b`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdacad12d34bc7735afc2e377722832e89e9a4bac7a2b9f0e65cc9a57e20e2c5`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3557c369292b42fb45610d54160e79c26acd2326cc9f21b9c0c4e7a23daace19`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:5134db0309f9c770e0f7e008db968b20bfb4bb579f23045ab0fe4a3718437397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:3c722e63526c5e965b26f9332bab440a36d3761cef6becab731ad1e3218d6f50
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548538837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54dbfd87063bbedbba8a02f2c4b03ee68139a76033e0eff013f1a21fe453a094`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:02:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:02:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:02:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:04:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:04:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:04:46 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:04:46 GMT
ENV ODOO_VERSION=15.0
# Thu, 27 Jan 2022 22:30:58 GMT
ARG ODOO_RELEASE=20220126
# Thu, 27 Jan 2022 22:30:58 GMT
ARG ODOO_SHA=06fd2afdaa200f8a59a8e9682fcdba1f8f525ca7
# Thu, 27 Jan 2022 22:32:19 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=06fd2afdaa200f8a59a8e9682fcdba1f8f525ca7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 27 Jan 2022 22:32:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 27 Jan 2022 22:32:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 27 Jan 2022 22:32:24 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=06fd2afdaa200f8a59a8e9682fcdba1f8f525ca7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 27 Jan 2022 22:32:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 27 Jan 2022 22:32:25 GMT
EXPOSE 8069 8071 8072
# Thu, 27 Jan 2022 22:32:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 27 Jan 2022 22:32:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 27 Jan 2022 22:32:25 GMT
USER odoo
# Thu, 27 Jan 2022 22:32:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 22:32:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9293b96c918352418f9470373a3ccf1788a2b957d28fcb51b99beab26e73f974`  
		Last Modified: Wed, 26 Jan 2022 09:14:12 GMT  
		Size: 220.3 MB (220291077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb4ef07b63f082d87ab75156c6ae62bcaf11e1ac37595986d8fd97b5dd5c80`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 2.5 MB (2506147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2f8d17d4fa74bd599ba34671d44d6da384f629a1bda0e322208540e26ae8ee`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 440.2 KB (440201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084eca7ff9de292c120c5b583459aef1ae0ffb457eb688858edaf8004cd69050`  
		Last Modified: Thu, 27 Jan 2022 22:36:21 GMT  
		Size: 293.9 MB (293932692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3976793283215b264be9ae1c43dd9c3eb803c1336fc75723731dd72f8a55f175`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e519e7fce90c6029c6c42669b486a184d4a4cd76024bffa362339247a3a61b`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdacad12d34bc7735afc2e377722832e89e9a4bac7a2b9f0e65cc9a57e20e2c5`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3557c369292b42fb45610d54160e79c26acd2326cc9f21b9c0c4e7a23daace19`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:5134db0309f9c770e0f7e008db968b20bfb4bb579f23045ab0fe4a3718437397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:3c722e63526c5e965b26f9332bab440a36d3761cef6becab731ad1e3218d6f50
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548538837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54dbfd87063bbedbba8a02f2c4b03ee68139a76033e0eff013f1a21fe453a094`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:02:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:02:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:02:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:04:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:04:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:04:46 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:04:46 GMT
ENV ODOO_VERSION=15.0
# Thu, 27 Jan 2022 22:30:58 GMT
ARG ODOO_RELEASE=20220126
# Thu, 27 Jan 2022 22:30:58 GMT
ARG ODOO_SHA=06fd2afdaa200f8a59a8e9682fcdba1f8f525ca7
# Thu, 27 Jan 2022 22:32:19 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=06fd2afdaa200f8a59a8e9682fcdba1f8f525ca7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 27 Jan 2022 22:32:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 27 Jan 2022 22:32:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 27 Jan 2022 22:32:24 GMT
# ARGS: ODOO_RELEASE=20220126 ODOO_SHA=06fd2afdaa200f8a59a8e9682fcdba1f8f525ca7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 27 Jan 2022 22:32:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 27 Jan 2022 22:32:25 GMT
EXPOSE 8069 8071 8072
# Thu, 27 Jan 2022 22:32:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 27 Jan 2022 22:32:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 27 Jan 2022 22:32:25 GMT
USER odoo
# Thu, 27 Jan 2022 22:32:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Jan 2022 22:32:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9293b96c918352418f9470373a3ccf1788a2b957d28fcb51b99beab26e73f974`  
		Last Modified: Wed, 26 Jan 2022 09:14:12 GMT  
		Size: 220.3 MB (220291077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb4ef07b63f082d87ab75156c6ae62bcaf11e1ac37595986d8fd97b5dd5c80`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 2.5 MB (2506147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2f8d17d4fa74bd599ba34671d44d6da384f629a1bda0e322208540e26ae8ee`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 440.2 KB (440201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084eca7ff9de292c120c5b583459aef1ae0ffb457eb688858edaf8004cd69050`  
		Last Modified: Thu, 27 Jan 2022 22:36:21 GMT  
		Size: 293.9 MB (293932692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3976793283215b264be9ae1c43dd9c3eb803c1336fc75723731dd72f8a55f175`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e519e7fce90c6029c6c42669b486a184d4a4cd76024bffa362339247a3a61b`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdacad12d34bc7735afc2e377722832e89e9a4bac7a2b9f0e65cc9a57e20e2c5`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3557c369292b42fb45610d54160e79c26acd2326cc9f21b9c0c4e7a23daace19`  
		Last Modified: Thu, 27 Jan 2022 22:35:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
