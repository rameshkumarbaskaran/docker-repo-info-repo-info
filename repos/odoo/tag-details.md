<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:latest`](#odoolatest)

## `odoo:14`

```console
$ docker pull odoo@sha256:01ac31e43e535915f8bccd94fd97c5ea234c6f686ab1948737736a167426e5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:39b0d6fb92d30054a91404f97902dc5cd64b75dd5ce43eaf7ff5afb06e513bda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531302465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de02da95f3e58e78aaff3909c334cd7e364fd10cfd33c5b5c911c1318fe8b3fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:04:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 12:04:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 12:04:03 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:05:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:05:40 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:05:43 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:05:43 GMT
ENV ODOO_VERSION=14.0
# Wed, 21 Dec 2022 12:05:43 GMT
ARG ODOO_RELEASE=20221216
# Wed, 21 Dec 2022 12:05:43 GMT
ARG ODOO_SHA=cf0fc33d169a845691b71cc03cfbaa7787b20b04
# Wed, 21 Dec 2022 12:07:02 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=cf0fc33d169a845691b71cc03cfbaa7787b20b04
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 21 Dec 2022 12:07:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 21 Dec 2022 12:07:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 21 Dec 2022 12:07:06 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=cf0fc33d169a845691b71cc03cfbaa7787b20b04
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 21 Dec 2022 12:07:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 21 Dec 2022 12:07:07 GMT
EXPOSE 8069 8071 8072
# Wed, 21 Dec 2022 12:07:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 21 Dec 2022 12:07:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 21 Dec 2022 12:07:07 GMT
USER odoo
# Wed, 21 Dec 2022 12:07:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 12:07:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fd809e7e6338e9ff619aa861a2c83ea5794e2e9f1e27208941b0cb0830d586`  
		Last Modified: Wed, 21 Dec 2022 12:09:24 GMT  
		Size: 213.2 MB (213188652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7447a10d2ac09f77c91f4405dd22b28022ae50b65e4a89bd2b93bc773c1a76f`  
		Last Modified: Wed, 21 Dec 2022 12:09:01 GMT  
		Size: 13.5 MB (13515235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2a982470c9023112777135e16db2722d58d0e80637be6f6512ed77e73a0e45`  
		Last Modified: Wed, 21 Dec 2022 12:08:58 GMT  
		Size: 457.1 KB (457118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc61f63298ca876772764cb457a63abc14004c5b63a3b9f4cc1e753dffc7a083`  
		Last Modified: Wed, 21 Dec 2022 12:09:32 GMT  
		Size: 277.0 MB (276998668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfaffac26688106df727b7952b852902281e4002447875da02341c0c5ace5a`  
		Last Modified: Wed, 21 Dec 2022 12:08:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa009bc3c3a440fc44fd55c8b977bfce4f6ffd53e172df90474f024115b827e8`  
		Last Modified: Wed, 21 Dec 2022 12:08:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249a3acd0adea59a0b7c738f7c2f3909b92f89fa2d371ed305119764681b74ec`  
		Last Modified: Wed, 21 Dec 2022 12:08:56 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddf4a702194e590a821c17b9cddb15eb4a3c4c3d5592e756da31c219511d67e`  
		Last Modified: Wed, 21 Dec 2022 12:08:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:01ac31e43e535915f8bccd94fd97c5ea234c6f686ab1948737736a167426e5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:39b0d6fb92d30054a91404f97902dc5cd64b75dd5ce43eaf7ff5afb06e513bda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531302465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de02da95f3e58e78aaff3909c334cd7e364fd10cfd33c5b5c911c1318fe8b3fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:04:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 12:04:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 12:04:03 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:05:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:05:40 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:05:43 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:05:43 GMT
ENV ODOO_VERSION=14.0
# Wed, 21 Dec 2022 12:05:43 GMT
ARG ODOO_RELEASE=20221216
# Wed, 21 Dec 2022 12:05:43 GMT
ARG ODOO_SHA=cf0fc33d169a845691b71cc03cfbaa7787b20b04
# Wed, 21 Dec 2022 12:07:02 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=cf0fc33d169a845691b71cc03cfbaa7787b20b04
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 21 Dec 2022 12:07:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 21 Dec 2022 12:07:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 21 Dec 2022 12:07:06 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=cf0fc33d169a845691b71cc03cfbaa7787b20b04
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 21 Dec 2022 12:07:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 21 Dec 2022 12:07:07 GMT
EXPOSE 8069 8071 8072
# Wed, 21 Dec 2022 12:07:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 21 Dec 2022 12:07:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 21 Dec 2022 12:07:07 GMT
USER odoo
# Wed, 21 Dec 2022 12:07:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 12:07:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fd809e7e6338e9ff619aa861a2c83ea5794e2e9f1e27208941b0cb0830d586`  
		Last Modified: Wed, 21 Dec 2022 12:09:24 GMT  
		Size: 213.2 MB (213188652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7447a10d2ac09f77c91f4405dd22b28022ae50b65e4a89bd2b93bc773c1a76f`  
		Last Modified: Wed, 21 Dec 2022 12:09:01 GMT  
		Size: 13.5 MB (13515235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2a982470c9023112777135e16db2722d58d0e80637be6f6512ed77e73a0e45`  
		Last Modified: Wed, 21 Dec 2022 12:08:58 GMT  
		Size: 457.1 KB (457118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc61f63298ca876772764cb457a63abc14004c5b63a3b9f4cc1e753dffc7a083`  
		Last Modified: Wed, 21 Dec 2022 12:09:32 GMT  
		Size: 277.0 MB (276998668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfaffac26688106df727b7952b852902281e4002447875da02341c0c5ace5a`  
		Last Modified: Wed, 21 Dec 2022 12:08:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa009bc3c3a440fc44fd55c8b977bfce4f6ffd53e172df90474f024115b827e8`  
		Last Modified: Wed, 21 Dec 2022 12:08:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249a3acd0adea59a0b7c738f7c2f3909b92f89fa2d371ed305119764681b74ec`  
		Last Modified: Wed, 21 Dec 2022 12:08:56 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddf4a702194e590a821c17b9cddb15eb4a3c4c3d5592e756da31c219511d67e`  
		Last Modified: Wed, 21 Dec 2022 12:08:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:37cb6fff2997ce52cf3c19a9b18a12b13ecdb72778539f1f93d7033de9a26ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:923906dff3ab4a78ec9ff557084a7114ac2beed4f53cebfca338964a727dc2fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.3 MB (559311840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de57cb720c6be9ff6eb3acd2f8fdd5870a63280b5d943a9d8642db0ad60d6e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:02:25 GMT
ENV ODOO_VERSION=15.0
# Wed, 21 Dec 2022 12:02:25 GMT
ARG ODOO_RELEASE=20221216
# Wed, 21 Dec 2022 12:02:25 GMT
ARG ODOO_SHA=db18fade18d691716ccb67ddbd583e288d4762be
# Wed, 21 Dec 2022 12:03:41 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=db18fade18d691716ccb67ddbd583e288d4762be
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 21 Dec 2022 12:03:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 21 Dec 2022 12:03:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 21 Dec 2022 12:03:46 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=db18fade18d691716ccb67ddbd583e288d4762be
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 21 Dec 2022 12:03:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 21 Dec 2022 12:03:46 GMT
EXPOSE 8069 8071 8072
# Wed, 21 Dec 2022 12:03:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 21 Dec 2022 12:03:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 21 Dec 2022 12:03:46 GMT
USER odoo
# Wed, 21 Dec 2022 12:03:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 12:03:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164cd26c3f88b1b9e4962292de7e471de412ee1364ea561452c917ef547c6ec3`  
		Last Modified: Wed, 21 Dec 2022 12:08:47 GMT  
		Size: 304.6 MB (304587510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3389f6a12d5d5241707571ed751306362938f4ca4c7b298a6efbbfa8e3ace7a0`  
		Last Modified: Wed, 21 Dec 2022 12:08:11 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc15d7721c7f1b0a4b954d28b8ec89118549413c6fe0d3b48d4cbd08cabbb2d`  
		Last Modified: Wed, 21 Dec 2022 12:08:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f6cbf9986a4248db065d7f473aa9d49a39c87701148fbffbc0008927d110dc`  
		Last Modified: Wed, 21 Dec 2022 12:08:11 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00059777cde31590afc44bdfd7f25f7d2473a52f258ae2019e40144799d3fc91`  
		Last Modified: Wed, 21 Dec 2022 12:08:11 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:37cb6fff2997ce52cf3c19a9b18a12b13ecdb72778539f1f93d7033de9a26ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:923906dff3ab4a78ec9ff557084a7114ac2beed4f53cebfca338964a727dc2fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.3 MB (559311840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de57cb720c6be9ff6eb3acd2f8fdd5870a63280b5d943a9d8642db0ad60d6e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:02:25 GMT
ENV ODOO_VERSION=15.0
# Wed, 21 Dec 2022 12:02:25 GMT
ARG ODOO_RELEASE=20221216
# Wed, 21 Dec 2022 12:02:25 GMT
ARG ODOO_SHA=db18fade18d691716ccb67ddbd583e288d4762be
# Wed, 21 Dec 2022 12:03:41 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=db18fade18d691716ccb67ddbd583e288d4762be
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 21 Dec 2022 12:03:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 21 Dec 2022 12:03:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 21 Dec 2022 12:03:46 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=db18fade18d691716ccb67ddbd583e288d4762be
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 21 Dec 2022 12:03:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 21 Dec 2022 12:03:46 GMT
EXPOSE 8069 8071 8072
# Wed, 21 Dec 2022 12:03:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 21 Dec 2022 12:03:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 21 Dec 2022 12:03:46 GMT
USER odoo
# Wed, 21 Dec 2022 12:03:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 12:03:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164cd26c3f88b1b9e4962292de7e471de412ee1364ea561452c917ef547c6ec3`  
		Last Modified: Wed, 21 Dec 2022 12:08:47 GMT  
		Size: 304.6 MB (304587510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3389f6a12d5d5241707571ed751306362938f4ca4c7b298a6efbbfa8e3ace7a0`  
		Last Modified: Wed, 21 Dec 2022 12:08:11 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc15d7721c7f1b0a4b954d28b8ec89118549413c6fe0d3b48d4cbd08cabbb2d`  
		Last Modified: Wed, 21 Dec 2022 12:08:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f6cbf9986a4248db065d7f473aa9d49a39c87701148fbffbc0008927d110dc`  
		Last Modified: Wed, 21 Dec 2022 12:08:11 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00059777cde31590afc44bdfd7f25f7d2473a52f258ae2019e40144799d3fc91`  
		Last Modified: Wed, 21 Dec 2022 12:08:11 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:98f9a0383fbae13c70579ee898c240d15d3d5d1f7d034dd8dd0fdd94c7dedda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:a40dd6980e83aee6bd1c966ad22e685dabe6ee77dfae0c22fe1b3d9da5e1baf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562345616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b587792a946386677ed2a4ffb243a597029a2cff40c0c54ce946b8aca2ed9919`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:00:39 GMT
ENV ODOO_VERSION=16.0
# Wed, 21 Dec 2022 12:00:39 GMT
ARG ODOO_RELEASE=20221216
# Wed, 21 Dec 2022 12:00:39 GMT
ARG ODOO_SHA=f6aeed95ae4fe3c891fe7c35e0dc08e83553493d
# Wed, 21 Dec 2022 12:02:04 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=f6aeed95ae4fe3c891fe7c35e0dc08e83553493d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 21 Dec 2022 12:02:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 21 Dec 2022 12:02:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 21 Dec 2022 12:02:09 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=f6aeed95ae4fe3c891fe7c35e0dc08e83553493d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 21 Dec 2022 12:02:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 21 Dec 2022 12:02:09 GMT
EXPOSE 8069 8071 8072
# Wed, 21 Dec 2022 12:02:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 21 Dec 2022 12:02:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 21 Dec 2022 12:02:10 GMT
USER odoo
# Wed, 21 Dec 2022 12:02:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 12:02:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab6ea4505f13fe06b1ef42c8f2da620fc68113a6a9511a90f68736a914677f`  
		Last Modified: Wed, 21 Dec 2022 12:07:59 GMT  
		Size: 307.6 MB (307621284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f16acccaa89194857ad86d13a08f0fffa06a5b5bb1d5b0ff95773cd46d69e4`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca616ca4f935f8171f7987d90834199a9fad30c4dba7bb889d4a30a2aac0323`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87581817148689d33b310cf5a3006cb71d7345a5a6261c2e20736d7aa7df771f`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f9782a9fa0c10134a663ad3dbf29048972f43137e1a6e7ec1025ac8e3415d6`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:98f9a0383fbae13c70579ee898c240d15d3d5d1f7d034dd8dd0fdd94c7dedda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:a40dd6980e83aee6bd1c966ad22e685dabe6ee77dfae0c22fe1b3d9da5e1baf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562345616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b587792a946386677ed2a4ffb243a597029a2cff40c0c54ce946b8aca2ed9919`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:00:39 GMT
ENV ODOO_VERSION=16.0
# Wed, 21 Dec 2022 12:00:39 GMT
ARG ODOO_RELEASE=20221216
# Wed, 21 Dec 2022 12:00:39 GMT
ARG ODOO_SHA=f6aeed95ae4fe3c891fe7c35e0dc08e83553493d
# Wed, 21 Dec 2022 12:02:04 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=f6aeed95ae4fe3c891fe7c35e0dc08e83553493d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 21 Dec 2022 12:02:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 21 Dec 2022 12:02:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 21 Dec 2022 12:02:09 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=f6aeed95ae4fe3c891fe7c35e0dc08e83553493d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 21 Dec 2022 12:02:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 21 Dec 2022 12:02:09 GMT
EXPOSE 8069 8071 8072
# Wed, 21 Dec 2022 12:02:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 21 Dec 2022 12:02:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 21 Dec 2022 12:02:10 GMT
USER odoo
# Wed, 21 Dec 2022 12:02:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 12:02:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab6ea4505f13fe06b1ef42c8f2da620fc68113a6a9511a90f68736a914677f`  
		Last Modified: Wed, 21 Dec 2022 12:07:59 GMT  
		Size: 307.6 MB (307621284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f16acccaa89194857ad86d13a08f0fffa06a5b5bb1d5b0ff95773cd46d69e4`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca616ca4f935f8171f7987d90834199a9fad30c4dba7bb889d4a30a2aac0323`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87581817148689d33b310cf5a3006cb71d7345a5a6261c2e20736d7aa7df771f`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f9782a9fa0c10134a663ad3dbf29048972f43137e1a6e7ec1025ac8e3415d6`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:98f9a0383fbae13c70579ee898c240d15d3d5d1f7d034dd8dd0fdd94c7dedda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:a40dd6980e83aee6bd1c966ad22e685dabe6ee77dfae0c22fe1b3d9da5e1baf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562345616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b587792a946386677ed2a4ffb243a597029a2cff40c0c54ce946b8aca2ed9919`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:00:39 GMT
ENV ODOO_VERSION=16.0
# Wed, 21 Dec 2022 12:00:39 GMT
ARG ODOO_RELEASE=20221216
# Wed, 21 Dec 2022 12:00:39 GMT
ARG ODOO_SHA=f6aeed95ae4fe3c891fe7c35e0dc08e83553493d
# Wed, 21 Dec 2022 12:02:04 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=f6aeed95ae4fe3c891fe7c35e0dc08e83553493d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 21 Dec 2022 12:02:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 21 Dec 2022 12:02:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 21 Dec 2022 12:02:09 GMT
# ARGS: ODOO_RELEASE=20221216 ODOO_SHA=f6aeed95ae4fe3c891fe7c35e0dc08e83553493d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 21 Dec 2022 12:02:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 21 Dec 2022 12:02:09 GMT
EXPOSE 8069 8071 8072
# Wed, 21 Dec 2022 12:02:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 21 Dec 2022 12:02:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 21 Dec 2022 12:02:10 GMT
USER odoo
# Wed, 21 Dec 2022 12:02:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 12:02:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab6ea4505f13fe06b1ef42c8f2da620fc68113a6a9511a90f68736a914677f`  
		Last Modified: Wed, 21 Dec 2022 12:07:59 GMT  
		Size: 307.6 MB (307621284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f16acccaa89194857ad86d13a08f0fffa06a5b5bb1d5b0ff95773cd46d69e4`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca616ca4f935f8171f7987d90834199a9fad30c4dba7bb889d4a30a2aac0323`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87581817148689d33b310cf5a3006cb71d7345a5a6261c2e20736d7aa7df771f`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f9782a9fa0c10134a663ad3dbf29048972f43137e1a6e7ec1025ac8e3415d6`  
		Last Modified: Wed, 21 Dec 2022 12:07:21 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
