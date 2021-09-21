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
$ docker pull odoo@sha256:e38d31f6c29ebfad6563fed1c2a87e690973d560d1dd4e735ed6648453b49f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:fb26007018accdce6fc434bcb96b742d8e509f303d0b066c85abb6896b5f58c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538424467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e7387c57945799d79216bb37c6784337cbc91c794e7691c471f162319f3ac3`
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
# Tue, 21 Sep 2021 19:23:10 GMT
ARG ODOO_RELEASE=20210921
# Tue, 21 Sep 2021 19:23:11 GMT
ARG ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
# Tue, 21 Sep 2021 19:24:15 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Sep 2021 19:24:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Sep 2021 19:24:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Sep 2021 19:24:19 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Sep 2021 19:24:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Sep 2021 19:24:19 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Sep 2021 19:24:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Sep 2021 19:24:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Sep 2021 19:24:20 GMT
USER odoo
# Tue, 21 Sep 2021 19:24:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Sep 2021 19:24:20 GMT
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
	-	`sha256:1f3f84a7254cc640a7113672935884e3e61fb123ec3999cbbe732e1d62a20d51`  
		Last Modified: Tue, 21 Sep 2021 19:26:44 GMT  
		Size: 272.0 MB (271979279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5f3b1de7674686f64a8c69611647bef9f5f0042b64b56eee5c15a1268e6338`  
		Last Modified: Tue, 21 Sep 2021 19:26:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d448dddd876ece05ac9bdce9f21a6c68c0f3f62d0441e1b67cc1c79907235`  
		Last Modified: Tue, 21 Sep 2021 19:26:16 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede1b69bc93be72c02a47a106f4d9bd29f12afb65507306dd2edd158ad89355`  
		Last Modified: Tue, 21 Sep 2021 19:26:16 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9947e2314bd095da5acbf2e50ffd80f2d871cb2a24186a04143ce74276446c7`  
		Last Modified: Tue, 21 Sep 2021 19:26:16 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:e38d31f6c29ebfad6563fed1c2a87e690973d560d1dd4e735ed6648453b49f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:fb26007018accdce6fc434bcb96b742d8e509f303d0b066c85abb6896b5f58c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538424467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e7387c57945799d79216bb37c6784337cbc91c794e7691c471f162319f3ac3`
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
# Tue, 21 Sep 2021 19:23:10 GMT
ARG ODOO_RELEASE=20210921
# Tue, 21 Sep 2021 19:23:11 GMT
ARG ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
# Tue, 21 Sep 2021 19:24:15 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Sep 2021 19:24:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Sep 2021 19:24:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Sep 2021 19:24:19 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Sep 2021 19:24:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Sep 2021 19:24:19 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Sep 2021 19:24:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Sep 2021 19:24:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Sep 2021 19:24:20 GMT
USER odoo
# Tue, 21 Sep 2021 19:24:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Sep 2021 19:24:20 GMT
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
	-	`sha256:1f3f84a7254cc640a7113672935884e3e61fb123ec3999cbbe732e1d62a20d51`  
		Last Modified: Tue, 21 Sep 2021 19:26:44 GMT  
		Size: 272.0 MB (271979279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5f3b1de7674686f64a8c69611647bef9f5f0042b64b56eee5c15a1268e6338`  
		Last Modified: Tue, 21 Sep 2021 19:26:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d448dddd876ece05ac9bdce9f21a6c68c0f3f62d0441e1b67cc1c79907235`  
		Last Modified: Tue, 21 Sep 2021 19:26:16 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede1b69bc93be72c02a47a106f4d9bd29f12afb65507306dd2edd158ad89355`  
		Last Modified: Tue, 21 Sep 2021 19:26:16 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9947e2314bd095da5acbf2e50ffd80f2d871cb2a24186a04143ce74276446c7`  
		Last Modified: Tue, 21 Sep 2021 19:26:16 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:0028355628fe056f737c9f4f2a4527ffe7d16342383f623c70987e55ac12a540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:8ec0c6787d27fdcf1b9233466dee87532369e134b72073257da5b07d4ead4d6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528477988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f827ee4ea7d982aa61ab84bcae91ab2c06fd53345c95524bb5ab5f29d33145e`
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
# Tue, 21 Sep 2021 19:21:45 GMT
ARG ODOO_RELEASE=20210921
# Tue, 21 Sep 2021 19:21:45 GMT
ARG ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
# Tue, 21 Sep 2021 19:22:55 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Sep 2021 19:22:58 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Sep 2021 19:22:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Sep 2021 19:22:59 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Sep 2021 19:23:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Sep 2021 19:23:00 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Sep 2021 19:23:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Sep 2021 19:23:00 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Sep 2021 19:23:00 GMT
USER odoo
# Tue, 21 Sep 2021 19:23:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Sep 2021 19:23:01 GMT
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
	-	`sha256:efa8035022e9cdf2a9c4cf558bdb6fe05a018ea07951d2c3840aa3d2679a8c1c`  
		Last Modified: Tue, 21 Sep 2021 19:26:05 GMT  
		Size: 291.0 MB (290958803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98362d1d65a0b3a79718e9488e13709a67d1d43e7111ceaa6997ec007180ce41`  
		Last Modified: Tue, 21 Sep 2021 19:25:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ff54b4aad4c08cdfac3bd763e22fe4fae53ad16ca62be4ea0da42973ff870`  
		Last Modified: Tue, 21 Sep 2021 19:25:35 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9414d8ddeb537af41fde5f34b6fe751d855d58ef9fd042ac3156e0b9a66a487a`  
		Last Modified: Tue, 21 Sep 2021 19:25:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e748eccac9debd43d6d30333460398295c19b82a1e5e9bf241f5bacf6c754bf`  
		Last Modified: Tue, 21 Sep 2021 19:25:35 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:0028355628fe056f737c9f4f2a4527ffe7d16342383f623c70987e55ac12a540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:8ec0c6787d27fdcf1b9233466dee87532369e134b72073257da5b07d4ead4d6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528477988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f827ee4ea7d982aa61ab84bcae91ab2c06fd53345c95524bb5ab5f29d33145e`
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
# Tue, 21 Sep 2021 19:21:45 GMT
ARG ODOO_RELEASE=20210921
# Tue, 21 Sep 2021 19:21:45 GMT
ARG ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
# Tue, 21 Sep 2021 19:22:55 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Sep 2021 19:22:58 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Sep 2021 19:22:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Sep 2021 19:22:59 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Sep 2021 19:23:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Sep 2021 19:23:00 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Sep 2021 19:23:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Sep 2021 19:23:00 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Sep 2021 19:23:00 GMT
USER odoo
# Tue, 21 Sep 2021 19:23:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Sep 2021 19:23:01 GMT
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
	-	`sha256:efa8035022e9cdf2a9c4cf558bdb6fe05a018ea07951d2c3840aa3d2679a8c1c`  
		Last Modified: Tue, 21 Sep 2021 19:26:05 GMT  
		Size: 291.0 MB (290958803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98362d1d65a0b3a79718e9488e13709a67d1d43e7111ceaa6997ec007180ce41`  
		Last Modified: Tue, 21 Sep 2021 19:25:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ff54b4aad4c08cdfac3bd763e22fe4fae53ad16ca62be4ea0da42973ff870`  
		Last Modified: Tue, 21 Sep 2021 19:25:35 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9414d8ddeb537af41fde5f34b6fe751d855d58ef9fd042ac3156e0b9a66a487a`  
		Last Modified: Tue, 21 Sep 2021 19:25:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e748eccac9debd43d6d30333460398295c19b82a1e5e9bf241f5bacf6c754bf`  
		Last Modified: Tue, 21 Sep 2021 19:25:35 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:ef6fce135de53b1e78191a9ff9047a7a778d4388b5a409e97056d42c28cbf859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:8eb51c2b46fcb47204786c3f48d0ca6e62967e68a271de78552fab5c0193b5fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (517005185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b2cc292b613c07a191e35293e4d70c465d9c8caf4cc80fd672cd22553cd22a`
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
# Tue, 21 Sep 2021 19:20:19 GMT
ARG ODOO_RELEASE=20210921
# Tue, 21 Sep 2021 19:20:19 GMT
ARG ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
# Tue, 21 Sep 2021 19:21:29 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Sep 2021 19:21:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Sep 2021 19:21:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Sep 2021 19:21:34 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Sep 2021 19:21:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Sep 2021 19:21:34 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Sep 2021 19:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Sep 2021 19:21:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Sep 2021 19:21:35 GMT
USER odoo
# Tue, 21 Sep 2021 19:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Sep 2021 19:21:35 GMT
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
	-	`sha256:229a2308410b5d9cdb62761b4e83c187a5a954196cca60fd9fca9ce67b9ee38f`  
		Last Modified: Tue, 21 Sep 2021 19:25:22 GMT  
		Size: 273.4 MB (273440243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb19017c56ec81a9816d36226c0d3aaea446ff79e71fc6e7731e4fd0fbb1010d`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807803fa5026c236548317c37f5399768ed6f1d5de47cf978d069e69663bb038`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde287a4ccd11f4ba81a1f26e890c4e35495c1cdd7e5d8ae1396068421145fe8`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c3b40f6f9a5c96421efa60f6a9f31c22a71e5aa3d4269a8dda014a4c8076b`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:ef6fce135de53b1e78191a9ff9047a7a778d4388b5a409e97056d42c28cbf859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:8eb51c2b46fcb47204786c3f48d0ca6e62967e68a271de78552fab5c0193b5fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (517005185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b2cc292b613c07a191e35293e4d70c465d9c8caf4cc80fd672cd22553cd22a`
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
# Tue, 21 Sep 2021 19:20:19 GMT
ARG ODOO_RELEASE=20210921
# Tue, 21 Sep 2021 19:20:19 GMT
ARG ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
# Tue, 21 Sep 2021 19:21:29 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Sep 2021 19:21:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Sep 2021 19:21:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Sep 2021 19:21:34 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Sep 2021 19:21:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Sep 2021 19:21:34 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Sep 2021 19:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Sep 2021 19:21:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Sep 2021 19:21:35 GMT
USER odoo
# Tue, 21 Sep 2021 19:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Sep 2021 19:21:35 GMT
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
	-	`sha256:229a2308410b5d9cdb62761b4e83c187a5a954196cca60fd9fca9ce67b9ee38f`  
		Last Modified: Tue, 21 Sep 2021 19:25:22 GMT  
		Size: 273.4 MB (273440243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb19017c56ec81a9816d36226c0d3aaea446ff79e71fc6e7731e4fd0fbb1010d`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807803fa5026c236548317c37f5399768ed6f1d5de47cf978d069e69663bb038`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde287a4ccd11f4ba81a1f26e890c4e35495c1cdd7e5d8ae1396068421145fe8`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c3b40f6f9a5c96421efa60f6a9f31c22a71e5aa3d4269a8dda014a4c8076b`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:ef6fce135de53b1e78191a9ff9047a7a778d4388b5a409e97056d42c28cbf859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:8eb51c2b46fcb47204786c3f48d0ca6e62967e68a271de78552fab5c0193b5fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (517005185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b2cc292b613c07a191e35293e4d70c465d9c8caf4cc80fd672cd22553cd22a`
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
# Tue, 21 Sep 2021 19:20:19 GMT
ARG ODOO_RELEASE=20210921
# Tue, 21 Sep 2021 19:20:19 GMT
ARG ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
# Tue, 21 Sep 2021 19:21:29 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Sep 2021 19:21:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Sep 2021 19:21:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Sep 2021 19:21:34 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Sep 2021 19:21:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Sep 2021 19:21:34 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Sep 2021 19:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Sep 2021 19:21:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Sep 2021 19:21:35 GMT
USER odoo
# Tue, 21 Sep 2021 19:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Sep 2021 19:21:35 GMT
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
	-	`sha256:229a2308410b5d9cdb62761b4e83c187a5a954196cca60fd9fca9ce67b9ee38f`  
		Last Modified: Tue, 21 Sep 2021 19:25:22 GMT  
		Size: 273.4 MB (273440243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb19017c56ec81a9816d36226c0d3aaea446ff79e71fc6e7731e4fd0fbb1010d`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807803fa5026c236548317c37f5399768ed6f1d5de47cf978d069e69663bb038`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde287a4ccd11f4ba81a1f26e890c4e35495c1cdd7e5d8ae1396068421145fe8`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c3b40f6f9a5c96421efa60f6a9f31c22a71e5aa3d4269a8dda014a4c8076b`  
		Last Modified: Tue, 21 Sep 2021 19:24:50 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
