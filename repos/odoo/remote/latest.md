## `odoo:latest`

```console
$ docker pull odoo@sha256:fdeb9c908208a5264a63b3a10af81cfa3f72846d3d66e09bb408ca5a0c5e823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b130f5076d19102ac6145d1f4ee592808ba321243b0f6dd6cd7162e663040ae3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.4 MB (546374022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd776d1a62ba310bce6f9a2e641bf0c39ce5e3d707e9f0ebb2a0ec7e40f3cd54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:21:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:21:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:21:37 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:22:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:23:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:23:04 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:23:04 GMT
ENV ODOO_VERSION=15.0
# Mon, 20 Dec 2021 18:41:39 GMT
ARG ODOO_RELEASE=20211220
# Mon, 20 Dec 2021 18:41:39 GMT
ARG ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
# Mon, 20 Dec 2021 18:42:57 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 20 Dec 2021 18:43:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 20 Dec 2021 18:43:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 20 Dec 2021 18:43:02 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 20 Dec 2021 18:43:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 20 Dec 2021 18:43:02 GMT
EXPOSE 8069 8071 8072
# Mon, 20 Dec 2021 18:43:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 20 Dec 2021 18:43:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 20 Dec 2021 18:43:03 GMT
USER odoo
# Mon, 20 Dec 2021 18:43:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 18:43:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8928362baaf188d2d35b07907f7df5a83838f416511d7c90d1001f0f69b22d`  
		Last Modified: Thu, 02 Dec 2021 03:32:31 GMT  
		Size: 220.3 MB (220290298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1196c36b7759c2bc3f823f01785a679ef74915d5281b24e23220cfac4fb643c`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 2.5 MB (2506050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014833e3ecaf723c362d63385e2ff1ece9d0f33f6818690c2ffb8acbbc320186`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 417.8 KB (417795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d94b7f799abd1e6ed0a3b0187568e9e71a1649e8ceaa290d3615370b537012`  
		Last Modified: Mon, 20 Dec 2021 18:47:01 GMT  
		Size: 291.8 MB (291787192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f63b88d6c03cd8dd557f401530f4caac4919b47e19e96cc9260c0fc06ac246b`  
		Last Modified: Mon, 20 Dec 2021 18:46:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e15b3c19fd3b76b1766d90eafa4a9efd07fdacd839387d06b969a6ee7e495`  
		Last Modified: Mon, 20 Dec 2021 18:46:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3402a091a99587b86e7e5f1b0354bc3fdfc7e8dfc72be93f07024f7a35b6f69`  
		Last Modified: Mon, 20 Dec 2021 18:46:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efd8836eb2b0b837c81d2ec615ad9e14e771b71a526e04958113a6726684a5`  
		Last Modified: Mon, 20 Dec 2021 18:46:29 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
