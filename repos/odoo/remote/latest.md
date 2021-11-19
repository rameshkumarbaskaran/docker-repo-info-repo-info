## `odoo:latest`

```console
$ docker pull odoo@sha256:736d410197cb100640b709a3058076fe7ac699c5a1594229c4079437736c4da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:66206450e7e099006be4654c11f7221215a0f2f58752970e5ff5a9ff875c77e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.6 MB (543620513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd1d3fdb0cb60b575c5151166e3707e773436922677c3d169a61fee0eba853a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:10:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Nov 2021 09:10:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Nov 2021 09:10:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:11:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Nov 2021 09:11:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:11:39 GMT
RUN npm install -g rtlcss
# Wed, 17 Nov 2021 09:11:39 GMT
ENV ODOO_VERSION=15.0
# Fri, 19 Nov 2021 21:19:51 GMT
ARG ODOO_RELEASE=20211119
# Fri, 19 Nov 2021 21:19:51 GMT
ARG ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
# Fri, 19 Nov 2021 21:21:07 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Nov 2021 21:21:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Nov 2021 21:21:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Nov 2021 21:21:12 GMT
# ARGS: ODOO_RELEASE=20211119 ODOO_SHA=19307c2187ec410e8fd945eac94893c8d245084f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Nov 2021 21:21:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Nov 2021 21:21:13 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Nov 2021 21:21:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Nov 2021 21:21:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Nov 2021 21:21:13 GMT
USER odoo
# Fri, 19 Nov 2021 21:21:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 21:21:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9400c757421e2063937e8b190c956fdda2687c92c013b5eff83fe1c61c0c2c8f`  
		Last Modified: Wed, 17 Nov 2021 09:20:38 GMT  
		Size: 220.3 MB (220291328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d1a3d79ceb0d2f1f442648da0e6ece72782b8656e052f0867231839dd0b0`  
		Last Modified: Wed, 17 Nov 2021 09:19:52 GMT  
		Size: 2.5 MB (2506093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9605eabe13664e4a62ea8056b48e7547ab78dad77c977652bc44a6e8e1e30d0`  
		Last Modified: Wed, 17 Nov 2021 09:19:51 GMT  
		Size: 724.5 KB (724479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b2a2b4cb7c943436d010061509f9e829f1d2b3a126693a51d6278e8c9e6a09`  
		Last Modified: Fri, 19 Nov 2021 21:24:58 GMT  
		Size: 288.7 MB (288725881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a504116b95e7a61b0655c01aa36fe96f4fa88fc75405158f0f93a7fbbdb2ac1`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7082a4e0e2488274559e0217b2fbe37407bf2fd954ef036385a0317c5dfb2691`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d675b10459be646feabe781878354971c3e484d3c0786c1abbd9104a834abc3f`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9128e3ab01360f00ee5f7d9ae23339f7a9e2330af685b34c94430189ec992bc2`  
		Last Modified: Fri, 19 Nov 2021 21:24:26 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
