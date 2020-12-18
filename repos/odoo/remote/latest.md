## `odoo:latest`

```console
$ docker pull odoo@sha256:081f8846546ce60f354ec74156acccd673f7b66ad42bbf2a337bec30f7431591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:1a8827774caab07a37eb451014585f9574070da3ec65044746960e513564e013
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.3 MB (404278250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c34e85682c0eec6617af427f7838e9849f21f92a3a240255e0b400c8f4b94d`
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
# Fri, 18 Dec 2020 19:53:49 GMT
ARG ODOO_RELEASE=20201218
# Fri, 18 Dec 2020 19:53:49 GMT
ARG ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
# Fri, 18 Dec 2020 19:54:43 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Dec 2020 19:54:44 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Dec 2020 19:54:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Dec 2020 19:54:45 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Dec 2020 19:54:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Dec 2020 19:54:46 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Dec 2020 19:54:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Dec 2020 19:54:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Dec 2020 19:54:46 GMT
USER odoo
# Fri, 18 Dec 2020 19:54:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Dec 2020 19:54:47 GMT
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
	-	`sha256:28ec16a7fdd6e0c0f407e3a27fd4cb3d411dbe897989b90e72943f3091c66ddb`  
		Last Modified: Fri, 18 Dec 2020 19:58:46 GMT  
		Size: 160.8 MB (160784729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0ea39d8e51a8daab3dc808a07ffe67161edb7a0a1047941222f9c49578883f`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00114de53a4a62fd509ac73e7c124f80043fab355f6ddfeb8544e3efbd8ee3aa`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c6820d46466f592923c1348b44496861a049aefdbcea8d87c4979dddd7160c`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14f21a099442af06b1adb9bfbb4cb6dd7eeef006b4ca1bf13184da39fe5ac34`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
