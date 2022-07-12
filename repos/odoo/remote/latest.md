## `odoo:latest`

```console
$ docker pull odoo@sha256:7f504868a038ef6ffdb21cd0157992a4a8c4786cc44338287c9c79829ba58f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:86beac119c4a2c8875beb22846589be3a4c416de72fe5932913c4e0c10f9656e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (555997148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945f4691df7b83f9262f500a4626fd95336bff3e4e819dff39a9314b0f259762`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:04:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jul 2022 05:04:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jul 2022 05:04:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 05:05:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jul 2022 05:05:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Jul 2022 05:05:45 GMT
ENV ODOO_VERSION=15.0
# Tue, 12 Jul 2022 05:05:45 GMT
ARG ODOO_RELEASE=20220708
# Tue, 12 Jul 2022 05:05:45 GMT
ARG ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
# Tue, 12 Jul 2022 05:07:00 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jul 2022 05:07:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Jul 2022 05:07:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jul 2022 05:07:04 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jul 2022 05:07:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jul 2022 05:07:05 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jul 2022 05:07:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jul 2022 05:07:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jul 2022 05:07:05 GMT
USER odoo
# Tue, 12 Jul 2022 05:07:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jul 2022 05:07:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd973b6810fdbba62ef6caa3ec20f653447cd19ce0363dc02605f788609e3250`  
		Last Modified: Tue, 12 Jul 2022 05:14:24 GMT  
		Size: 220.3 MB (220289612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f428c41f4b038745626ff998e2d14ffd12d10db8fd0ca26db599d6427281e19`  
		Last Modified: Tue, 12 Jul 2022 05:13:58 GMT  
		Size: 2.5 MB (2513248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb3d7b1346d040310c399b056054bed18f042bdc35c215a26e90aaa77cc27c0`  
		Last Modified: Tue, 12 Jul 2022 05:13:58 GMT  
		Size: 500.9 KB (500921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef71235ae8aed2a0852fac4e0bb02ec93adb286841ec0b1116b1c91bec4ebd94`  
		Last Modified: Tue, 12 Jul 2022 05:14:32 GMT  
		Size: 301.3 MB (301324297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1f6abab6ef9b470c117bf9f8e500212183ab5296b3893c89567724a918277`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fe699d0f7d0e568d895d7b54d49852a77d728947b1808168f079b77e1f3f1`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d92d364f0ec62e24e0b325c6d6c352966a63d091e9aebf9ff42f68b30f0b19`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d468e3f46819db39e9e41b14d2ae73b47cea5c4a7d0402da22885a0bc448bd94`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
