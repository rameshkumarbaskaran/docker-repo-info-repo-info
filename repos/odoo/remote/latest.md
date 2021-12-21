## `odoo:latest`

```console
$ docker pull odoo@sha256:af1c1767faca2249a67560e30b7f0e96a9413dfe15160dbb3709cf3800069487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b0166c884d85ccf99fcc29f0f0ffe9d61b56a54e2b2c50bc0e388cdbf115ba52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.4 MB (546360735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3c963a9620306c5ac3ea03eb18228552b2ae18e20a8337372f84f3f8a81d0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:16:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:16:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:16:14 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:17:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:17:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:17:51 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:17:51 GMT
ENV ODOO_VERSION=15.0
# Tue, 21 Dec 2021 19:17:52 GMT
ARG ODOO_RELEASE=20211220
# Tue, 21 Dec 2021 19:17:52 GMT
ARG ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
# Tue, 21 Dec 2021 19:19:48 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Dec 2021 19:19:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Dec 2021 19:19:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Dec 2021 19:19:54 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Dec 2021 19:19:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Dec 2021 19:19:54 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Dec 2021 19:19:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Dec 2021 19:19:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Dec 2021 19:19:55 GMT
USER odoo
# Tue, 21 Dec 2021 19:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 19:19:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18f47f481fcbd4d626a886574914b5046fe3d49070c6a0a31cd83608a315562`  
		Last Modified: Tue, 21 Dec 2021 19:27:38 GMT  
		Size: 220.3 MB (220290625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60111a5713506722102fe10c4473131ef16d2d04c11aa7f95ab5a23f3a71755e`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 2.5 MB (2506156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454f9f25d81ee861429e96088735eecd4428b8c3276b2d2c397ff274383b7b27`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 417.5 KB (417452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353f3d83812684614d191ce37d8351e75f8e0b3f4a147aba8a5f5d4bc9eecb41`  
		Last Modified: Tue, 21 Dec 2021 19:27:45 GMT  
		Size: 291.8 MB (291786418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372b4d0f6796c8a803f948792e7d7674e70e3b8958240f0f534651aecc8a5666`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75082d4cef54dcaba9f83fbdf124d9064d016a1212a14844ef7c97c91a0b12`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2beb32d152bea1f6af261c3b25178d862454a5e68967285f786a96396586e4`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4f367689813caa53e78c047671fb76eaa6cb25b67da621117a4ed4720e866c`  
		Last Modified: Tue, 21 Dec 2021 19:27:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
