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
$ docker pull odoo@sha256:4e381967d816dd1a5e0a7ff36f4af885f544bc72fd031c9409876525816eff9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:57e0d27080e94a4838b062e2a48b832f8e52796c819c530f8be12f31767dbdb7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.3 MB (538310899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a91f2d1016f79ee77ec65410700d2535dd7aaa7ad58db25829dc8979dcb769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:50:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:50:48 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 12 May 2021 08:52:09 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:52:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:52:45 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:52:46 GMT
ENV ODOO_VERSION=12.0
# Tue, 25 May 2021 18:48:44 GMT
ARG ODOO_RELEASE=20210525
# Tue, 25 May 2021 18:48:44 GMT
ARG ODOO_SHA=c08514dbe2c590a2d9f6029a3fe8abb58306e3a6
# Tue, 25 May 2021 18:49:47 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=c08514dbe2c590a2d9f6029a3fe8abb58306e3a6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 25 May 2021 18:49:50 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 25 May 2021 18:49:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 25 May 2021 18:49:51 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=c08514dbe2c590a2d9f6029a3fe8abb58306e3a6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 25 May 2021 18:49:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 25 May 2021 18:49:52 GMT
EXPOSE 8069 8071 8072
# Tue, 25 May 2021 18:49:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 25 May 2021 18:49:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 25 May 2021 18:49:52 GMT
USER odoo
# Tue, 25 May 2021 18:49:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 May 2021 18:49:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af54249d19fe626a77f15839d273f8d043ce913784302e4e5ee6a810b158f43`  
		Last Modified: Wed, 12 May 2021 08:56:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019e7996c57952fa770bb898324d340b77024067ab213469f9fefe533da19ea4`  
		Last Modified: Wed, 12 May 2021 08:57:13 GMT  
		Size: 219.6 MB (219644042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a2f907c0eef99db7b697ab129fdefdf63e755e22e9fee296c13a5179009c44`  
		Last Modified: Wed, 12 May 2021 08:56:45 GMT  
		Size: 2.2 MB (2224133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764a9260e7d9a4e20c20fb21502f10d7ff5406fe00b088e79e0a80a0c421d5f5`  
		Last Modified: Wed, 12 May 2021 08:56:50 GMT  
		Size: 22.0 MB (22043646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a899a635fa763056624f572aeb7855a7795602d143162db46dff61dfe69cc566`  
		Last Modified: Tue, 25 May 2021 18:52:06 GMT  
		Size: 271.9 MB (271868148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16e0d267845513e8c963f50b60587762153b1bd5c5d897c65c14f83d8cedcc9`  
		Last Modified: Tue, 25 May 2021 18:51:37 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22912b956303cdf14828486fb91642806cf4a609d5fbaff57a49c05009af16c`  
		Last Modified: Tue, 25 May 2021 18:51:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ea43223c6ba8a331e2a6a901ab264c9454949a7c09c0d189f55670d82a3bd7`  
		Last Modified: Tue, 25 May 2021 18:51:37 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38688b261786b31c673eb1f813cc9be3b8afc28e3324e13bf21604a9e18fe2c6`  
		Last Modified: Tue, 25 May 2021 18:51:37 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:4e381967d816dd1a5e0a7ff36f4af885f544bc72fd031c9409876525816eff9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:57e0d27080e94a4838b062e2a48b832f8e52796c819c530f8be12f31767dbdb7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.3 MB (538310899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a91f2d1016f79ee77ec65410700d2535dd7aaa7ad58db25829dc8979dcb769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:50:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:50:48 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 12 May 2021 08:52:09 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:52:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:52:45 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:52:46 GMT
ENV ODOO_VERSION=12.0
# Tue, 25 May 2021 18:48:44 GMT
ARG ODOO_RELEASE=20210525
# Tue, 25 May 2021 18:48:44 GMT
ARG ODOO_SHA=c08514dbe2c590a2d9f6029a3fe8abb58306e3a6
# Tue, 25 May 2021 18:49:47 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=c08514dbe2c590a2d9f6029a3fe8abb58306e3a6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 25 May 2021 18:49:50 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 25 May 2021 18:49:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 25 May 2021 18:49:51 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=c08514dbe2c590a2d9f6029a3fe8abb58306e3a6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 25 May 2021 18:49:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 25 May 2021 18:49:52 GMT
EXPOSE 8069 8071 8072
# Tue, 25 May 2021 18:49:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 25 May 2021 18:49:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 25 May 2021 18:49:52 GMT
USER odoo
# Tue, 25 May 2021 18:49:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 May 2021 18:49:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af54249d19fe626a77f15839d273f8d043ce913784302e4e5ee6a810b158f43`  
		Last Modified: Wed, 12 May 2021 08:56:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019e7996c57952fa770bb898324d340b77024067ab213469f9fefe533da19ea4`  
		Last Modified: Wed, 12 May 2021 08:57:13 GMT  
		Size: 219.6 MB (219644042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a2f907c0eef99db7b697ab129fdefdf63e755e22e9fee296c13a5179009c44`  
		Last Modified: Wed, 12 May 2021 08:56:45 GMT  
		Size: 2.2 MB (2224133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764a9260e7d9a4e20c20fb21502f10d7ff5406fe00b088e79e0a80a0c421d5f5`  
		Last Modified: Wed, 12 May 2021 08:56:50 GMT  
		Size: 22.0 MB (22043646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a899a635fa763056624f572aeb7855a7795602d143162db46dff61dfe69cc566`  
		Last Modified: Tue, 25 May 2021 18:52:06 GMT  
		Size: 271.9 MB (271868148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16e0d267845513e8c963f50b60587762153b1bd5c5d897c65c14f83d8cedcc9`  
		Last Modified: Tue, 25 May 2021 18:51:37 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22912b956303cdf14828486fb91642806cf4a609d5fbaff57a49c05009af16c`  
		Last Modified: Tue, 25 May 2021 18:51:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ea43223c6ba8a331e2a6a901ab264c9454949a7c09c0d189f55670d82a3bd7`  
		Last Modified: Tue, 25 May 2021 18:51:37 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38688b261786b31c673eb1f813cc9be3b8afc28e3324e13bf21604a9e18fe2c6`  
		Last Modified: Tue, 25 May 2021 18:51:37 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:57adf38f1eaff6c09a1d897b2ce004395a505fc46470ee77d7a1f459fbcd4e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:1ebbc5c5853386c0a1f54f310966871878831733d3f5f232e0159f3d2dc7d6da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.1 MB (528131421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c9e86341a42f5cdd9627d5c3d3c6ee3bd49a4be89d5b14390efb041f733de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:49:03 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:49:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:49:14 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:49:14 GMT
ENV ODOO_VERSION=13.0
# Tue, 25 May 2021 18:47:19 GMT
ARG ODOO_RELEASE=20210525
# Tue, 25 May 2021 18:47:19 GMT
ARG ODOO_SHA=206c082550b13c745f446e412562d997da6fefc6
# Tue, 25 May 2021 18:48:28 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=206c082550b13c745f446e412562d997da6fefc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 25 May 2021 18:48:32 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 25 May 2021 18:48:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 25 May 2021 18:48:33 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=206c082550b13c745f446e412562d997da6fefc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 25 May 2021 18:48:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 25 May 2021 18:48:34 GMT
EXPOSE 8069 8071 8072
# Tue, 25 May 2021 18:48:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 25 May 2021 18:48:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 25 May 2021 18:48:34 GMT
USER odoo
# Tue, 25 May 2021 18:48:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 May 2021 18:48:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd2340d2eb35cffa9ca9e4bde49346d44e9b5256f115d1d5ef505381aa063b2`  
		Last Modified: Wed, 12 May 2021 08:56:16 GMT  
		Size: 207.1 MB (207123504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db2bf3253f515783426050c6c8a278f5d8a9d574287fae7bc3630e3586a0dc7`  
		Last Modified: Wed, 12 May 2021 08:55:20 GMT  
		Size: 2.3 MB (2345380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37981d08650c3b2e5a5e757ba40494eb86a34a4162414076c592efa41f10e3ea`  
		Last Modified: Wed, 12 May 2021 08:55:20 GMT  
		Size: 906.3 KB (906348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35f14edd8c7d6cd24aa56656700972ee745ef832bdc5046113d994ef6a893cf`  
		Last Modified: Tue, 25 May 2021 18:51:25 GMT  
		Size: 290.6 MB (290607840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a97e9841b7c80a72d49ae7a9f9a4ca6df7bd323617d39cbc4d97d95c536895`  
		Last Modified: Tue, 25 May 2021 18:50:53 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b088be3c2a90fa46be91b706ee07d2caca79ef7fb57bcc6cb683289cd6b89e`  
		Last Modified: Tue, 25 May 2021 18:50:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58f281ba45525fc3ac54bb313ed3e45ed333c60fd8e115d92aa8c2c70f07a9`  
		Last Modified: Tue, 25 May 2021 18:50:54 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33af878d64c93976b3728c03a7c0051615511a43ed28b0291ddf32682d369d`  
		Last Modified: Tue, 25 May 2021 18:50:53 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:57adf38f1eaff6c09a1d897b2ce004395a505fc46470ee77d7a1f459fbcd4e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:1ebbc5c5853386c0a1f54f310966871878831733d3f5f232e0159f3d2dc7d6da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.1 MB (528131421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c9e86341a42f5cdd9627d5c3d3c6ee3bd49a4be89d5b14390efb041f733de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:49:03 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:49:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:49:14 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:49:14 GMT
ENV ODOO_VERSION=13.0
# Tue, 25 May 2021 18:47:19 GMT
ARG ODOO_RELEASE=20210525
# Tue, 25 May 2021 18:47:19 GMT
ARG ODOO_SHA=206c082550b13c745f446e412562d997da6fefc6
# Tue, 25 May 2021 18:48:28 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=206c082550b13c745f446e412562d997da6fefc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 25 May 2021 18:48:32 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 25 May 2021 18:48:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 25 May 2021 18:48:33 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=206c082550b13c745f446e412562d997da6fefc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 25 May 2021 18:48:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 25 May 2021 18:48:34 GMT
EXPOSE 8069 8071 8072
# Tue, 25 May 2021 18:48:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 25 May 2021 18:48:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 25 May 2021 18:48:34 GMT
USER odoo
# Tue, 25 May 2021 18:48:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 May 2021 18:48:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd2340d2eb35cffa9ca9e4bde49346d44e9b5256f115d1d5ef505381aa063b2`  
		Last Modified: Wed, 12 May 2021 08:56:16 GMT  
		Size: 207.1 MB (207123504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db2bf3253f515783426050c6c8a278f5d8a9d574287fae7bc3630e3586a0dc7`  
		Last Modified: Wed, 12 May 2021 08:55:20 GMT  
		Size: 2.3 MB (2345380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37981d08650c3b2e5a5e757ba40494eb86a34a4162414076c592efa41f10e3ea`  
		Last Modified: Wed, 12 May 2021 08:55:20 GMT  
		Size: 906.3 KB (906348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35f14edd8c7d6cd24aa56656700972ee745ef832bdc5046113d994ef6a893cf`  
		Last Modified: Tue, 25 May 2021 18:51:25 GMT  
		Size: 290.6 MB (290607840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a97e9841b7c80a72d49ae7a9f9a4ca6df7bd323617d39cbc4d97d95c536895`  
		Last Modified: Tue, 25 May 2021 18:50:53 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b088be3c2a90fa46be91b706ee07d2caca79ef7fb57bcc6cb683289cd6b89e`  
		Last Modified: Tue, 25 May 2021 18:50:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58f281ba45525fc3ac54bb313ed3e45ed333c60fd8e115d92aa8c2c70f07a9`  
		Last Modified: Tue, 25 May 2021 18:50:54 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33af878d64c93976b3728c03a7c0051615511a43ed28b0291ddf32682d369d`  
		Last Modified: Tue, 25 May 2021 18:50:53 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:8602b33ad2aaecde347ae50fae63fd8f2193d3ae69b06aa371a591d7774284ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:542e36dfc7ad121ea51813e8f6526b5417983cbf490c6702512d5ffcfa7efb8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.8 MB (513825136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca003a231ac54b3baef2e0149fdec14d0e8014fa0ce5583e1e5c5cf5bf3d5ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:46:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:46:32 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:46:32 GMT
ENV ODOO_VERSION=14.0
# Tue, 25 May 2021 18:45:53 GMT
ARG ODOO_RELEASE=20210525
# Tue, 25 May 2021 18:45:53 GMT
ARG ODOO_SHA=1d095badf1a6639b0d029a69ac4a43d360280d95
# Tue, 25 May 2021 18:47:03 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=1d095badf1a6639b0d029a69ac4a43d360280d95
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 25 May 2021 18:47:07 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 25 May 2021 18:47:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 25 May 2021 18:47:08 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=1d095badf1a6639b0d029a69ac4a43d360280d95
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 25 May 2021 18:47:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 25 May 2021 18:47:08 GMT
EXPOSE 8069 8071 8072
# Tue, 25 May 2021 18:47:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 25 May 2021 18:47:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 25 May 2021 18:47:09 GMT
USER odoo
# Tue, 25 May 2021 18:47:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 May 2021 18:47:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4b0e38652c25af879825f24dbea2383353d341f344d6380e333c3acfe1fdaa`  
		Last Modified: Wed, 12 May 2021 08:54:57 GMT  
		Size: 213.2 MB (213170176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9893a9d4028d8617a36b2cec12ad0bd2f635a565ad68099c04d5e7f25aebe81`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 2.3 MB (2348569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646c61bff1d0763d58e8409ab91365ab8469566e7f5cf9a1f9be81b21d4eeeb`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 906.3 KB (906251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1367e90a020de60f57cdfc907de2aed63e3f8031684991ac15651e372dd9f5`  
		Last Modified: Tue, 25 May 2021 18:50:40 GMT  
		Size: 270.3 MB (270251793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f2a124af8a36703f40381b8158689a25cd595970b56a665a57c79768c1da1`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca879da81b2af88ffe32448cf7aa986c8d73901792a1daa19f19496019817f`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a4f26098ff4e21d2de216d48ae6af64eeb448a94b4b8b662a476189cebdec3`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b689ed50b09a2d49852d4b2ff4954e5544f9f47795e6dbc84ca07e8cd847c10`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:8602b33ad2aaecde347ae50fae63fd8f2193d3ae69b06aa371a591d7774284ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:542e36dfc7ad121ea51813e8f6526b5417983cbf490c6702512d5ffcfa7efb8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.8 MB (513825136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca003a231ac54b3baef2e0149fdec14d0e8014fa0ce5583e1e5c5cf5bf3d5ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:46:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:46:32 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:46:32 GMT
ENV ODOO_VERSION=14.0
# Tue, 25 May 2021 18:45:53 GMT
ARG ODOO_RELEASE=20210525
# Tue, 25 May 2021 18:45:53 GMT
ARG ODOO_SHA=1d095badf1a6639b0d029a69ac4a43d360280d95
# Tue, 25 May 2021 18:47:03 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=1d095badf1a6639b0d029a69ac4a43d360280d95
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 25 May 2021 18:47:07 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 25 May 2021 18:47:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 25 May 2021 18:47:08 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=1d095badf1a6639b0d029a69ac4a43d360280d95
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 25 May 2021 18:47:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 25 May 2021 18:47:08 GMT
EXPOSE 8069 8071 8072
# Tue, 25 May 2021 18:47:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 25 May 2021 18:47:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 25 May 2021 18:47:09 GMT
USER odoo
# Tue, 25 May 2021 18:47:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 May 2021 18:47:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4b0e38652c25af879825f24dbea2383353d341f344d6380e333c3acfe1fdaa`  
		Last Modified: Wed, 12 May 2021 08:54:57 GMT  
		Size: 213.2 MB (213170176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9893a9d4028d8617a36b2cec12ad0bd2f635a565ad68099c04d5e7f25aebe81`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 2.3 MB (2348569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646c61bff1d0763d58e8409ab91365ab8469566e7f5cf9a1f9be81b21d4eeeb`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 906.3 KB (906251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1367e90a020de60f57cdfc907de2aed63e3f8031684991ac15651e372dd9f5`  
		Last Modified: Tue, 25 May 2021 18:50:40 GMT  
		Size: 270.3 MB (270251793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f2a124af8a36703f40381b8158689a25cd595970b56a665a57c79768c1da1`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca879da81b2af88ffe32448cf7aa986c8d73901792a1daa19f19496019817f`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a4f26098ff4e21d2de216d48ae6af64eeb448a94b4b8b662a476189cebdec3`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b689ed50b09a2d49852d4b2ff4954e5544f9f47795e6dbc84ca07e8cd847c10`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:8602b33ad2aaecde347ae50fae63fd8f2193d3ae69b06aa371a591d7774284ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:542e36dfc7ad121ea51813e8f6526b5417983cbf490c6702512d5ffcfa7efb8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.8 MB (513825136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca003a231ac54b3baef2e0149fdec14d0e8014fa0ce5583e1e5c5cf5bf3d5ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:46:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:46:32 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:46:32 GMT
ENV ODOO_VERSION=14.0
# Tue, 25 May 2021 18:45:53 GMT
ARG ODOO_RELEASE=20210525
# Tue, 25 May 2021 18:45:53 GMT
ARG ODOO_SHA=1d095badf1a6639b0d029a69ac4a43d360280d95
# Tue, 25 May 2021 18:47:03 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=1d095badf1a6639b0d029a69ac4a43d360280d95
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 25 May 2021 18:47:07 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 25 May 2021 18:47:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 25 May 2021 18:47:08 GMT
# ARGS: ODOO_RELEASE=20210525 ODOO_SHA=1d095badf1a6639b0d029a69ac4a43d360280d95
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 25 May 2021 18:47:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 25 May 2021 18:47:08 GMT
EXPOSE 8069 8071 8072
# Tue, 25 May 2021 18:47:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 25 May 2021 18:47:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 25 May 2021 18:47:09 GMT
USER odoo
# Tue, 25 May 2021 18:47:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 May 2021 18:47:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4b0e38652c25af879825f24dbea2383353d341f344d6380e333c3acfe1fdaa`  
		Last Modified: Wed, 12 May 2021 08:54:57 GMT  
		Size: 213.2 MB (213170176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9893a9d4028d8617a36b2cec12ad0bd2f635a565ad68099c04d5e7f25aebe81`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 2.3 MB (2348569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646c61bff1d0763d58e8409ab91365ab8469566e7f5cf9a1f9be81b21d4eeeb`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 906.3 KB (906251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1367e90a020de60f57cdfc907de2aed63e3f8031684991ac15651e372dd9f5`  
		Last Modified: Tue, 25 May 2021 18:50:40 GMT  
		Size: 270.3 MB (270251793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f2a124af8a36703f40381b8158689a25cd595970b56a665a57c79768c1da1`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca879da81b2af88ffe32448cf7aa986c8d73901792a1daa19f19496019817f`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a4f26098ff4e21d2de216d48ae6af64eeb448a94b4b8b662a476189cebdec3`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b689ed50b09a2d49852d4b2ff4954e5544f9f47795e6dbc84ca07e8cd847c10`  
		Last Modified: Tue, 25 May 2021 18:50:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
