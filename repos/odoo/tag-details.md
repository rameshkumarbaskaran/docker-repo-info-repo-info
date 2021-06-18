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
$ docker pull odoo@sha256:bd7794fd308ed200a087b7da1112d1688a03d11b99ded02542a6dab1cc8c7ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:5d327df4078ddfbc9bbfe0f3a9d5d24d9e38d77f895658cc050ebdc5d54a584d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538364058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de40f1e89d3d78a1f8487462c281dc16e419a7f91d81676c358f678a8b7bb0b4`
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
# Fri, 18 Jun 2021 18:25:54 GMT
ARG ODOO_RELEASE=20210618
# Fri, 18 Jun 2021 18:25:54 GMT
ARG ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
# Fri, 18 Jun 2021 18:27:01 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Jun 2021 18:27:04 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Jun 2021 18:27:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Jun 2021 18:27:05 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Jun 2021 18:27:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Jun 2021 18:27:05 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Jun 2021 18:27:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Jun 2021 18:27:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Jun 2021 18:27:06 GMT
USER odoo
# Fri, 18 Jun 2021 18:27:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 18:27:06 GMT
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
	-	`sha256:96ebe6720fb1a95b82e44d034e8211966432ac5f7cc180287af487ee23ecd25e`  
		Last Modified: Fri, 18 Jun 2021 18:29:35 GMT  
		Size: 271.9 MB (271921311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbab1063fff49b710f4fb0237306a467d2e80a01182191310144274d56c4099`  
		Last Modified: Fri, 18 Jun 2021 18:29:05 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30492097cae678c1fc56a2133cf6cd01d7604a5a59b62c153cb3b6d698895f60`  
		Last Modified: Fri, 18 Jun 2021 18:29:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472cdb0f9a76cb0651cae83a83592de264b097b4eb3bfbb8e4343e8c13384dc`  
		Last Modified: Fri, 18 Jun 2021 18:29:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860e17fc6df1477a2d87f876b203d5678636ac1b21ef3a2a396dbdd7ddad97d6`  
		Last Modified: Fri, 18 Jun 2021 18:29:05 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:bd7794fd308ed200a087b7da1112d1688a03d11b99ded02542a6dab1cc8c7ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:5d327df4078ddfbc9bbfe0f3a9d5d24d9e38d77f895658cc050ebdc5d54a584d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538364058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de40f1e89d3d78a1f8487462c281dc16e419a7f91d81676c358f678a8b7bb0b4`
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
# Fri, 18 Jun 2021 18:25:54 GMT
ARG ODOO_RELEASE=20210618
# Fri, 18 Jun 2021 18:25:54 GMT
ARG ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
# Fri, 18 Jun 2021 18:27:01 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Jun 2021 18:27:04 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Jun 2021 18:27:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Jun 2021 18:27:05 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=1d696a2d048cfdf49ba5daa4e1655901ea507bc1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Jun 2021 18:27:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Jun 2021 18:27:05 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Jun 2021 18:27:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Jun 2021 18:27:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Jun 2021 18:27:06 GMT
USER odoo
# Fri, 18 Jun 2021 18:27:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 18:27:06 GMT
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
	-	`sha256:96ebe6720fb1a95b82e44d034e8211966432ac5f7cc180287af487ee23ecd25e`  
		Last Modified: Fri, 18 Jun 2021 18:29:35 GMT  
		Size: 271.9 MB (271921311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbab1063fff49b710f4fb0237306a467d2e80a01182191310144274d56c4099`  
		Last Modified: Fri, 18 Jun 2021 18:29:05 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30492097cae678c1fc56a2133cf6cd01d7604a5a59b62c153cb3b6d698895f60`  
		Last Modified: Fri, 18 Jun 2021 18:29:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472cdb0f9a76cb0651cae83a83592de264b097b4eb3bfbb8e4343e8c13384dc`  
		Last Modified: Fri, 18 Jun 2021 18:29:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860e17fc6df1477a2d87f876b203d5678636ac1b21ef3a2a396dbdd7ddad97d6`  
		Last Modified: Fri, 18 Jun 2021 18:29:05 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:6d7a2557d71f113461d8b81da249002398a241ee24ac96d63f151ba0d95a73c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:717d824cd6ef47b680747c53d3125b166329657827e6926f5609e3fb591fe62d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.2 MB (528212461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db04eeb87b9b164b0da581dd332f0be31bc3587018c5fee631ea87ec4cf33620`
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
# Fri, 18 Jun 2021 18:24:28 GMT
ARG ODOO_RELEASE=20210618
# Fri, 18 Jun 2021 18:24:29 GMT
ARG ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
# Fri, 18 Jun 2021 18:25:42 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Jun 2021 18:25:45 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Jun 2021 18:25:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Jun 2021 18:25:47 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Jun 2021 18:25:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Jun 2021 18:25:47 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Jun 2021 18:25:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Jun 2021 18:25:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Jun 2021 18:25:48 GMT
USER odoo
# Fri, 18 Jun 2021 18:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 18:25:48 GMT
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
	-	`sha256:132f5b41a64b54a1897beba5045c296996e16ddc483902e4c76711df35e850fe`  
		Last Modified: Fri, 18 Jun 2021 18:28:51 GMT  
		Size: 290.7 MB (290688880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eff0a917c0ee4ea0dcf8793489bd458ed00635dc8933cc28d3393894faee651`  
		Last Modified: Fri, 18 Jun 2021 18:28:18 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78330cbf641b05aed600fd2412eaf46a3580ebb8a0199c079f554cf6a7c4027`  
		Last Modified: Fri, 18 Jun 2021 18:28:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b737c4ebad7b8d5f82f1186d72548cf9b6ce70ce2bf84067b5911d7edfeb13f`  
		Last Modified: Fri, 18 Jun 2021 18:28:18 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25b4ec70b65da7517a434bef22ed674eee5c4f96933ab4d534fa3e69b562018`  
		Last Modified: Fri, 18 Jun 2021 18:28:18 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:6d7a2557d71f113461d8b81da249002398a241ee24ac96d63f151ba0d95a73c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:717d824cd6ef47b680747c53d3125b166329657827e6926f5609e3fb591fe62d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.2 MB (528212461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db04eeb87b9b164b0da581dd332f0be31bc3587018c5fee631ea87ec4cf33620`
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
# Fri, 18 Jun 2021 18:24:28 GMT
ARG ODOO_RELEASE=20210618
# Fri, 18 Jun 2021 18:24:29 GMT
ARG ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
# Fri, 18 Jun 2021 18:25:42 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Jun 2021 18:25:45 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Jun 2021 18:25:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Jun 2021 18:25:47 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=772a85f570e240254221fe3ecd977324db81e2bf
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Jun 2021 18:25:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Jun 2021 18:25:47 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Jun 2021 18:25:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Jun 2021 18:25:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Jun 2021 18:25:48 GMT
USER odoo
# Fri, 18 Jun 2021 18:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 18:25:48 GMT
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
	-	`sha256:132f5b41a64b54a1897beba5045c296996e16ddc483902e4c76711df35e850fe`  
		Last Modified: Fri, 18 Jun 2021 18:28:51 GMT  
		Size: 290.7 MB (290688880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eff0a917c0ee4ea0dcf8793489bd458ed00635dc8933cc28d3393894faee651`  
		Last Modified: Fri, 18 Jun 2021 18:28:18 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78330cbf641b05aed600fd2412eaf46a3580ebb8a0199c079f554cf6a7c4027`  
		Last Modified: Fri, 18 Jun 2021 18:28:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b737c4ebad7b8d5f82f1186d72548cf9b6ce70ce2bf84067b5911d7edfeb13f`  
		Last Modified: Fri, 18 Jun 2021 18:28:18 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25b4ec70b65da7517a434bef22ed674eee5c4f96933ab4d534fa3e69b562018`  
		Last Modified: Fri, 18 Jun 2021 18:28:18 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:c9ffb6c039a9ff60507b5270ce227371e83d1f28c603d285e10d511514a8adc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:6c26b6f3d051a02a576bf282b5da3b3f440f7f116483c435fa06a564e1e47c86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514260123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0108a745b286fa0a9cdeb7474b854de26ce3efe92fb930568052d5077d363b0a`
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
# Fri, 18 Jun 2021 18:23:03 GMT
ARG ODOO_RELEASE=20210618
# Fri, 18 Jun 2021 18:23:03 GMT
ARG ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
# Fri, 18 Jun 2021 18:24:17 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Jun 2021 18:24:20 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Jun 2021 18:24:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Jun 2021 18:24:22 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Jun 2021 18:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Jun 2021 18:24:22 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Jun 2021 18:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Jun 2021 18:24:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Jun 2021 18:24:23 GMT
USER odoo
# Fri, 18 Jun 2021 18:24:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 18:24:23 GMT
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
	-	`sha256:f7576f4e6590b7502369be9f87ae92591702b72f478d67594d8fb1f6a0e9908e`  
		Last Modified: Fri, 18 Jun 2021 18:28:04 GMT  
		Size: 270.7 MB (270686779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba077925991d8ece3b921f677104f376a5ef22710ab438c17a4e95ca9cc1b77`  
		Last Modified: Fri, 18 Jun 2021 18:27:31 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b1b795d60c2fd9a66bff088b0f52f288b646bcffb64f8c3ea4f276a38c4f8`  
		Last Modified: Fri, 18 Jun 2021 18:27:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb669f0511807cdf28c62961741c40f456eb2b7e2acf48ba47b1b75d3f810a80`  
		Last Modified: Fri, 18 Jun 2021 18:27:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ed42830001dfc2908f44fbc8a8f714dc9a6ed0c083c10798bbe423163c1a68`  
		Last Modified: Fri, 18 Jun 2021 18:27:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:c9ffb6c039a9ff60507b5270ce227371e83d1f28c603d285e10d511514a8adc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:6c26b6f3d051a02a576bf282b5da3b3f440f7f116483c435fa06a564e1e47c86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514260123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0108a745b286fa0a9cdeb7474b854de26ce3efe92fb930568052d5077d363b0a`
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
# Fri, 18 Jun 2021 18:23:03 GMT
ARG ODOO_RELEASE=20210618
# Fri, 18 Jun 2021 18:23:03 GMT
ARG ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
# Fri, 18 Jun 2021 18:24:17 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Jun 2021 18:24:20 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Jun 2021 18:24:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Jun 2021 18:24:22 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Jun 2021 18:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Jun 2021 18:24:22 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Jun 2021 18:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Jun 2021 18:24:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Jun 2021 18:24:23 GMT
USER odoo
# Fri, 18 Jun 2021 18:24:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 18:24:23 GMT
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
	-	`sha256:f7576f4e6590b7502369be9f87ae92591702b72f478d67594d8fb1f6a0e9908e`  
		Last Modified: Fri, 18 Jun 2021 18:28:04 GMT  
		Size: 270.7 MB (270686779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba077925991d8ece3b921f677104f376a5ef22710ab438c17a4e95ca9cc1b77`  
		Last Modified: Fri, 18 Jun 2021 18:27:31 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b1b795d60c2fd9a66bff088b0f52f288b646bcffb64f8c3ea4f276a38c4f8`  
		Last Modified: Fri, 18 Jun 2021 18:27:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb669f0511807cdf28c62961741c40f456eb2b7e2acf48ba47b1b75d3f810a80`  
		Last Modified: Fri, 18 Jun 2021 18:27:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ed42830001dfc2908f44fbc8a8f714dc9a6ed0c083c10798bbe423163c1a68`  
		Last Modified: Fri, 18 Jun 2021 18:27:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:c9ffb6c039a9ff60507b5270ce227371e83d1f28c603d285e10d511514a8adc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:6c26b6f3d051a02a576bf282b5da3b3f440f7f116483c435fa06a564e1e47c86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514260123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0108a745b286fa0a9cdeb7474b854de26ce3efe92fb930568052d5077d363b0a`
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
# Fri, 18 Jun 2021 18:23:03 GMT
ARG ODOO_RELEASE=20210618
# Fri, 18 Jun 2021 18:23:03 GMT
ARG ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
# Fri, 18 Jun 2021 18:24:17 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Jun 2021 18:24:20 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Jun 2021 18:24:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Jun 2021 18:24:22 GMT
# ARGS: ODOO_RELEASE=20210618 ODOO_SHA=261431b2bcb6d64751560cbd4dd98a9d98863e0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Jun 2021 18:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Jun 2021 18:24:22 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Jun 2021 18:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Jun 2021 18:24:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Jun 2021 18:24:23 GMT
USER odoo
# Fri, 18 Jun 2021 18:24:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 18:24:23 GMT
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
	-	`sha256:f7576f4e6590b7502369be9f87ae92591702b72f478d67594d8fb1f6a0e9908e`  
		Last Modified: Fri, 18 Jun 2021 18:28:04 GMT  
		Size: 270.7 MB (270686779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba077925991d8ece3b921f677104f376a5ef22710ab438c17a4e95ca9cc1b77`  
		Last Modified: Fri, 18 Jun 2021 18:27:31 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b1b795d60c2fd9a66bff088b0f52f288b646bcffb64f8c3ea4f276a38c4f8`  
		Last Modified: Fri, 18 Jun 2021 18:27:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb669f0511807cdf28c62961741c40f456eb2b7e2acf48ba47b1b75d3f810a80`  
		Last Modified: Fri, 18 Jun 2021 18:27:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ed42830001dfc2908f44fbc8a8f714dc9a6ed0c083c10798bbe423163c1a68`  
		Last Modified: Fri, 18 Jun 2021 18:27:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
