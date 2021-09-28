## `odoo:latest`

```console
$ docker pull odoo@sha256:0123fb5ec226a75b4c6f3166c6ebee8c133adea50efb49378b1e5b6a52dab16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:d4671d3fbde2e39f434959f01b91f6551eab2ba7343c287d0eb9a017424c6d8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (516997258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f53998176ca6ea910168fca4d57a2520518de2052b41f6526900f2003978fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:57:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 28 Sep 2021 08:57:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 28 Sep 2021 08:57:31 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 08:59:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 28 Sep 2021 08:59:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 08:59:24 GMT
RUN npm install -g rtlcss
# Tue, 28 Sep 2021 08:59:24 GMT
ENV ODOO_VERSION=14.0
# Tue, 28 Sep 2021 08:59:24 GMT
ARG ODOO_RELEASE=20210921
# Tue, 28 Sep 2021 08:59:24 GMT
ARG ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
# Tue, 28 Sep 2021 09:00:38 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Sep 2021 09:00:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Sep 2021 09:00:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Sep 2021 09:00:43 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Sep 2021 09:00:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Sep 2021 09:00:43 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Sep 2021 09:00:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Sep 2021 09:00:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Sep 2021 09:00:44 GMT
USER odoo
# Tue, 28 Sep 2021 09:00:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 09:00:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4202cc4801528046f1295d1e9fde12d1ca51922bb3bbb78f28414392e496affb`  
		Last Modified: Tue, 28 Sep 2021 09:10:33 GMT  
		Size: 213.2 MB (213172416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f9940244ebdbb6e2808ac61f977f7a881c116cf6b1a5ff5400656affb2122`  
		Last Modified: Tue, 28 Sep 2021 09:10:05 GMT  
		Size: 2.4 MB (2350586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07d3bb02ae4b65c91447226f5c9402577d6f42a0cc8060e112b073485266a8`  
		Last Modified: Tue, 28 Sep 2021 09:10:05 GMT  
		Size: 882.7 KB (882660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b79eecf29fa0fb1a9bb616898f6ac47b44549f8376427246889b4a13aeb6007`  
		Last Modified: Tue, 28 Sep 2021 09:10:40 GMT  
		Size: 273.4 MB (273443143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666b37ca5246526d8c602ce02dc80380f82fa333de01bb48063a3675d5b12fd4`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbac68a7e779e4d5d201f4f1a81aaadcf5a4d0be5e7edb041e1df9639d8c2f9`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1329d58b792ba188877914ebda45349a38eea132d7dfd5f1bed26948e522f62`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b366991d41c0934ac1a1421f007ad21ff87ec7c19018012471bc443f50af2a7`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
