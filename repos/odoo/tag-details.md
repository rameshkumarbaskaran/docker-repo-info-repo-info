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
$ docker pull odoo@sha256:3345864e9fe299c4d544d0af5d4794f75072bb78cc5b825737e8bd8da233fd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:070f3f5ac3d96105cc6dd5c4c7cb5b03216c5ba2835755b442a86f1893feacf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.8 MB (532786574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f04d93b28c19a4c5930c80e9b02006cabca98b05c40771e9e3931807672757`
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
# Thu, 29 Jun 2023 20:23:15 GMT
ARG ODOO_RELEASE=20230629
# Thu, 29 Jun 2023 20:23:15 GMT
ARG ODOO_SHA=621799a3ab09aacdf4139b3dbea6af48a2fb0df0
# Thu, 29 Jun 2023 20:24:40 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=621799a3ab09aacdf4139b3dbea6af48a2fb0df0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Jun 2023 20:24:44 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Jun 2023 20:24:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Jun 2023 20:24:44 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=621799a3ab09aacdf4139b3dbea6af48a2fb0df0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Jun 2023 20:24:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Jun 2023 20:24:45 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Jun 2023 20:24:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Jun 2023 20:24:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Jun 2023 20:24:45 GMT
USER odoo
# Thu, 29 Jun 2023 20:24:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jun 2023 20:24:45 GMT
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
	-	`sha256:c6b4cc3c5a66be69332cff7a095cb99972a06fcd8922f913c9c5da4baad90170`  
		Last Modified: Thu, 29 Jun 2023 20:27:07 GMT  
		Size: 278.5 MB (278466748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18180e32bf8d97c966b532e261acc9a551ff74a40bb732578738247379fc143c`  
		Last Modified: Thu, 29 Jun 2023 20:26:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5fbb997266c17624bb94af9b7f95db03ca45cc94da8fc1ac3cb983324efd56`  
		Last Modified: Thu, 29 Jun 2023 20:26:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f934c609f54edad5fe2aedf0897dfc7f70843b6628b3c4559c77288feca26e51`  
		Last Modified: Thu, 29 Jun 2023 20:26:35 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fe23b209027a739477acb33e621f0b0acacba366075afd23cd38b23f05baba`  
		Last Modified: Thu, 29 Jun 2023 20:26:36 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:3345864e9fe299c4d544d0af5d4794f75072bb78cc5b825737e8bd8da233fd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:070f3f5ac3d96105cc6dd5c4c7cb5b03216c5ba2835755b442a86f1893feacf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.8 MB (532786574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f04d93b28c19a4c5930c80e9b02006cabca98b05c40771e9e3931807672757`
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
# Thu, 29 Jun 2023 20:23:15 GMT
ARG ODOO_RELEASE=20230629
# Thu, 29 Jun 2023 20:23:15 GMT
ARG ODOO_SHA=621799a3ab09aacdf4139b3dbea6af48a2fb0df0
# Thu, 29 Jun 2023 20:24:40 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=621799a3ab09aacdf4139b3dbea6af48a2fb0df0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Jun 2023 20:24:44 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Jun 2023 20:24:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Jun 2023 20:24:44 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=621799a3ab09aacdf4139b3dbea6af48a2fb0df0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Jun 2023 20:24:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Jun 2023 20:24:45 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Jun 2023 20:24:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Jun 2023 20:24:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Jun 2023 20:24:45 GMT
USER odoo
# Thu, 29 Jun 2023 20:24:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jun 2023 20:24:45 GMT
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
	-	`sha256:c6b4cc3c5a66be69332cff7a095cb99972a06fcd8922f913c9c5da4baad90170`  
		Last Modified: Thu, 29 Jun 2023 20:27:07 GMT  
		Size: 278.5 MB (278466748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18180e32bf8d97c966b532e261acc9a551ff74a40bb732578738247379fc143c`  
		Last Modified: Thu, 29 Jun 2023 20:26:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5fbb997266c17624bb94af9b7f95db03ca45cc94da8fc1ac3cb983324efd56`  
		Last Modified: Thu, 29 Jun 2023 20:26:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f934c609f54edad5fe2aedf0897dfc7f70843b6628b3c4559c77288feca26e51`  
		Last Modified: Thu, 29 Jun 2023 20:26:35 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fe23b209027a739477acb33e621f0b0acacba366075afd23cd38b23f05baba`  
		Last Modified: Thu, 29 Jun 2023 20:26:36 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:f9a7e984ac356132bacbb91dd443ea3d5dc3ffba3b7fa956621ef4e610225335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:ac2491ff78b56547b6832931a2f68b4861e7f1d6ada9869973b91fac438ceb01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.6 MB (561604376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327374e713312c894013d5c5adc96da9ba2683cfa54d0e0c092374d582c3f2d1`
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
# Thu, 29 Jun 2023 20:21:51 GMT
ARG ODOO_RELEASE=20230629
# Thu, 29 Jun 2023 20:21:51 GMT
ARG ODOO_SHA=0d61fc77caa30bb4687fe3418606581f29bbb6ae
# Thu, 29 Jun 2023 20:23:06 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=0d61fc77caa30bb4687fe3418606581f29bbb6ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Jun 2023 20:23:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Jun 2023 20:23:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Jun 2023 20:23:11 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=0d61fc77caa30bb4687fe3418606581f29bbb6ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Jun 2023 20:23:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Jun 2023 20:23:11 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Jun 2023 20:23:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Jun 2023 20:23:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Jun 2023 20:23:11 GMT
USER odoo
# Thu, 29 Jun 2023 20:23:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jun 2023 20:23:11 GMT
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
	-	`sha256:b52358c09f5ed22f167d22dff547503c8e9f28b5f2e1e6284c3200e66143794c`  
		Last Modified: Thu, 29 Jun 2023 20:26:24 GMT  
		Size: 306.9 MB (306851422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c6a0f2696e285e434030a17e0f2e338746dcbc85f99402b221e4f395c64c37`  
		Last Modified: Thu, 29 Jun 2023 20:25:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8084ab1f3ac1a02179ebf7b724ce3187e7d1c51fc2cf320180c5c2b065d5048e`  
		Last Modified: Thu, 29 Jun 2023 20:25:49 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f56f70f8736da9ed478903c69a700144187f3ce8996e1c3982e7b8beaa4d4ea`  
		Last Modified: Thu, 29 Jun 2023 20:25:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8e801611095b168414ba28efab3e95fc39e4cf0b38327375e94419f2f1ef4`  
		Last Modified: Thu, 29 Jun 2023 20:25:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:f9a7e984ac356132bacbb91dd443ea3d5dc3ffba3b7fa956621ef4e610225335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:ac2491ff78b56547b6832931a2f68b4861e7f1d6ada9869973b91fac438ceb01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.6 MB (561604376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327374e713312c894013d5c5adc96da9ba2683cfa54d0e0c092374d582c3f2d1`
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
# Thu, 29 Jun 2023 20:21:51 GMT
ARG ODOO_RELEASE=20230629
# Thu, 29 Jun 2023 20:21:51 GMT
ARG ODOO_SHA=0d61fc77caa30bb4687fe3418606581f29bbb6ae
# Thu, 29 Jun 2023 20:23:06 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=0d61fc77caa30bb4687fe3418606581f29bbb6ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Jun 2023 20:23:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Jun 2023 20:23:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Jun 2023 20:23:11 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=0d61fc77caa30bb4687fe3418606581f29bbb6ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Jun 2023 20:23:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Jun 2023 20:23:11 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Jun 2023 20:23:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Jun 2023 20:23:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Jun 2023 20:23:11 GMT
USER odoo
# Thu, 29 Jun 2023 20:23:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jun 2023 20:23:11 GMT
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
	-	`sha256:b52358c09f5ed22f167d22dff547503c8e9f28b5f2e1e6284c3200e66143794c`  
		Last Modified: Thu, 29 Jun 2023 20:26:24 GMT  
		Size: 306.9 MB (306851422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c6a0f2696e285e434030a17e0f2e338746dcbc85f99402b221e4f395c64c37`  
		Last Modified: Thu, 29 Jun 2023 20:25:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8084ab1f3ac1a02179ebf7b724ce3187e7d1c51fc2cf320180c5c2b065d5048e`  
		Last Modified: Thu, 29 Jun 2023 20:25:49 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f56f70f8736da9ed478903c69a700144187f3ce8996e1c3982e7b8beaa4d4ea`  
		Last Modified: Thu, 29 Jun 2023 20:25:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8e801611095b168414ba28efab3e95fc39e4cf0b38327375e94419f2f1ef4`  
		Last Modified: Thu, 29 Jun 2023 20:25:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:655b7ba36017440c1c702248564c8e78c3a59903abedad917030b04b79bc8c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:d6bc15bf242b0d4c4889c682056c0c7df6ebd76cdeb6b98a93ed449649a8b4db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (573032206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b195402e8a2da7a606227485917b5b0ca70d7b79d07c77145175fec097db16`
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
# Wed, 14 Jun 2023 04:27:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 14 Jun 2023 04:27:35 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 04:27:37 GMT
RUN npm install -g rtlcss
# Wed, 14 Jun 2023 04:27:37 GMT
ENV ODOO_VERSION=16.0
# Thu, 29 Jun 2023 20:19:58 GMT
ARG ODOO_RELEASE=20230629
# Thu, 29 Jun 2023 20:19:58 GMT
ARG ODOO_SHA=ef1a7436be87a897efa0d0b4a50a159d2ee3e1e3
# Thu, 29 Jun 2023 20:21:34 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=ef1a7436be87a897efa0d0b4a50a159d2ee3e1e3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Jun 2023 20:21:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Jun 2023 20:21:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Jun 2023 20:21:40 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=ef1a7436be87a897efa0d0b4a50a159d2ee3e1e3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Jun 2023 20:21:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Jun 2023 20:21:40 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Jun 2023 20:21:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Jun 2023 20:21:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Jun 2023 20:21:40 GMT
USER odoo
# Thu, 29 Jun 2023 20:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jun 2023 20:21:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0150bee3cf7fd565f38365a92baed4868a70bda3097098238210c9059af7204`  
		Last Modified: Wed, 14 Jun 2023 04:32:59 GMT  
		Size: 221.0 MB (220992456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4009085967d4272bf851a9728ec147d197d9ae6a1f8df3f47bebffd2ab1a4360`  
		Last Modified: Wed, 14 Jun 2023 04:32:35 GMT  
		Size: 2.6 MB (2579555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525116348075279c320d804574bf4ecb000e0141c6da9e43d183af7422dd459e`  
		Last Modified: Wed, 14 Jun 2023 04:32:35 GMT  
		Size: 454.4 KB (454369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a9fade6e53b5222b54e7351e30c082de5e636059f9bb0e7a32a90019c27d2`  
		Last Modified: Thu, 29 Jun 2023 20:25:38 GMT  
		Size: 317.6 MB (317585951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c23228ec292daea37744ebd9ec8318b355d025e10f084cf5dc18de6063724b`  
		Last Modified: Thu, 29 Jun 2023 20:25:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477213da636d03a5a6efcf0a1b556e854fe6ac4ac2869d466841d3519dca8089`  
		Last Modified: Thu, 29 Jun 2023 20:25:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42635efe0cf6e31bfc3404a5297e07046f69c2db0a06e828cf40dcbba7217099`  
		Last Modified: Thu, 29 Jun 2023 20:25:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963553a890cd9c475345a89b090d1b4b2a6c6fbeab1fb64933271bdeb20c0705`  
		Last Modified: Thu, 29 Jun 2023 20:25:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:655b7ba36017440c1c702248564c8e78c3a59903abedad917030b04b79bc8c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:d6bc15bf242b0d4c4889c682056c0c7df6ebd76cdeb6b98a93ed449649a8b4db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (573032206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b195402e8a2da7a606227485917b5b0ca70d7b79d07c77145175fec097db16`
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
# Wed, 14 Jun 2023 04:27:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 14 Jun 2023 04:27:35 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 04:27:37 GMT
RUN npm install -g rtlcss
# Wed, 14 Jun 2023 04:27:37 GMT
ENV ODOO_VERSION=16.0
# Thu, 29 Jun 2023 20:19:58 GMT
ARG ODOO_RELEASE=20230629
# Thu, 29 Jun 2023 20:19:58 GMT
ARG ODOO_SHA=ef1a7436be87a897efa0d0b4a50a159d2ee3e1e3
# Thu, 29 Jun 2023 20:21:34 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=ef1a7436be87a897efa0d0b4a50a159d2ee3e1e3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Jun 2023 20:21:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Jun 2023 20:21:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Jun 2023 20:21:40 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=ef1a7436be87a897efa0d0b4a50a159d2ee3e1e3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Jun 2023 20:21:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Jun 2023 20:21:40 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Jun 2023 20:21:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Jun 2023 20:21:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Jun 2023 20:21:40 GMT
USER odoo
# Thu, 29 Jun 2023 20:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jun 2023 20:21:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0150bee3cf7fd565f38365a92baed4868a70bda3097098238210c9059af7204`  
		Last Modified: Wed, 14 Jun 2023 04:32:59 GMT  
		Size: 221.0 MB (220992456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4009085967d4272bf851a9728ec147d197d9ae6a1f8df3f47bebffd2ab1a4360`  
		Last Modified: Wed, 14 Jun 2023 04:32:35 GMT  
		Size: 2.6 MB (2579555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525116348075279c320d804574bf4ecb000e0141c6da9e43d183af7422dd459e`  
		Last Modified: Wed, 14 Jun 2023 04:32:35 GMT  
		Size: 454.4 KB (454369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a9fade6e53b5222b54e7351e30c082de5e636059f9bb0e7a32a90019c27d2`  
		Last Modified: Thu, 29 Jun 2023 20:25:38 GMT  
		Size: 317.6 MB (317585951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c23228ec292daea37744ebd9ec8318b355d025e10f084cf5dc18de6063724b`  
		Last Modified: Thu, 29 Jun 2023 20:25:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477213da636d03a5a6efcf0a1b556e854fe6ac4ac2869d466841d3519dca8089`  
		Last Modified: Thu, 29 Jun 2023 20:25:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42635efe0cf6e31bfc3404a5297e07046f69c2db0a06e828cf40dcbba7217099`  
		Last Modified: Thu, 29 Jun 2023 20:25:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963553a890cd9c475345a89b090d1b4b2a6c6fbeab1fb64933271bdeb20c0705`  
		Last Modified: Thu, 29 Jun 2023 20:25:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:655b7ba36017440c1c702248564c8e78c3a59903abedad917030b04b79bc8c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:d6bc15bf242b0d4c4889c682056c0c7df6ebd76cdeb6b98a93ed449649a8b4db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (573032206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b195402e8a2da7a606227485917b5b0ca70d7b79d07c77145175fec097db16`
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
# Wed, 14 Jun 2023 04:27:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 14 Jun 2023 04:27:35 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 04:27:37 GMT
RUN npm install -g rtlcss
# Wed, 14 Jun 2023 04:27:37 GMT
ENV ODOO_VERSION=16.0
# Thu, 29 Jun 2023 20:19:58 GMT
ARG ODOO_RELEASE=20230629
# Thu, 29 Jun 2023 20:19:58 GMT
ARG ODOO_SHA=ef1a7436be87a897efa0d0b4a50a159d2ee3e1e3
# Thu, 29 Jun 2023 20:21:34 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=ef1a7436be87a897efa0d0b4a50a159d2ee3e1e3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Jun 2023 20:21:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Jun 2023 20:21:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Jun 2023 20:21:40 GMT
# ARGS: ODOO_RELEASE=20230629 ODOO_SHA=ef1a7436be87a897efa0d0b4a50a159d2ee3e1e3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Jun 2023 20:21:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Jun 2023 20:21:40 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Jun 2023 20:21:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Jun 2023 20:21:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Jun 2023 20:21:40 GMT
USER odoo
# Thu, 29 Jun 2023 20:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jun 2023 20:21:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0150bee3cf7fd565f38365a92baed4868a70bda3097098238210c9059af7204`  
		Last Modified: Wed, 14 Jun 2023 04:32:59 GMT  
		Size: 221.0 MB (220992456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4009085967d4272bf851a9728ec147d197d9ae6a1f8df3f47bebffd2ab1a4360`  
		Last Modified: Wed, 14 Jun 2023 04:32:35 GMT  
		Size: 2.6 MB (2579555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525116348075279c320d804574bf4ecb000e0141c6da9e43d183af7422dd459e`  
		Last Modified: Wed, 14 Jun 2023 04:32:35 GMT  
		Size: 454.4 KB (454369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a9fade6e53b5222b54e7351e30c082de5e636059f9bb0e7a32a90019c27d2`  
		Last Modified: Thu, 29 Jun 2023 20:25:38 GMT  
		Size: 317.6 MB (317585951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c23228ec292daea37744ebd9ec8318b355d025e10f084cf5dc18de6063724b`  
		Last Modified: Thu, 29 Jun 2023 20:25:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477213da636d03a5a6efcf0a1b556e854fe6ac4ac2869d466841d3519dca8089`  
		Last Modified: Thu, 29 Jun 2023 20:25:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42635efe0cf6e31bfc3404a5297e07046f69c2db0a06e828cf40dcbba7217099`  
		Last Modified: Thu, 29 Jun 2023 20:25:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963553a890cd9c475345a89b090d1b4b2a6c6fbeab1fb64933271bdeb20c0705`  
		Last Modified: Thu, 29 Jun 2023 20:25:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
