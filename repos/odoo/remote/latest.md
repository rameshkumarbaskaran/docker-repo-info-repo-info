## `odoo:latest`

```console
$ docker pull odoo@sha256:02bdcf58a3801d13f62fa2ade4a183e4bfbfb056fee9ed64c06c45e24eab4687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:23dfc9de3548f16817fe648a0dda17c566faa31ae806bf53281f1f74e886edd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.4 MB (404367818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147ca9fc691922defa55503b41157dffd74d146003953c932fc584fc259e3ca2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:17:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:17:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:17:16 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:17:16 GMT
ENV ODOO_VERSION=14.0
# Mon, 04 Jan 2021 18:22:01 GMT
ARG ODOO_RELEASE=20210104
# Mon, 04 Jan 2021 18:22:02 GMT
ARG ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
# Mon, 04 Jan 2021 18:23:00 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 04 Jan 2021 18:23:01 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 04 Jan 2021 18:23:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 04 Jan 2021 18:23:02 GMT
# ARGS: ODOO_RELEASE=20210104 ODOO_SHA=4f669f6ef2e7474aa1bda52d9d5c25f1ee678520
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 04 Jan 2021 18:23:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 Jan 2021 18:23:02 GMT
EXPOSE 8069 8071 8072
# Mon, 04 Jan 2021 18:23:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 Jan 2021 18:23:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 04 Jan 2021 18:23:03 GMT
USER odoo
# Mon, 04 Jan 2021 18:23:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Jan 2021 18:23:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bc76188888637b8d6d4343790322715f6ff67e2f556d95ba4007bba46aa4b4`  
		Last Modified: Fri, 11 Dec 2020 17:26:02 GMT  
		Size: 213.1 MB (213118166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1489eaa0a91c1579cd0b86042b35ce651421b6d4be8baac3ff6f5e28fc88b423`  
		Last Modified: Fri, 11 Dec 2020 17:25:21 GMT  
		Size: 2.3 MB (2346249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8179dcb4a5c98894d38fdcf9748cbea2ad22a70c2b85c8118ca1f2f23e42afe1`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 927.4 KB (927408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82fbb70cacb8b09b8fb9a8d04fda82f6540427fc50545a0a676139bba4a4a186`  
		Last Modified: Mon, 04 Jan 2021 18:26:05 GMT  
		Size: 160.9 MB (160874293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599b946630292f82db18c345e9ec3a140ff7e812b12ee9d98133a59530046de9`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c8bcdc0422486b06953fe304dee0bb7b18eeaa78c26b5135278c2b724f955e`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa23a330216453fefb15e67922a055fe1541489b613804acbd14f94f51e22c5d`  
		Last Modified: Mon, 04 Jan 2021 18:25:34 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd1dc685ce01a39daccda579f6ff9adff94ced9efc19811e2f6153f9a8f58de`  
		Last Modified: Mon, 04 Jan 2021 18:25:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
