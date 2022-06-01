## `odoo:latest`

```console
$ docker pull odoo@sha256:319a8380299d6bfb2c91ab502dd3c5ed1fbd4473ae53cdfa8c6a09d9850a1ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:8e7af29884eca907e9aba2b0708e813ad7122e415c91283f7b07500d15176247
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.5 MB (555505905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efbf7ab8133c1f9075d549c0c1391b903ded05974397edcc081f467d3a9a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Tue, 31 May 2022 23:41:44 GMT
ARG ODOO_RELEASE=20220531
# Tue, 31 May 2022 23:41:44 GMT
ARG ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
# Tue, 31 May 2022 23:43:03 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 May 2022 23:43:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 31 May 2022 23:43:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 May 2022 23:43:08 GMT
# ARGS: ODOO_RELEASE=20220531 ODOO_SHA=a7011fdc43d565203812612ba28e601d7038ba0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 May 2022 23:43:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 May 2022 23:43:08 GMT
EXPOSE 8069 8071 8072
# Tue, 31 May 2022 23:43:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 May 2022 23:43:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 May 2022 23:43:09 GMT
USER odoo
# Tue, 31 May 2022 23:43:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 May 2022 23:43:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe67b31b4a5d6e70f802e329f746cc5eb83b5f4d7308f659a275e0d4e95ed98`  
		Last Modified: Tue, 31 May 2022 23:46:53 GMT  
		Size: 300.8 MB (300828310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b92606d73201d0611ce0ab91b00bcb675da44dfe47e6050763807c40a8b4535`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dcb455fed951bc0539d10ae1963ad5d43645245cc0e4924e5c1d3ef03fd588`  
		Last Modified: Tue, 31 May 2022 23:46:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f50b42ae4fae483f6da3a48796adab460af20bb8553f0049b33b6eed11ef06`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe14c42b771b8bb1cf5bc12be1bd5184ce631d417af78b4f056d4f1ca75ad69`  
		Last Modified: Tue, 31 May 2022 23:46:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
