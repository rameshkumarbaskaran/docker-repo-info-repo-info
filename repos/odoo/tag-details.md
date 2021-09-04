<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:12`](#odoo12)
-	[`odoo:12.0`](#odoo120)
-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:latest`](#odoolatest)

## `odoo:12`

```console
$ docker pull odoo@sha256:7f369026c8796e91563ea889279d994b167f4eaa30d3c4bc31377a5bc6fbc195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:8cf6c6ec9b07fa00beffaff717ba325a1ad5d1fdb48fe5100a5079ebc6979078
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538412724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5373e136a90f414ba890cb4d6fc4a8dd58da724337f13afdc2ee4a0c2ffe7f90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:21:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:21:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:21:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:21:43 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 03 Sep 2021 08:23:12 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:24:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:25:00 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:25:01 GMT
ENV ODOO_VERSION=12.0
# Sat, 04 Sep 2021 15:07:59 GMT
ARG ODOO_RELEASE=20210903
# Sat, 04 Sep 2021 15:07:59 GMT
ARG ODOO_SHA=9597721c9b951e32263a051a53d9a6e392eaf81b
# Sat, 04 Sep 2021 15:09:03 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=9597721c9b951e32263a051a53d9a6e392eaf81b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 04 Sep 2021 15:09:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 04 Sep 2021 15:09:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 04 Sep 2021 15:09:08 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=9597721c9b951e32263a051a53d9a6e392eaf81b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 04 Sep 2021 15:09:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 04 Sep 2021 15:09:08 GMT
EXPOSE 8069 8071 8072
# Sat, 04 Sep 2021 15:09:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 04 Sep 2021 15:09:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 04 Sep 2021 15:09:09 GMT
USER odoo
# Sat, 04 Sep 2021 15:09:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 15:09:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef1fc36ce9f3859bf889c86d8cd74979ed71ae7106adb1aad7d64adb740273`  
		Last Modified: Fri, 03 Sep 2021 08:29:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2c6c124745ce3574461d76e169045d3084e09b9c4f9a596b17659b03b4dd2`  
		Last Modified: Fri, 03 Sep 2021 08:29:29 GMT  
		Size: 219.7 MB (219657617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dde6f436aefae775b74932ee4deb96d884f715e70db318fa94b046d3080086`  
		Last Modified: Fri, 03 Sep 2021 08:29:02 GMT  
		Size: 2.2 MB (2227388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6736d7cb64ee6e1a364dcddaedf7d1e246cbf2e7cd24b3fa9c63f244fbc1b5`  
		Last Modified: Fri, 03 Sep 2021 08:29:07 GMT  
		Size: 22.0 MB (22030059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ce7dc9487789da989004d81cfe009f047be7385a86db88612c542521ce22c5`  
		Last Modified: Sat, 04 Sep 2021 15:11:28 GMT  
		Size: 272.0 MB (271967540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dacef777d3bfb9b56c73c42420295104b755ff1f5a9ac9f0c2f1069fe82593`  
		Last Modified: Sat, 04 Sep 2021 15:11:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21665e70d2f31e236ee6dbc594a0a6bcb322949907e01bee9f9205dfff6f18cb`  
		Last Modified: Sat, 04 Sep 2021 15:11:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac52c3dd9f8dedec302ca8223901747d7174374b47d861b315186c740c394e6`  
		Last Modified: Sat, 04 Sep 2021 15:11:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaea90b3f35575b99bc4268b8441bf71b45bc535654ac704fe693cc84a18ffe`  
		Last Modified: Sat, 04 Sep 2021 15:11:01 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:7f369026c8796e91563ea889279d994b167f4eaa30d3c4bc31377a5bc6fbc195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:8cf6c6ec9b07fa00beffaff717ba325a1ad5d1fdb48fe5100a5079ebc6979078
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538412724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5373e136a90f414ba890cb4d6fc4a8dd58da724337f13afdc2ee4a0c2ffe7f90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:21:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:21:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:21:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:21:43 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 03 Sep 2021 08:23:12 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:24:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:25:00 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:25:01 GMT
ENV ODOO_VERSION=12.0
# Sat, 04 Sep 2021 15:07:59 GMT
ARG ODOO_RELEASE=20210903
# Sat, 04 Sep 2021 15:07:59 GMT
ARG ODOO_SHA=9597721c9b951e32263a051a53d9a6e392eaf81b
# Sat, 04 Sep 2021 15:09:03 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=9597721c9b951e32263a051a53d9a6e392eaf81b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 04 Sep 2021 15:09:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 04 Sep 2021 15:09:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 04 Sep 2021 15:09:08 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=9597721c9b951e32263a051a53d9a6e392eaf81b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 04 Sep 2021 15:09:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 04 Sep 2021 15:09:08 GMT
EXPOSE 8069 8071 8072
# Sat, 04 Sep 2021 15:09:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 04 Sep 2021 15:09:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 04 Sep 2021 15:09:09 GMT
USER odoo
# Sat, 04 Sep 2021 15:09:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 15:09:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef1fc36ce9f3859bf889c86d8cd74979ed71ae7106adb1aad7d64adb740273`  
		Last Modified: Fri, 03 Sep 2021 08:29:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2c6c124745ce3574461d76e169045d3084e09b9c4f9a596b17659b03b4dd2`  
		Last Modified: Fri, 03 Sep 2021 08:29:29 GMT  
		Size: 219.7 MB (219657617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dde6f436aefae775b74932ee4deb96d884f715e70db318fa94b046d3080086`  
		Last Modified: Fri, 03 Sep 2021 08:29:02 GMT  
		Size: 2.2 MB (2227388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6736d7cb64ee6e1a364dcddaedf7d1e246cbf2e7cd24b3fa9c63f244fbc1b5`  
		Last Modified: Fri, 03 Sep 2021 08:29:07 GMT  
		Size: 22.0 MB (22030059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ce7dc9487789da989004d81cfe009f047be7385a86db88612c542521ce22c5`  
		Last Modified: Sat, 04 Sep 2021 15:11:28 GMT  
		Size: 272.0 MB (271967540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dacef777d3bfb9b56c73c42420295104b755ff1f5a9ac9f0c2f1069fe82593`  
		Last Modified: Sat, 04 Sep 2021 15:11:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21665e70d2f31e236ee6dbc594a0a6bcb322949907e01bee9f9205dfff6f18cb`  
		Last Modified: Sat, 04 Sep 2021 15:11:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac52c3dd9f8dedec302ca8223901747d7174374b47d861b315186c740c394e6`  
		Last Modified: Sat, 04 Sep 2021 15:11:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaea90b3f35575b99bc4268b8441bf71b45bc535654ac704fe693cc84a18ffe`  
		Last Modified: Sat, 04 Sep 2021 15:11:01 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:21d3149f6f19530327054cdf70b75b2d4f41067a4e924b225b2b99e4964d4c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:1124941872a225471198bcfe1cb371c51fc382941b774a7150b3ee46898e0c2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528444689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0016c97ecdc34a462419f638c4c4bb14ce48798d9bbd949c404c9eb8d36317b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:19:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:19:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:19:47 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:19:48 GMT
ENV ODOO_VERSION=13.0
# Sat, 04 Sep 2021 15:06:33 GMT
ARG ODOO_RELEASE=20210903
# Sat, 04 Sep 2021 15:06:33 GMT
ARG ODOO_SHA=ad7e373a34fea964e6ea1fbcb65fc3dbc566165f
# Sat, 04 Sep 2021 15:07:44 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=ad7e373a34fea964e6ea1fbcb65fc3dbc566165f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 04 Sep 2021 15:07:47 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 04 Sep 2021 15:07:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 04 Sep 2021 15:07:48 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=ad7e373a34fea964e6ea1fbcb65fc3dbc566165f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 04 Sep 2021 15:07:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 04 Sep 2021 15:07:49 GMT
EXPOSE 8069 8071 8072
# Sat, 04 Sep 2021 15:07:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 04 Sep 2021 15:07:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 04 Sep 2021 15:07:49 GMT
USER odoo
# Sat, 04 Sep 2021 15:07:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 15:07:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f62eaaa3a419466e2cd8478b7344c1acd06a6095fb959f5981431356166c72`  
		Last Modified: Fri, 03 Sep 2021 08:28:43 GMT  
		Size: 207.1 MB (207129591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564b1b987da5a51f9753c4e9903495b0b9cb9d58f79cf0e7ff747938a4237a5`  
		Last Modified: Fri, 03 Sep 2021 08:28:15 GMT  
		Size: 2.3 MB (2347919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f6c8a96ec08781ed03569e5dc126ee49838d7d7891d7606e9aa97091348ad6`  
		Last Modified: Fri, 03 Sep 2021 08:28:14 GMT  
		Size: 893.4 KB (893373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472ab35a6f1c04eab5dac5420a5c518cfca9d4539781c20398e56bc79d2f4c2`  
		Last Modified: Sat, 04 Sep 2021 15:10:50 GMT  
		Size: 290.9 MB (290925499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8a458c6ec45a92d98e774e65167f1732f7db16a210546eae9e6734146b2947`  
		Last Modified: Sat, 04 Sep 2021 15:10:19 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c560db787a2e2f17f980ec0c8049b03911b3dc3c11ea184c586e0e74c95be5`  
		Last Modified: Sat, 04 Sep 2021 15:10:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6acb875b4407207ee509a1342b3faa5985591ad4e3f6d75b7f3a39208d83b9`  
		Last Modified: Sat, 04 Sep 2021 15:10:21 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65eabbb2b8f58c9809f5d988933ea7a8f6493a9d6aef685da46930b64b14e389`  
		Last Modified: Sat, 04 Sep 2021 15:10:19 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:21d3149f6f19530327054cdf70b75b2d4f41067a4e924b225b2b99e4964d4c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:1124941872a225471198bcfe1cb371c51fc382941b774a7150b3ee46898e0c2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528444689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0016c97ecdc34a462419f638c4c4bb14ce48798d9bbd949c404c9eb8d36317b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:19:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:19:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:19:47 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:19:48 GMT
ENV ODOO_VERSION=13.0
# Sat, 04 Sep 2021 15:06:33 GMT
ARG ODOO_RELEASE=20210903
# Sat, 04 Sep 2021 15:06:33 GMT
ARG ODOO_SHA=ad7e373a34fea964e6ea1fbcb65fc3dbc566165f
# Sat, 04 Sep 2021 15:07:44 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=ad7e373a34fea964e6ea1fbcb65fc3dbc566165f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 04 Sep 2021 15:07:47 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 04 Sep 2021 15:07:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 04 Sep 2021 15:07:48 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=ad7e373a34fea964e6ea1fbcb65fc3dbc566165f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 04 Sep 2021 15:07:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 04 Sep 2021 15:07:49 GMT
EXPOSE 8069 8071 8072
# Sat, 04 Sep 2021 15:07:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 04 Sep 2021 15:07:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 04 Sep 2021 15:07:49 GMT
USER odoo
# Sat, 04 Sep 2021 15:07:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 15:07:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f62eaaa3a419466e2cd8478b7344c1acd06a6095fb959f5981431356166c72`  
		Last Modified: Fri, 03 Sep 2021 08:28:43 GMT  
		Size: 207.1 MB (207129591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564b1b987da5a51f9753c4e9903495b0b9cb9d58f79cf0e7ff747938a4237a5`  
		Last Modified: Fri, 03 Sep 2021 08:28:15 GMT  
		Size: 2.3 MB (2347919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f6c8a96ec08781ed03569e5dc126ee49838d7d7891d7606e9aa97091348ad6`  
		Last Modified: Fri, 03 Sep 2021 08:28:14 GMT  
		Size: 893.4 KB (893373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472ab35a6f1c04eab5dac5420a5c518cfca9d4539781c20398e56bc79d2f4c2`  
		Last Modified: Sat, 04 Sep 2021 15:10:50 GMT  
		Size: 290.9 MB (290925499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8a458c6ec45a92d98e774e65167f1732f7db16a210546eae9e6734146b2947`  
		Last Modified: Sat, 04 Sep 2021 15:10:19 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c560db787a2e2f17f980ec0c8049b03911b3dc3c11ea184c586e0e74c95be5`  
		Last Modified: Sat, 04 Sep 2021 15:10:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6acb875b4407207ee509a1342b3faa5985591ad4e3f6d75b7f3a39208d83b9`  
		Last Modified: Sat, 04 Sep 2021 15:10:21 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65eabbb2b8f58c9809f5d988933ea7a8f6493a9d6aef685da46930b64b14e389`  
		Last Modified: Sat, 04 Sep 2021 15:10:19 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:df2289452ac5defadc4d4b64aa97fafe7409619d38562122aba9bf4e6c4dadfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:bf6fd28fc7127a2fee59cfc05ea43432dbc679f9b7f322a269c3e292a7dcc00d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.9 MB (516894546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a893e162a95cfbdd58d5314a8063ac9feb139399e0c15d5ebe3f6ae3130838f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:15:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:16:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:16:12 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:16:13 GMT
ENV ODOO_VERSION=14.0
# Sat, 04 Sep 2021 15:05:08 GMT
ARG ODOO_RELEASE=20210903
# Sat, 04 Sep 2021 15:05:08 GMT
ARG ODOO_SHA=d16cb5f6759ab873761f1ec651df20a29de606e7
# Sat, 04 Sep 2021 15:06:16 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=d16cb5f6759ab873761f1ec651df20a29de606e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 04 Sep 2021 15:06:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 04 Sep 2021 15:06:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 04 Sep 2021 15:06:21 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=d16cb5f6759ab873761f1ec651df20a29de606e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 04 Sep 2021 15:06:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 04 Sep 2021 15:06:21 GMT
EXPOSE 8069 8071 8072
# Sat, 04 Sep 2021 15:06:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 04 Sep 2021 15:06:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 04 Sep 2021 15:06:22 GMT
USER odoo
# Sat, 04 Sep 2021 15:06:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 15:06:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747cf09456121867c9a11a2b2e1b877b80dd32b1ffe451e88685f790bd2188f6`  
		Last Modified: Fri, 03 Sep 2021 08:27:50 GMT  
		Size: 213.2 MB (213172901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c6b9c93241bd96d38967891f77680616b4df0ad6f2255bf7b4e375736d481`  
		Last Modified: Fri, 03 Sep 2021 08:27:14 GMT  
		Size: 2.4 MB (2350482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644c7d878f88578d6d5aa3edcc8f5f864b3568da52f0cbd89f566950d57bc9c8`  
		Last Modified: Fri, 03 Sep 2021 08:27:13 GMT  
		Size: 893.3 KB (893252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c8485f64c7a4d81e9442849d545cc52f0a86bbd7a20f71b93dc6f384b4aab1`  
		Last Modified: Sat, 04 Sep 2021 15:10:06 GMT  
		Size: 273.3 MB (273329611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb341f1c6781615d9bd4c76c84bb0ae211eeb6f67b62750dc6a208fdad9f05b`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73102c322f81b64d238a3b52866b0b0db16944cc0d064b462eaca2d332aaee1`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a8bd3575f13de9e74a7b673f0038ed781f55ad8d8d6e4e9c595b19282cb480`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ea1b8edd15bff4c6e462abe7c44d3239c04bad0a986405040150a56fbef0ff`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:df2289452ac5defadc4d4b64aa97fafe7409619d38562122aba9bf4e6c4dadfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:bf6fd28fc7127a2fee59cfc05ea43432dbc679f9b7f322a269c3e292a7dcc00d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.9 MB (516894546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a893e162a95cfbdd58d5314a8063ac9feb139399e0c15d5ebe3f6ae3130838f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:15:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:16:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:16:12 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:16:13 GMT
ENV ODOO_VERSION=14.0
# Sat, 04 Sep 2021 15:05:08 GMT
ARG ODOO_RELEASE=20210903
# Sat, 04 Sep 2021 15:05:08 GMT
ARG ODOO_SHA=d16cb5f6759ab873761f1ec651df20a29de606e7
# Sat, 04 Sep 2021 15:06:16 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=d16cb5f6759ab873761f1ec651df20a29de606e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 04 Sep 2021 15:06:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 04 Sep 2021 15:06:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 04 Sep 2021 15:06:21 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=d16cb5f6759ab873761f1ec651df20a29de606e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 04 Sep 2021 15:06:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 04 Sep 2021 15:06:21 GMT
EXPOSE 8069 8071 8072
# Sat, 04 Sep 2021 15:06:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 04 Sep 2021 15:06:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 04 Sep 2021 15:06:22 GMT
USER odoo
# Sat, 04 Sep 2021 15:06:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 15:06:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747cf09456121867c9a11a2b2e1b877b80dd32b1ffe451e88685f790bd2188f6`  
		Last Modified: Fri, 03 Sep 2021 08:27:50 GMT  
		Size: 213.2 MB (213172901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c6b9c93241bd96d38967891f77680616b4df0ad6f2255bf7b4e375736d481`  
		Last Modified: Fri, 03 Sep 2021 08:27:14 GMT  
		Size: 2.4 MB (2350482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644c7d878f88578d6d5aa3edcc8f5f864b3568da52f0cbd89f566950d57bc9c8`  
		Last Modified: Fri, 03 Sep 2021 08:27:13 GMT  
		Size: 893.3 KB (893252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c8485f64c7a4d81e9442849d545cc52f0a86bbd7a20f71b93dc6f384b4aab1`  
		Last Modified: Sat, 04 Sep 2021 15:10:06 GMT  
		Size: 273.3 MB (273329611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb341f1c6781615d9bd4c76c84bb0ae211eeb6f67b62750dc6a208fdad9f05b`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73102c322f81b64d238a3b52866b0b0db16944cc0d064b462eaca2d332aaee1`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a8bd3575f13de9e74a7b673f0038ed781f55ad8d8d6e4e9c595b19282cb480`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ea1b8edd15bff4c6e462abe7c44d3239c04bad0a986405040150a56fbef0ff`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:df2289452ac5defadc4d4b64aa97fafe7409619d38562122aba9bf4e6c4dadfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:bf6fd28fc7127a2fee59cfc05ea43432dbc679f9b7f322a269c3e292a7dcc00d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.9 MB (516894546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a893e162a95cfbdd58d5314a8063ac9feb139399e0c15d5ebe3f6ae3130838f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:15:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:16:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:16:12 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:16:13 GMT
ENV ODOO_VERSION=14.0
# Sat, 04 Sep 2021 15:05:08 GMT
ARG ODOO_RELEASE=20210903
# Sat, 04 Sep 2021 15:05:08 GMT
ARG ODOO_SHA=d16cb5f6759ab873761f1ec651df20a29de606e7
# Sat, 04 Sep 2021 15:06:16 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=d16cb5f6759ab873761f1ec651df20a29de606e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 04 Sep 2021 15:06:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 04 Sep 2021 15:06:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 04 Sep 2021 15:06:21 GMT
# ARGS: ODOO_RELEASE=20210903 ODOO_SHA=d16cb5f6759ab873761f1ec651df20a29de606e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 04 Sep 2021 15:06:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 04 Sep 2021 15:06:21 GMT
EXPOSE 8069 8071 8072
# Sat, 04 Sep 2021 15:06:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 04 Sep 2021 15:06:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 04 Sep 2021 15:06:22 GMT
USER odoo
# Sat, 04 Sep 2021 15:06:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 15:06:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747cf09456121867c9a11a2b2e1b877b80dd32b1ffe451e88685f790bd2188f6`  
		Last Modified: Fri, 03 Sep 2021 08:27:50 GMT  
		Size: 213.2 MB (213172901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c6b9c93241bd96d38967891f77680616b4df0ad6f2255bf7b4e375736d481`  
		Last Modified: Fri, 03 Sep 2021 08:27:14 GMT  
		Size: 2.4 MB (2350482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644c7d878f88578d6d5aa3edcc8f5f864b3568da52f0cbd89f566950d57bc9c8`  
		Last Modified: Fri, 03 Sep 2021 08:27:13 GMT  
		Size: 893.3 KB (893252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c8485f64c7a4d81e9442849d545cc52f0a86bbd7a20f71b93dc6f384b4aab1`  
		Last Modified: Sat, 04 Sep 2021 15:10:06 GMT  
		Size: 273.3 MB (273329611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb341f1c6781615d9bd4c76c84bb0ae211eeb6f67b62750dc6a208fdad9f05b`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73102c322f81b64d238a3b52866b0b0db16944cc0d064b462eaca2d332aaee1`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a8bd3575f13de9e74a7b673f0038ed781f55ad8d8d6e4e9c595b19282cb480`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ea1b8edd15bff4c6e462abe7c44d3239c04bad0a986405040150a56fbef0ff`  
		Last Modified: Sat, 04 Sep 2021 15:09:35 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
