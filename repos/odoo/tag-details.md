<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:latest`](#odoolatest)

## `odoo:13`

```console
$ docker pull odoo@sha256:645d1e0a2da65bf614d8657fe745050e00259fb759b9af4dd10fcc2bffe52ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:faf0d6ab8ccf9871529a29f46b78c16a6ce61f40e17b4604533c781fc444076f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540331566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fe6e40a0875b24aa76aaa5d5817a027658056f3173bb590eef02dc22d7c007`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:20:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 Aug 2022 04:20:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 Aug 2022 04:20:42 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 04:24:34 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 Aug 2022 04:24:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:24:46 GMT
RUN npm install -g rtlcss
# Tue, 23 Aug 2022 04:24:46 GMT
ENV ODOO_VERSION=13.0
# Tue, 23 Aug 2022 04:24:46 GMT
ARG ODOO_RELEASE=20220819
# Tue, 23 Aug 2022 04:24:46 GMT
ARG ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
# Tue, 23 Aug 2022 04:25:59 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 23 Aug 2022 04:26:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 23 Aug 2022 04:26:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 23 Aug 2022 04:26:03 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 23 Aug 2022 04:26:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 23 Aug 2022 04:26:03 GMT
EXPOSE 8069 8071 8072
# Tue, 23 Aug 2022 04:26:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 23 Aug 2022 04:26:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 23 Aug 2022 04:26:03 GMT
USER odoo
# Tue, 23 Aug 2022 04:26:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Aug 2022 04:26:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bc659c82c5df3ceed5b594b12d2276649ddada6c21fc27a2f70b40a9e475a9`  
		Last Modified: Tue, 23 Aug 2022 04:28:26 GMT  
		Size: 207.1 MB (207143904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf9beead154e3aab7df26112ce7e2825e3fad4784b1e5c98c8c19370334c1e1`  
		Last Modified: Tue, 23 Aug 2022 04:28:05 GMT  
		Size: 13.4 MB (13442806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f765d64561bd0be0eaa52035b4ec790b19e63dae6849f79cc86644fb84b6b`  
		Last Modified: Tue, 23 Aug 2022 04:28:02 GMT  
		Size: 454.2 KB (454230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480200694743f69976ef925beef119bcca53824de5f72ebb281dddd0a35813e9`  
		Last Modified: Tue, 23 Aug 2022 04:28:32 GMT  
		Size: 292.1 MB (292149830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f78237f2db7d85fefeadc576f8cab0ae0c31bb983790c4aa4291d7916b9e7c8`  
		Last Modified: Tue, 23 Aug 2022 04:27:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c102771023bd8580bee5e3796aa29f9347d6320c5bbf903e64687d4bfe446204`  
		Last Modified: Tue, 23 Aug 2022 04:28:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454e871c5068376d7f42fb69f25f25a57388c7c4bc0d3b633bb74936655b1e85`  
		Last Modified: Tue, 23 Aug 2022 04:27:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40a974690cdee7e4b8c174f6559ac5ce6b3c47c04fb357de3b4f806bfe214d`  
		Last Modified: Tue, 23 Aug 2022 04:27:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:645d1e0a2da65bf614d8657fe745050e00259fb759b9af4dd10fcc2bffe52ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:faf0d6ab8ccf9871529a29f46b78c16a6ce61f40e17b4604533c781fc444076f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540331566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fe6e40a0875b24aa76aaa5d5817a027658056f3173bb590eef02dc22d7c007`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:20:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 Aug 2022 04:20:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 Aug 2022 04:20:42 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 04:24:34 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 Aug 2022 04:24:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:24:46 GMT
RUN npm install -g rtlcss
# Tue, 23 Aug 2022 04:24:46 GMT
ENV ODOO_VERSION=13.0
# Tue, 23 Aug 2022 04:24:46 GMT
ARG ODOO_RELEASE=20220819
# Tue, 23 Aug 2022 04:24:46 GMT
ARG ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
# Tue, 23 Aug 2022 04:25:59 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 23 Aug 2022 04:26:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 23 Aug 2022 04:26:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 23 Aug 2022 04:26:03 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 23 Aug 2022 04:26:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 23 Aug 2022 04:26:03 GMT
EXPOSE 8069 8071 8072
# Tue, 23 Aug 2022 04:26:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 23 Aug 2022 04:26:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 23 Aug 2022 04:26:03 GMT
USER odoo
# Tue, 23 Aug 2022 04:26:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Aug 2022 04:26:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bc659c82c5df3ceed5b594b12d2276649ddada6c21fc27a2f70b40a9e475a9`  
		Last Modified: Tue, 23 Aug 2022 04:28:26 GMT  
		Size: 207.1 MB (207143904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf9beead154e3aab7df26112ce7e2825e3fad4784b1e5c98c8c19370334c1e1`  
		Last Modified: Tue, 23 Aug 2022 04:28:05 GMT  
		Size: 13.4 MB (13442806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f765d64561bd0be0eaa52035b4ec790b19e63dae6849f79cc86644fb84b6b`  
		Last Modified: Tue, 23 Aug 2022 04:28:02 GMT  
		Size: 454.2 KB (454230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480200694743f69976ef925beef119bcca53824de5f72ebb281dddd0a35813e9`  
		Last Modified: Tue, 23 Aug 2022 04:28:32 GMT  
		Size: 292.1 MB (292149830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f78237f2db7d85fefeadc576f8cab0ae0c31bb983790c4aa4291d7916b9e7c8`  
		Last Modified: Tue, 23 Aug 2022 04:27:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c102771023bd8580bee5e3796aa29f9347d6320c5bbf903e64687d4bfe446204`  
		Last Modified: Tue, 23 Aug 2022 04:28:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454e871c5068376d7f42fb69f25f25a57388c7c4bc0d3b633bb74936655b1e85`  
		Last Modified: Tue, 23 Aug 2022 04:27:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40a974690cdee7e4b8c174f6559ac5ce6b3c47c04fb357de3b4f806bfe214d`  
		Last Modified: Tue, 23 Aug 2022 04:27:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:30e66e27f6d144823b1c9a5badb11bee10939d34d23e80fa044153058d6f4e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:6dab8100029b4a2e0864662dd75813e75e03be57756c7b79f8a589eda811b18f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530806947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4086a9601dbfba73215974eeefa21557d24f181e9dea1903e8cc70468f85a764`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:20:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 Aug 2022 04:20:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 Aug 2022 04:20:42 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 04:21:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 Aug 2022 04:21:59 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:22:02 GMT
RUN npm install -g rtlcss
# Tue, 23 Aug 2022 04:22:02 GMT
ENV ODOO_VERSION=14.0
# Tue, 23 Aug 2022 04:22:02 GMT
ARG ODOO_RELEASE=20220819
# Tue, 23 Aug 2022 04:22:02 GMT
ARG ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
# Tue, 23 Aug 2022 04:23:14 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 23 Aug 2022 04:23:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 23 Aug 2022 04:23:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 23 Aug 2022 04:23:18 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 23 Aug 2022 04:23:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 23 Aug 2022 04:23:18 GMT
EXPOSE 8069 8071 8072
# Tue, 23 Aug 2022 04:23:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 23 Aug 2022 04:23:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 23 Aug 2022 04:23:19 GMT
USER odoo
# Tue, 23 Aug 2022 04:23:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Aug 2022 04:23:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a659d0e2ab4fe22a3e85e8063766519e98d39e86af6b71909b51058e7bb4d`  
		Last Modified: Tue, 23 Aug 2022 04:27:42 GMT  
		Size: 213.2 MB (213182299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13632be899adb63dd5166f35d4195b362d0c1be609d4dcabac13530b04d03fd1`  
		Last Modified: Tue, 23 Aug 2022 04:27:19 GMT  
		Size: 13.4 MB (13444767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89ec81fb9348e6b4f6a91ae54dbad2d7fea55f2b1ee189efcbf42d3825a51a`  
		Last Modified: Tue, 23 Aug 2022 04:27:17 GMT  
		Size: 454.2 KB (454214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab59f1e601a83619201e618d1506b3470552f82470795f47a3daa21a43545a2`  
		Last Modified: Tue, 23 Aug 2022 04:27:49 GMT  
		Size: 276.6 MB (276584874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b7f42a79c5fa52717611134692d44ae969d433e0713a30761e4a21ea62ed4b`  
		Last Modified: Tue, 23 Aug 2022 04:27:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f22f51fa3384a844a1b59abfe912c53cacac4dc1974a192ab74de91ce29edca`  
		Last Modified: Tue, 23 Aug 2022 04:27:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46c91a65a35fbf0aeb1d83b336659c35fd72ce60760f91351d4c8bd9d677458`  
		Last Modified: Tue, 23 Aug 2022 04:27:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe302448aef770268a9057a089d63a1f1d9d4575459d7cc7c11a318f8de0422`  
		Last Modified: Tue, 23 Aug 2022 04:27:14 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:30e66e27f6d144823b1c9a5badb11bee10939d34d23e80fa044153058d6f4e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:6dab8100029b4a2e0864662dd75813e75e03be57756c7b79f8a589eda811b18f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530806947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4086a9601dbfba73215974eeefa21557d24f181e9dea1903e8cc70468f85a764`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:20:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 Aug 2022 04:20:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 Aug 2022 04:20:42 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 04:21:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 Aug 2022 04:21:59 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:22:02 GMT
RUN npm install -g rtlcss
# Tue, 23 Aug 2022 04:22:02 GMT
ENV ODOO_VERSION=14.0
# Tue, 23 Aug 2022 04:22:02 GMT
ARG ODOO_RELEASE=20220819
# Tue, 23 Aug 2022 04:22:02 GMT
ARG ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
# Tue, 23 Aug 2022 04:23:14 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 23 Aug 2022 04:23:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 23 Aug 2022 04:23:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 23 Aug 2022 04:23:18 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 23 Aug 2022 04:23:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 23 Aug 2022 04:23:18 GMT
EXPOSE 8069 8071 8072
# Tue, 23 Aug 2022 04:23:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 23 Aug 2022 04:23:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 23 Aug 2022 04:23:19 GMT
USER odoo
# Tue, 23 Aug 2022 04:23:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Aug 2022 04:23:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a659d0e2ab4fe22a3e85e8063766519e98d39e86af6b71909b51058e7bb4d`  
		Last Modified: Tue, 23 Aug 2022 04:27:42 GMT  
		Size: 213.2 MB (213182299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13632be899adb63dd5166f35d4195b362d0c1be609d4dcabac13530b04d03fd1`  
		Last Modified: Tue, 23 Aug 2022 04:27:19 GMT  
		Size: 13.4 MB (13444767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89ec81fb9348e6b4f6a91ae54dbad2d7fea55f2b1ee189efcbf42d3825a51a`  
		Last Modified: Tue, 23 Aug 2022 04:27:17 GMT  
		Size: 454.2 KB (454214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab59f1e601a83619201e618d1506b3470552f82470795f47a3daa21a43545a2`  
		Last Modified: Tue, 23 Aug 2022 04:27:49 GMT  
		Size: 276.6 MB (276584874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b7f42a79c5fa52717611134692d44ae969d433e0713a30761e4a21ea62ed4b`  
		Last Modified: Tue, 23 Aug 2022 04:27:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f22f51fa3384a844a1b59abfe912c53cacac4dc1974a192ab74de91ce29edca`  
		Last Modified: Tue, 23 Aug 2022 04:27:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46c91a65a35fbf0aeb1d83b336659c35fd72ce60760f91351d4c8bd9d677458`  
		Last Modified: Tue, 23 Aug 2022 04:27:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe302448aef770268a9057a089d63a1f1d9d4575459d7cc7c11a318f8de0422`  
		Last Modified: Tue, 23 Aug 2022 04:27:14 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:5be72a3f1a59c3f37ea5cbbc791beece6ff34199259306ab5fa83c89e0a87a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:ba9434e98b231033158cc6139230d5bab01b350790791928d5215a5a8fe339a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557751791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565bc47ebd32b0fd5e9509643cf1bce18145015c1a00ddfdbfb127d58e96c80c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:18:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 Aug 2022 04:18:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 Aug 2022 04:18:04 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 04:19:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 Aug 2022 04:19:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:19:14 GMT
RUN npm install -g rtlcss
# Tue, 23 Aug 2022 04:19:15 GMT
ENV ODOO_VERSION=15.0
# Tue, 23 Aug 2022 04:19:15 GMT
ARG ODOO_RELEASE=20220819
# Tue, 23 Aug 2022 04:19:15 GMT
ARG ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
# Tue, 23 Aug 2022 04:20:31 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 23 Aug 2022 04:20:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 23 Aug 2022 04:20:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 23 Aug 2022 04:20:36 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 23 Aug 2022 04:20:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 23 Aug 2022 04:20:36 GMT
EXPOSE 8069 8071 8072
# Tue, 23 Aug 2022 04:20:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 23 Aug 2022 04:20:36 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 23 Aug 2022 04:20:36 GMT
USER odoo
# Tue, 23 Aug 2022 04:20:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Aug 2022 04:20:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb8f3073d7aa12b590bbcfb6b670ff30bdce9db379f2ebccdd4349cd3d1b17`  
		Last Modified: Tue, 23 Aug 2022 04:26:53 GMT  
		Size: 220.3 MB (220296783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b432e5a5fa86f6c173d9d8614889a638ff0891c38a9c08f7fa5cdf9e9a63b044`  
		Last Modified: Tue, 23 Aug 2022 04:26:27 GMT  
		Size: 2.5 MB (2514624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdd6ff1405cad92ef01a751c4193873ed8078e06ba52d718c300386c2189830`  
		Last Modified: Tue, 23 Aug 2022 04:26:27 GMT  
		Size: 449.9 KB (449883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7081f29ca3c4e377f6a90209b7fbef73976a4ddcce86095843d50a8b4945d0`  
		Last Modified: Tue, 23 Aug 2022 04:27:01 GMT  
		Size: 303.1 MB (303106551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b83828199ee9f5a4681c24774f4d003768ee92a2b6e4062d0c1dc3ba4acc907`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305715fb7811b6787566f06c214f28e637563f6fe7ea7eba4f53d94a1b617ebd`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34377b3689563ea195cfb317f1dcb14a057ddf5b22d7a8e14dacd1bcd4383854`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92dd5e7fe9c7afccd6f4af094ac4e7a14298a7fec05896db31996bf5443b536`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:5be72a3f1a59c3f37ea5cbbc791beece6ff34199259306ab5fa83c89e0a87a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:ba9434e98b231033158cc6139230d5bab01b350790791928d5215a5a8fe339a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557751791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565bc47ebd32b0fd5e9509643cf1bce18145015c1a00ddfdbfb127d58e96c80c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:18:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 Aug 2022 04:18:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 Aug 2022 04:18:04 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 04:19:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 Aug 2022 04:19:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:19:14 GMT
RUN npm install -g rtlcss
# Tue, 23 Aug 2022 04:19:15 GMT
ENV ODOO_VERSION=15.0
# Tue, 23 Aug 2022 04:19:15 GMT
ARG ODOO_RELEASE=20220819
# Tue, 23 Aug 2022 04:19:15 GMT
ARG ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
# Tue, 23 Aug 2022 04:20:31 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 23 Aug 2022 04:20:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 23 Aug 2022 04:20:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 23 Aug 2022 04:20:36 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 23 Aug 2022 04:20:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 23 Aug 2022 04:20:36 GMT
EXPOSE 8069 8071 8072
# Tue, 23 Aug 2022 04:20:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 23 Aug 2022 04:20:36 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 23 Aug 2022 04:20:36 GMT
USER odoo
# Tue, 23 Aug 2022 04:20:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Aug 2022 04:20:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb8f3073d7aa12b590bbcfb6b670ff30bdce9db379f2ebccdd4349cd3d1b17`  
		Last Modified: Tue, 23 Aug 2022 04:26:53 GMT  
		Size: 220.3 MB (220296783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b432e5a5fa86f6c173d9d8614889a638ff0891c38a9c08f7fa5cdf9e9a63b044`  
		Last Modified: Tue, 23 Aug 2022 04:26:27 GMT  
		Size: 2.5 MB (2514624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdd6ff1405cad92ef01a751c4193873ed8078e06ba52d718c300386c2189830`  
		Last Modified: Tue, 23 Aug 2022 04:26:27 GMT  
		Size: 449.9 KB (449883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7081f29ca3c4e377f6a90209b7fbef73976a4ddcce86095843d50a8b4945d0`  
		Last Modified: Tue, 23 Aug 2022 04:27:01 GMT  
		Size: 303.1 MB (303106551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b83828199ee9f5a4681c24774f4d003768ee92a2b6e4062d0c1dc3ba4acc907`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305715fb7811b6787566f06c214f28e637563f6fe7ea7eba4f53d94a1b617ebd`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34377b3689563ea195cfb317f1dcb14a057ddf5b22d7a8e14dacd1bcd4383854`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92dd5e7fe9c7afccd6f4af094ac4e7a14298a7fec05896db31996bf5443b536`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:5be72a3f1a59c3f37ea5cbbc791beece6ff34199259306ab5fa83c89e0a87a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:ba9434e98b231033158cc6139230d5bab01b350790791928d5215a5a8fe339a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557751791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565bc47ebd32b0fd5e9509643cf1bce18145015c1a00ddfdbfb127d58e96c80c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:18:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 23 Aug 2022 04:18:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 23 Aug 2022 04:18:04 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 04:19:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 23 Aug 2022 04:19:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:19:14 GMT
RUN npm install -g rtlcss
# Tue, 23 Aug 2022 04:19:15 GMT
ENV ODOO_VERSION=15.0
# Tue, 23 Aug 2022 04:19:15 GMT
ARG ODOO_RELEASE=20220819
# Tue, 23 Aug 2022 04:19:15 GMT
ARG ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
# Tue, 23 Aug 2022 04:20:31 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 23 Aug 2022 04:20:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 23 Aug 2022 04:20:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 23 Aug 2022 04:20:36 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 23 Aug 2022 04:20:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 23 Aug 2022 04:20:36 GMT
EXPOSE 8069 8071 8072
# Tue, 23 Aug 2022 04:20:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 23 Aug 2022 04:20:36 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 23 Aug 2022 04:20:36 GMT
USER odoo
# Tue, 23 Aug 2022 04:20:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Aug 2022 04:20:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb8f3073d7aa12b590bbcfb6b670ff30bdce9db379f2ebccdd4349cd3d1b17`  
		Last Modified: Tue, 23 Aug 2022 04:26:53 GMT  
		Size: 220.3 MB (220296783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b432e5a5fa86f6c173d9d8614889a638ff0891c38a9c08f7fa5cdf9e9a63b044`  
		Last Modified: Tue, 23 Aug 2022 04:26:27 GMT  
		Size: 2.5 MB (2514624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdd6ff1405cad92ef01a751c4193873ed8078e06ba52d718c300386c2189830`  
		Last Modified: Tue, 23 Aug 2022 04:26:27 GMT  
		Size: 449.9 KB (449883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7081f29ca3c4e377f6a90209b7fbef73976a4ddcce86095843d50a8b4945d0`  
		Last Modified: Tue, 23 Aug 2022 04:27:01 GMT  
		Size: 303.1 MB (303106551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b83828199ee9f5a4681c24774f4d003768ee92a2b6e4062d0c1dc3ba4acc907`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305715fb7811b6787566f06c214f28e637563f6fe7ea7eba4f53d94a1b617ebd`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34377b3689563ea195cfb317f1dcb14a057ddf5b22d7a8e14dacd1bcd4383854`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92dd5e7fe9c7afccd6f4af094ac4e7a14298a7fec05896db31996bf5443b536`  
		Last Modified: Tue, 23 Aug 2022 04:26:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
