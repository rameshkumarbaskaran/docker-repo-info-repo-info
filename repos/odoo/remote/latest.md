## `odoo:latest`

```console
$ docker pull odoo@sha256:a031c56ca922d2d6261068a8683ff41bb3b6801fd62ebbd55ae6b4f9b6ea2191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:68b80fe23c7628e9c5598c9cbf691d152b18be1e5ccbf1bfd82695c8a9f1d3be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557834753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64086f4235b99e4fb0fb905f1faa7fea2947dad926e6117b5e073f9ee8a4d33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:49:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:49:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:49:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:50:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:51:11 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:51:11 GMT
ENV ODOO_VERSION=15.0
# Tue, 13 Sep 2022 06:51:12 GMT
ARG ODOO_RELEASE=20220902
# Tue, 13 Sep 2022 06:51:12 GMT
ARG ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
# Tue, 13 Sep 2022 06:52:32 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Sep 2022 06:52:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Sep 2022 06:52:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Sep 2022 06:52:37 GMT
# ARGS: ODOO_RELEASE=20220902 ODOO_SHA=f08078727fff11b2e0778627c476e7b95cbebdea
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Sep 2022 06:52:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Sep 2022 06:52:37 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Sep 2022 06:52:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Sep 2022 06:52:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Sep 2022 06:52:37 GMT
USER odoo
# Tue, 13 Sep 2022 06:52:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Sep 2022 06:52:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b73f80e874fc2998c5758d4c8d65d96b8f9ff5544bf075b31ed62614eb1071b`  
		Last Modified: Tue, 13 Sep 2022 06:59:13 GMT  
		Size: 220.3 MB (220296011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc15e3be86616ca7da0dcee3866c41e512cc3db88484000d55cc15b194c5b4`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 2.5 MB (2513532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69e7aa750a4c8478c7e63dba1a777a14a00d608706683711ced35910615545`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 449.9 KB (449869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2abdba36a6b1b535554ad4234b99333c91ec73ea7bb7930ef3a5100514d54e1`  
		Last Modified: Tue, 13 Sep 2022 06:59:21 GMT  
		Size: 303.2 MB (303168757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1391fd906b3ad65b2ef8480014aec6e6db9814f08616915ce9ec33f6a62b69a1`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05780b88ded15ca7f26ad55d1e7577d8c58ab7ab00882e8051e19156c26a7f84`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52439d711f43551963deeae77d923287e6c8f67e178ca198ce9ab7bde53d7522`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd51f312699a823b9e7188fe18575bb0016162a05e2524b322dac8412751bc1`  
		Last Modified: Tue, 13 Sep 2022 06:58:44 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
