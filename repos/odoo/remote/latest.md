## `odoo:latest`

```console
$ docker pull odoo@sha256:8ec96bd8559e83fe003a216b4dd6ef49546a85b2c78d2dad9e92f850d34b80bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:fa320f11b5924cfcecc58226639a43b8ffcbb8a00ae448ffa5b0ecceb43dffba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546324416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5646c5d94d0de3107c5e321ba30631e3287291ece61f1558d93a24cfd41af10c`
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
# Thu, 02 Dec 2021 01:59:55 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 01:59:56 GMT
ARG ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
# Thu, 02 Dec 2021 02:01:16 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 02:01:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 02:01:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 02:01:22 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 02:01:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 02:01:22 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 02:01:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 02:01:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 02:01:23 GMT
USER odoo
# Thu, 02 Dec 2021 02:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 02:01:23 GMT
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
	-	`sha256:7ee0b1bd513bbc9b878db73bd012250e519cda964c8a1749cf3360a9347b44a7`  
		Last Modified: Thu, 02 Dec 2021 02:05:37 GMT  
		Size: 291.4 MB (291429788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace20f6a532415956863a4a803f8a562f907d26547a9a98acfaeb9b551871cec`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa763ba23682a745126c6dcafecfa139e435fce23a668ae8bb23d30e6b05e1`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246c8348bd558ab323038bbf240e76b7566f2336a212864fd4b6a6934d95e943`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d9ed61e4d29eb64d7f0be5941c9c2abebdcccf6ccf3097f016b3b59ab5e59`  
		Last Modified: Thu, 02 Dec 2021 02:05:03 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
