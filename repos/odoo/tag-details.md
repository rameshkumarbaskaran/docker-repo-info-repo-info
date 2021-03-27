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
$ docker pull odoo@sha256:e7d33c11165e216ea387c2ecb27ed548ecfdba4b73a1133e0a780986e155b802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:aad88142399be179b3dcaa035a18f1a79bb62dc50e349e255e2663cdd45c3684
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542559413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8e2a1935555ac8ff4f86f617137a0d84e38af35675a10525fc3706fe4db893`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:15:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:15:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:15:29 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:15:30 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 27 Mar 2021 06:17:31 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:17:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:17:58 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:17:58 GMT
ENV ODOO_VERSION=12.0
# Sat, 27 Mar 2021 06:17:58 GMT
ARG ODOO_RELEASE=20210318
# Sat, 27 Mar 2021 06:17:58 GMT
ARG ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
# Sat, 27 Mar 2021 06:19:06 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 27 Mar 2021 06:19:09 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 27 Mar 2021 06:19:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 27 Mar 2021 06:19:10 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 27 Mar 2021 06:19:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 27 Mar 2021 06:19:11 GMT
EXPOSE 8069 8071 8072
# Sat, 27 Mar 2021 06:19:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 27 Mar 2021 06:19:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 27 Mar 2021 06:19:11 GMT
USER odoo
# Sat, 27 Mar 2021 06:19:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 06:19:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d85905ea21b22f3cf49d1544d54fa33de25fbd3fb032724098214829848cb7e`  
		Last Modified: Sat, 27 Mar 2021 06:22:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997e5ef07b089b7d6a8a1ab2cc7851f20c4bd8eab43877b4e69f39d90aa2dacd`  
		Last Modified: Sat, 27 Mar 2021 06:22:45 GMT  
		Size: 219.7 MB (219658920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03046533a143ccada4bcf38fe3cf27238bf9807d1705bd7f63fbb7c99d17accc`  
		Last Modified: Sat, 27 Mar 2021 06:22:02 GMT  
		Size: 2.2 MB (2224133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555b0321ec586fdb7780ba6462caba21fe7328c3b6971007ffb99e4c1d83212e`  
		Last Modified: Sat, 27 Mar 2021 06:22:11 GMT  
		Size: 22.1 MB (22053347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbd16047d0f141cdcb76d0aebba6ed5006df30a185e7ff158aa389306772ca7`  
		Last Modified: Sat, 27 Mar 2021 06:22:52 GMT  
		Size: 276.1 MB (276091950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83cc2e108b31ad343da784db4a76c5c6967cbb10cd185a14973212724a0d07c`  
		Last Modified: Sat, 27 Mar 2021 06:21:59 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f0278cbdf63c9651ad421d27bf1ea89f46c6df99981dd54579a884a4b13f4`  
		Last Modified: Sat, 27 Mar 2021 06:22:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30e2d4c7c1a7aa86b34d49812cf19c686cd3657b57cf25bd687b4ea2bde6c2`  
		Last Modified: Sat, 27 Mar 2021 06:21:59 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c983dd9a95c6e04b465fb3a7d5743d274d707f052446fa38b9ba54336007a70d`  
		Last Modified: Sat, 27 Mar 2021 06:21:59 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:e7d33c11165e216ea387c2ecb27ed548ecfdba4b73a1133e0a780986e155b802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:aad88142399be179b3dcaa035a18f1a79bb62dc50e349e255e2663cdd45c3684
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542559413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8e2a1935555ac8ff4f86f617137a0d84e38af35675a10525fc3706fe4db893`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:15:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:15:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:15:29 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:15:30 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 27 Mar 2021 06:17:31 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:17:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:17:58 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:17:58 GMT
ENV ODOO_VERSION=12.0
# Sat, 27 Mar 2021 06:17:58 GMT
ARG ODOO_RELEASE=20210318
# Sat, 27 Mar 2021 06:17:58 GMT
ARG ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
# Sat, 27 Mar 2021 06:19:06 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 27 Mar 2021 06:19:09 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 27 Mar 2021 06:19:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 27 Mar 2021 06:19:10 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 27 Mar 2021 06:19:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 27 Mar 2021 06:19:11 GMT
EXPOSE 8069 8071 8072
# Sat, 27 Mar 2021 06:19:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 27 Mar 2021 06:19:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 27 Mar 2021 06:19:11 GMT
USER odoo
# Sat, 27 Mar 2021 06:19:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 06:19:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d85905ea21b22f3cf49d1544d54fa33de25fbd3fb032724098214829848cb7e`  
		Last Modified: Sat, 27 Mar 2021 06:22:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997e5ef07b089b7d6a8a1ab2cc7851f20c4bd8eab43877b4e69f39d90aa2dacd`  
		Last Modified: Sat, 27 Mar 2021 06:22:45 GMT  
		Size: 219.7 MB (219658920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03046533a143ccada4bcf38fe3cf27238bf9807d1705bd7f63fbb7c99d17accc`  
		Last Modified: Sat, 27 Mar 2021 06:22:02 GMT  
		Size: 2.2 MB (2224133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555b0321ec586fdb7780ba6462caba21fe7328c3b6971007ffb99e4c1d83212e`  
		Last Modified: Sat, 27 Mar 2021 06:22:11 GMT  
		Size: 22.1 MB (22053347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbd16047d0f141cdcb76d0aebba6ed5006df30a185e7ff158aa389306772ca7`  
		Last Modified: Sat, 27 Mar 2021 06:22:52 GMT  
		Size: 276.1 MB (276091950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83cc2e108b31ad343da784db4a76c5c6967cbb10cd185a14973212724a0d07c`  
		Last Modified: Sat, 27 Mar 2021 06:21:59 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f0278cbdf63c9651ad421d27bf1ea89f46c6df99981dd54579a884a4b13f4`  
		Last Modified: Sat, 27 Mar 2021 06:22:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30e2d4c7c1a7aa86b34d49812cf19c686cd3657b57cf25bd687b4ea2bde6c2`  
		Last Modified: Sat, 27 Mar 2021 06:21:59 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c983dd9a95c6e04b465fb3a7d5743d274d707f052446fa38b9ba54336007a70d`  
		Last Modified: Sat, 27 Mar 2021 06:21:59 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:84619767562caf73c7f8a3b2fcc57bebc4b361c56c3ca9b8888c355c713c32e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:2bd93fba5be9d191850d0783d9c1357dab9720755925732f0276e0c969af38bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532202693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f23ccaa7d8fdf108da572d9fc9cf5a13822aa2741b8ce87ff114096391208a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:13:16 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:13:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:13:35 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:13:35 GMT
ENV ODOO_VERSION=13.0
# Sat, 27 Mar 2021 06:13:35 GMT
ARG ODOO_RELEASE=20210318
# Sat, 27 Mar 2021 06:13:35 GMT
ARG ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
# Sat, 27 Mar 2021 06:15:15 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 27 Mar 2021 06:15:19 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 27 Mar 2021 06:15:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 27 Mar 2021 06:15:21 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 27 Mar 2021 06:15:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 27 Mar 2021 06:15:22 GMT
EXPOSE 8069 8071 8072
# Sat, 27 Mar 2021 06:15:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 27 Mar 2021 06:15:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 27 Mar 2021 06:15:22 GMT
USER odoo
# Sat, 27 Mar 2021 06:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 06:15:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526d3837c49e3c6200cfda6d26a6a95d4cfad7afa9fa844b8c35089e92dffb36`  
		Last Modified: Sat, 27 Mar 2021 06:21:34 GMT  
		Size: 207.1 MB (207120267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eaf1ef56328b5cbcbe06575a189e8eb7d8aa1e73926fe07cfb752c883eb46e`  
		Last Modified: Sat, 27 Mar 2021 06:21:02 GMT  
		Size: 2.3 MB (2345443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68a125c2a68878ed8b102fb46ce796a30f6d773f1ddb77fa7ca748d00cd94b8`  
		Last Modified: Sat, 27 Mar 2021 06:21:01 GMT  
		Size: 909.8 KB (909791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ebc253e8e463b4790edcb67a2c18d3160b513550df9006ee7edfda57fca29f`  
		Last Modified: Sat, 27 Mar 2021 06:21:42 GMT  
		Size: 294.7 MB (294723766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58c5d149680fa78d9141c3534b8cfcfbb1f4d9afd7191d66e126b693021ce8c`  
		Last Modified: Sat, 27 Mar 2021 06:20:58 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac1f8708cfa15f098aa7dd8b6b5efedf2175bc1d14657a8220fdd1f6d3aea0a`  
		Last Modified: Sat, 27 Mar 2021 06:20:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce89e413f431e764ac953dd0d6b9de461c594532bda95dbd7d5e0c92fc0164b4`  
		Last Modified: Sat, 27 Mar 2021 06:20:58 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8842201f6543af7ae10f176af1b7a96f10e50081275b5af91e29662c1266a70`  
		Last Modified: Sat, 27 Mar 2021 06:20:58 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:84619767562caf73c7f8a3b2fcc57bebc4b361c56c3ca9b8888c355c713c32e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:2bd93fba5be9d191850d0783d9c1357dab9720755925732f0276e0c969af38bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532202693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f23ccaa7d8fdf108da572d9fc9cf5a13822aa2741b8ce87ff114096391208a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:13:16 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:13:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:13:35 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:13:35 GMT
ENV ODOO_VERSION=13.0
# Sat, 27 Mar 2021 06:13:35 GMT
ARG ODOO_RELEASE=20210318
# Sat, 27 Mar 2021 06:13:35 GMT
ARG ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
# Sat, 27 Mar 2021 06:15:15 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 27 Mar 2021 06:15:19 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 27 Mar 2021 06:15:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 27 Mar 2021 06:15:21 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 27 Mar 2021 06:15:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 27 Mar 2021 06:15:22 GMT
EXPOSE 8069 8071 8072
# Sat, 27 Mar 2021 06:15:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 27 Mar 2021 06:15:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 27 Mar 2021 06:15:22 GMT
USER odoo
# Sat, 27 Mar 2021 06:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 06:15:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526d3837c49e3c6200cfda6d26a6a95d4cfad7afa9fa844b8c35089e92dffb36`  
		Last Modified: Sat, 27 Mar 2021 06:21:34 GMT  
		Size: 207.1 MB (207120267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eaf1ef56328b5cbcbe06575a189e8eb7d8aa1e73926fe07cfb752c883eb46e`  
		Last Modified: Sat, 27 Mar 2021 06:21:02 GMT  
		Size: 2.3 MB (2345443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68a125c2a68878ed8b102fb46ce796a30f6d773f1ddb77fa7ca748d00cd94b8`  
		Last Modified: Sat, 27 Mar 2021 06:21:01 GMT  
		Size: 909.8 KB (909791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ebc253e8e463b4790edcb67a2c18d3160b513550df9006ee7edfda57fca29f`  
		Last Modified: Sat, 27 Mar 2021 06:21:42 GMT  
		Size: 294.7 MB (294723766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58c5d149680fa78d9141c3534b8cfcfbb1f4d9afd7191d66e126b693021ce8c`  
		Last Modified: Sat, 27 Mar 2021 06:20:58 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac1f8708cfa15f098aa7dd8b6b5efedf2175bc1d14657a8220fdd1f6d3aea0a`  
		Last Modified: Sat, 27 Mar 2021 06:20:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce89e413f431e764ac953dd0d6b9de461c594532bda95dbd7d5e0c92fc0164b4`  
		Last Modified: Sat, 27 Mar 2021 06:20:58 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8842201f6543af7ae10f176af1b7a96f10e50081275b5af91e29662c1266a70`  
		Last Modified: Sat, 27 Mar 2021 06:20:58 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:de90615a7c5c0568eafc1ab358d347f6884abff7573edfe6ea9f73e9c36ad07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:89d4261c01f47db87c3ec235e91175585971061cacad557d7db70d181b32eaeb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515350608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d29229a34fd090a14def1fc1390e8b03ea88d171a6bc4c25a61d79c3ac88d6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:09:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:10:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:10:15 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:10:15 GMT
ENV ODOO_VERSION=14.0
# Sat, 27 Mar 2021 06:10:16 GMT
ARG ODOO_RELEASE=20210318
# Sat, 27 Mar 2021 06:10:16 GMT
ARG ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
# Sat, 27 Mar 2021 06:11:47 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 27 Mar 2021 06:11:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 27 Mar 2021 06:11:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 27 Mar 2021 06:11:54 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 27 Mar 2021 06:11:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 27 Mar 2021 06:11:54 GMT
EXPOSE 8069 8071 8072
# Sat, 27 Mar 2021 06:11:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 27 Mar 2021 06:11:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 27 Mar 2021 06:11:55 GMT
USER odoo
# Sat, 27 Mar 2021 06:11:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 06:11:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95e614e07c856f6c1da438d4c95c0a6e5eac30d89fcc3a5734f5135633ed4a`  
		Last Modified: Sat, 27 Mar 2021 06:20:33 GMT  
		Size: 213.2 MB (213156617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08230c79e58cbef992d03708a57cb446a37e38c4aae753a3b55270d96eccf46d`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 2.3 MB (2348523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfde40794ec1a3832504589fefca9859cb38526d3244c425e3dbcefa0cbc7356`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 910.1 KB (910061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136108e662a3ea0b080347a7bd4f6b5a100dafdf4c4e7f72056199b7744538e8`  
		Last Modified: Sat, 27 Mar 2021 06:20:43 GMT  
		Size: 271.8 MB (271831975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeae6f35ea3708dc1929dfe0345044845a0a16efbe58b4ec2329dab5016a2018`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352a82d83cf06ce462d3364a3daf448362575feee490995e34a9d18aed584139`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7637f801e1bf07fb58cef47fc64591cd139de3aec91ee8e4a57127ddd29da9a`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c54b3b7ae9d5c458caf3be743a564ed05553332c970f1c2d3c24af345b287a`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:de90615a7c5c0568eafc1ab358d347f6884abff7573edfe6ea9f73e9c36ad07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:89d4261c01f47db87c3ec235e91175585971061cacad557d7db70d181b32eaeb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515350608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d29229a34fd090a14def1fc1390e8b03ea88d171a6bc4c25a61d79c3ac88d6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:09:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:10:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:10:15 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:10:15 GMT
ENV ODOO_VERSION=14.0
# Sat, 27 Mar 2021 06:10:16 GMT
ARG ODOO_RELEASE=20210318
# Sat, 27 Mar 2021 06:10:16 GMT
ARG ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
# Sat, 27 Mar 2021 06:11:47 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 27 Mar 2021 06:11:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 27 Mar 2021 06:11:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 27 Mar 2021 06:11:54 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 27 Mar 2021 06:11:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 27 Mar 2021 06:11:54 GMT
EXPOSE 8069 8071 8072
# Sat, 27 Mar 2021 06:11:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 27 Mar 2021 06:11:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 27 Mar 2021 06:11:55 GMT
USER odoo
# Sat, 27 Mar 2021 06:11:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 06:11:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95e614e07c856f6c1da438d4c95c0a6e5eac30d89fcc3a5734f5135633ed4a`  
		Last Modified: Sat, 27 Mar 2021 06:20:33 GMT  
		Size: 213.2 MB (213156617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08230c79e58cbef992d03708a57cb446a37e38c4aae753a3b55270d96eccf46d`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 2.3 MB (2348523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfde40794ec1a3832504589fefca9859cb38526d3244c425e3dbcefa0cbc7356`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 910.1 KB (910061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136108e662a3ea0b080347a7bd4f6b5a100dafdf4c4e7f72056199b7744538e8`  
		Last Modified: Sat, 27 Mar 2021 06:20:43 GMT  
		Size: 271.8 MB (271831975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeae6f35ea3708dc1929dfe0345044845a0a16efbe58b4ec2329dab5016a2018`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352a82d83cf06ce462d3364a3daf448362575feee490995e34a9d18aed584139`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7637f801e1bf07fb58cef47fc64591cd139de3aec91ee8e4a57127ddd29da9a`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c54b3b7ae9d5c458caf3be743a564ed05553332c970f1c2d3c24af345b287a`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:de90615a7c5c0568eafc1ab358d347f6884abff7573edfe6ea9f73e9c36ad07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:89d4261c01f47db87c3ec235e91175585971061cacad557d7db70d181b32eaeb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515350608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d29229a34fd090a14def1fc1390e8b03ea88d171a6bc4c25a61d79c3ac88d6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:09:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:10:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:10:15 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:10:15 GMT
ENV ODOO_VERSION=14.0
# Sat, 27 Mar 2021 06:10:16 GMT
ARG ODOO_RELEASE=20210318
# Sat, 27 Mar 2021 06:10:16 GMT
ARG ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
# Sat, 27 Mar 2021 06:11:47 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 27 Mar 2021 06:11:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 27 Mar 2021 06:11:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 27 Mar 2021 06:11:54 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 27 Mar 2021 06:11:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 27 Mar 2021 06:11:54 GMT
EXPOSE 8069 8071 8072
# Sat, 27 Mar 2021 06:11:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 27 Mar 2021 06:11:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 27 Mar 2021 06:11:55 GMT
USER odoo
# Sat, 27 Mar 2021 06:11:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 06:11:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95e614e07c856f6c1da438d4c95c0a6e5eac30d89fcc3a5734f5135633ed4a`  
		Last Modified: Sat, 27 Mar 2021 06:20:33 GMT  
		Size: 213.2 MB (213156617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08230c79e58cbef992d03708a57cb446a37e38c4aae753a3b55270d96eccf46d`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 2.3 MB (2348523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfde40794ec1a3832504589fefca9859cb38526d3244c425e3dbcefa0cbc7356`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 910.1 KB (910061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136108e662a3ea0b080347a7bd4f6b5a100dafdf4c4e7f72056199b7744538e8`  
		Last Modified: Sat, 27 Mar 2021 06:20:43 GMT  
		Size: 271.8 MB (271831975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeae6f35ea3708dc1929dfe0345044845a0a16efbe58b4ec2329dab5016a2018`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352a82d83cf06ce462d3364a3daf448362575feee490995e34a9d18aed584139`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7637f801e1bf07fb58cef47fc64591cd139de3aec91ee8e4a57127ddd29da9a`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c54b3b7ae9d5c458caf3be743a564ed05553332c970f1c2d3c24af345b287a`  
		Last Modified: Sat, 27 Mar 2021 06:19:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
