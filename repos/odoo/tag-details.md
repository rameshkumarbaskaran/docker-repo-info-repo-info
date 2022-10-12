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
$ docker pull odoo@sha256:334414ad9065c4032e90d02aaa71a310a37a208e7f694dc23d0c670fd9d9fd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:3c779f60cb7462ba30afa9326e4b93f8202b182982f7baa937c97b95c6c345f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.0 MB (530984394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b4a303acd886c9496ea09720f9bbdda90f39b9bef822b6dadbb9c6142d9014`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:50:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:50:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:50:50 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:52:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:52:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:52:35 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:52:35 GMT
ENV ODOO_VERSION=14.0
# Wed, 12 Oct 2022 19:24:40 GMT
ARG ODOO_RELEASE=20221012
# Wed, 12 Oct 2022 19:24:40 GMT
ARG ODOO_SHA=f938f53b8c9de5bb941bffbca1eb4d6bf44fa314
# Wed, 12 Oct 2022 19:26:01 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f938f53b8c9de5bb941bffbca1eb4d6bf44fa314
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 Oct 2022 19:26:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 12 Oct 2022 19:26:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 Oct 2022 19:26:05 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f938f53b8c9de5bb941bffbca1eb4d6bf44fa314
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 Oct 2022 19:26:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 Oct 2022 19:26:05 GMT
EXPOSE 8069 8071 8072
# Wed, 12 Oct 2022 19:26:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 Oct 2022 19:26:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 Oct 2022 19:26:06 GMT
USER odoo
# Wed, 12 Oct 2022 19:26:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 19:26:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73991209e36bf89d51fca585d2b4242c0cb80cbfd84e98fe6314e9b7c0d1dde1`  
		Last Modified: Wed, 05 Oct 2022 12:59:16 GMT  
		Size: 213.2 MB (213182348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b040c0568df4c7a36beaffa7b2957e709200877eb8d18ce95049f470d8381`  
		Last Modified: Wed, 05 Oct 2022 12:58:54 GMT  
		Size: 13.4 MB (13443968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101df339f0e4711374ae94bdfc877da10ab15e76776311e1cc4ea61abed09c22`  
		Last Modified: Wed, 05 Oct 2022 12:58:51 GMT  
		Size: 453.2 KB (453236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263669d770c2101176c96e9d72e4e56a436592b47ed841ef89e603ddefc745f6`  
		Last Modified: Wed, 12 Oct 2022 19:28:35 GMT  
		Size: 276.8 MB (276764335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a106717a3ac5cb020d4485d5486b64f2f85a083910e8bf4c8020de43a88871f`  
		Last Modified: Wed, 12 Oct 2022 19:28:01 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ab4787300a1c5da88ebb0952ecd7ace16786231d6c132d4ff1890e894f3255`  
		Last Modified: Wed, 12 Oct 2022 19:28:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d240b55954c69301b2b074c0db75363a29a1be65df9a67dee784554892bcd5d7`  
		Last Modified: Wed, 12 Oct 2022 19:28:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebe85dcdccf07941efeda9f0b9a8cfd37ca63b0a228de1d9607f40aad2aed64`  
		Last Modified: Wed, 12 Oct 2022 19:28:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:334414ad9065c4032e90d02aaa71a310a37a208e7f694dc23d0c670fd9d9fd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:3c779f60cb7462ba30afa9326e4b93f8202b182982f7baa937c97b95c6c345f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.0 MB (530984394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b4a303acd886c9496ea09720f9bbdda90f39b9bef822b6dadbb9c6142d9014`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:50:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:50:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:50:50 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:52:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:52:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:52:35 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:52:35 GMT
ENV ODOO_VERSION=14.0
# Wed, 12 Oct 2022 19:24:40 GMT
ARG ODOO_RELEASE=20221012
# Wed, 12 Oct 2022 19:24:40 GMT
ARG ODOO_SHA=f938f53b8c9de5bb941bffbca1eb4d6bf44fa314
# Wed, 12 Oct 2022 19:26:01 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f938f53b8c9de5bb941bffbca1eb4d6bf44fa314
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 Oct 2022 19:26:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 12 Oct 2022 19:26:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 Oct 2022 19:26:05 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f938f53b8c9de5bb941bffbca1eb4d6bf44fa314
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 Oct 2022 19:26:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 Oct 2022 19:26:05 GMT
EXPOSE 8069 8071 8072
# Wed, 12 Oct 2022 19:26:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 Oct 2022 19:26:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 Oct 2022 19:26:06 GMT
USER odoo
# Wed, 12 Oct 2022 19:26:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 19:26:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73991209e36bf89d51fca585d2b4242c0cb80cbfd84e98fe6314e9b7c0d1dde1`  
		Last Modified: Wed, 05 Oct 2022 12:59:16 GMT  
		Size: 213.2 MB (213182348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b040c0568df4c7a36beaffa7b2957e709200877eb8d18ce95049f470d8381`  
		Last Modified: Wed, 05 Oct 2022 12:58:54 GMT  
		Size: 13.4 MB (13443968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101df339f0e4711374ae94bdfc877da10ab15e76776311e1cc4ea61abed09c22`  
		Last Modified: Wed, 05 Oct 2022 12:58:51 GMT  
		Size: 453.2 KB (453236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263669d770c2101176c96e9d72e4e56a436592b47ed841ef89e603ddefc745f6`  
		Last Modified: Wed, 12 Oct 2022 19:28:35 GMT  
		Size: 276.8 MB (276764335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a106717a3ac5cb020d4485d5486b64f2f85a083910e8bf4c8020de43a88871f`  
		Last Modified: Wed, 12 Oct 2022 19:28:01 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ab4787300a1c5da88ebb0952ecd7ace16786231d6c132d4ff1890e894f3255`  
		Last Modified: Wed, 12 Oct 2022 19:28:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d240b55954c69301b2b074c0db75363a29a1be65df9a67dee784554892bcd5d7`  
		Last Modified: Wed, 12 Oct 2022 19:28:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebe85dcdccf07941efeda9f0b9a8cfd37ca63b0a228de1d9607f40aad2aed64`  
		Last Modified: Wed, 12 Oct 2022 19:28:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:e283b7b1c067287761fef77359e84e93945edca037ce8ff8d534a37e75150983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:dbe22aeff08004c44f63e56134677fcb76b92ec631d907814997ad9d6c65811a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.7 MB (558706323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640c02b51f011d547eabd2dfb28569eb17cc6a517cb3210afdaf86647b35f12d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:47:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:47:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:47:42 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:48:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:49:04 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:49:05 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:49:05 GMT
ENV ODOO_VERSION=15.0
# Wed, 12 Oct 2022 19:23:02 GMT
ARG ODOO_RELEASE=20221012
# Wed, 12 Oct 2022 19:23:02 GMT
ARG ODOO_SHA=55bf57fd9544ba5ea4033507eaf424cbbf1e95dc
# Wed, 12 Oct 2022 19:24:19 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=55bf57fd9544ba5ea4033507eaf424cbbf1e95dc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 Oct 2022 19:24:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 12 Oct 2022 19:24:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 Oct 2022 19:24:24 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=55bf57fd9544ba5ea4033507eaf424cbbf1e95dc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 Oct 2022 19:24:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 Oct 2022 19:24:24 GMT
EXPOSE 8069 8071 8072
# Wed, 12 Oct 2022 19:24:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 Oct 2022 19:24:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 Oct 2022 19:24:24 GMT
USER odoo
# Wed, 12 Oct 2022 19:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 19:24:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1eb84e6e02a853d9decd11a159b54a0995b7293fa476df2fec218d33b1df6d`  
		Last Modified: Wed, 05 Oct 2022 12:58:29 GMT  
		Size: 220.3 MB (220296502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e514ed12a4b7e196251756d20aa16acbeaf5a3a34f67005bd99c3faa6bf6cfba`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 2.5 MB (2513557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bec1ca6984d8b904d4439a7f235c18d3ab647da175de5faa8ba74a9c232cb8`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 449.2 KB (449160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2864a11ef2e69535a4a0e23b61e2cebae9f992dfb84f1636dacf980bc026973d`  
		Last Modified: Wed, 12 Oct 2022 19:27:52 GMT  
		Size: 304.0 MB (304024542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5aefc400d057e61aa73446847fbb2a451d9866fa65a2bcb58b5e32cb274204`  
		Last Modified: Wed, 12 Oct 2022 19:27:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f666df7d16aceb1f96d3ae465110ca585c9656684f9f857d25c3b0c0571260d0`  
		Last Modified: Wed, 12 Oct 2022 19:27:16 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bbdb142b4abe4a5c6315bb522189f74e35126d3bead21a38ac54a28571f57c`  
		Last Modified: Wed, 12 Oct 2022 19:27:16 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a381787e0b6683f8fd2236648e00ad114851d8b329c1f64ea50393b867bab2`  
		Last Modified: Wed, 12 Oct 2022 19:27:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:e283b7b1c067287761fef77359e84e93945edca037ce8ff8d534a37e75150983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:dbe22aeff08004c44f63e56134677fcb76b92ec631d907814997ad9d6c65811a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.7 MB (558706323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640c02b51f011d547eabd2dfb28569eb17cc6a517cb3210afdaf86647b35f12d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:47:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:47:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:47:42 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:48:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:49:04 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:49:05 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:49:05 GMT
ENV ODOO_VERSION=15.0
# Wed, 12 Oct 2022 19:23:02 GMT
ARG ODOO_RELEASE=20221012
# Wed, 12 Oct 2022 19:23:02 GMT
ARG ODOO_SHA=55bf57fd9544ba5ea4033507eaf424cbbf1e95dc
# Wed, 12 Oct 2022 19:24:19 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=55bf57fd9544ba5ea4033507eaf424cbbf1e95dc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 Oct 2022 19:24:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 12 Oct 2022 19:24:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 Oct 2022 19:24:24 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=55bf57fd9544ba5ea4033507eaf424cbbf1e95dc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 Oct 2022 19:24:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 Oct 2022 19:24:24 GMT
EXPOSE 8069 8071 8072
# Wed, 12 Oct 2022 19:24:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 Oct 2022 19:24:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 Oct 2022 19:24:24 GMT
USER odoo
# Wed, 12 Oct 2022 19:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 19:24:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1eb84e6e02a853d9decd11a159b54a0995b7293fa476df2fec218d33b1df6d`  
		Last Modified: Wed, 05 Oct 2022 12:58:29 GMT  
		Size: 220.3 MB (220296502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e514ed12a4b7e196251756d20aa16acbeaf5a3a34f67005bd99c3faa6bf6cfba`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 2.5 MB (2513557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bec1ca6984d8b904d4439a7f235c18d3ab647da175de5faa8ba74a9c232cb8`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 449.2 KB (449160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2864a11ef2e69535a4a0e23b61e2cebae9f992dfb84f1636dacf980bc026973d`  
		Last Modified: Wed, 12 Oct 2022 19:27:52 GMT  
		Size: 304.0 MB (304024542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5aefc400d057e61aa73446847fbb2a451d9866fa65a2bcb58b5e32cb274204`  
		Last Modified: Wed, 12 Oct 2022 19:27:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f666df7d16aceb1f96d3ae465110ca585c9656684f9f857d25c3b0c0571260d0`  
		Last Modified: Wed, 12 Oct 2022 19:27:16 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bbdb142b4abe4a5c6315bb522189f74e35126d3bead21a38ac54a28571f57c`  
		Last Modified: Wed, 12 Oct 2022 19:27:16 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a381787e0b6683f8fd2236648e00ad114851d8b329c1f64ea50393b867bab2`  
		Last Modified: Wed, 12 Oct 2022 19:27:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:77c4f3784e373614562ab63252db807ab7dbe683faaa88b65e0f519eccdae83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:b0eb4010bef8bfab2e430755f62504c4f4b1d97da377411a5dfc07a276737aa5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548887141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8138ed2d21817c3bc4f66ab46911682f46d148341c5add269567dd4ebee1d46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:47:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:47:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:47:42 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:48:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:49:04 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:49:05 GMT
RUN npm install -g rtlcss
# Wed, 12 Oct 2022 19:21:23 GMT
ENV ODOO_VERSION=16.0
# Wed, 12 Oct 2022 19:21:24 GMT
ARG ODOO_RELEASE=20221012
# Wed, 12 Oct 2022 19:21:24 GMT
ARG ODOO_SHA=f34bc089609c2a7da65f25f29cf4e0218c7af464
# Wed, 12 Oct 2022 19:22:47 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f34bc089609c2a7da65f25f29cf4e0218c7af464
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 Oct 2022 19:22:51 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 12 Oct 2022 19:22:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 Oct 2022 19:22:52 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f34bc089609c2a7da65f25f29cf4e0218c7af464
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 Oct 2022 19:22:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 Oct 2022 19:22:52 GMT
EXPOSE 8069 8071 8072
# Wed, 12 Oct 2022 19:22:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 Oct 2022 19:22:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 Oct 2022 19:22:52 GMT
USER odoo
# Wed, 12 Oct 2022 19:22:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 19:22:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1eb84e6e02a853d9decd11a159b54a0995b7293fa476df2fec218d33b1df6d`  
		Last Modified: Wed, 05 Oct 2022 12:58:29 GMT  
		Size: 220.3 MB (220296502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e514ed12a4b7e196251756d20aa16acbeaf5a3a34f67005bd99c3faa6bf6cfba`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 2.5 MB (2513557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bec1ca6984d8b904d4439a7f235c18d3ab647da175de5faa8ba74a9c232cb8`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 449.2 KB (449160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600f159e804299de6915fa0623c12e0938e07be04a9470823c48191bb7d0efec`  
		Last Modified: Wed, 12 Oct 2022 19:27:03 GMT  
		Size: 294.2 MB (294205351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5b4fea774e431316951574fd4a8b7aaac22fec8039eb18a7ae09ebaa3b59a6`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da1dd2d3ed8d6c79e354d86ed8c603502103ca7eb944ff0f9d788163823c4d3`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57a7274778f6fd9a52fb18ea3d96af0449b88de20f33d91438fcc94f9fe36ff`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b5e08bffe8ddc92a4b0ced0e51b0d58ce45167dc741bf3168a021c4d5d1c20`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:77c4f3784e373614562ab63252db807ab7dbe683faaa88b65e0f519eccdae83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:b0eb4010bef8bfab2e430755f62504c4f4b1d97da377411a5dfc07a276737aa5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548887141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8138ed2d21817c3bc4f66ab46911682f46d148341c5add269567dd4ebee1d46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:47:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:47:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:47:42 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:48:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:49:04 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:49:05 GMT
RUN npm install -g rtlcss
# Wed, 12 Oct 2022 19:21:23 GMT
ENV ODOO_VERSION=16.0
# Wed, 12 Oct 2022 19:21:24 GMT
ARG ODOO_RELEASE=20221012
# Wed, 12 Oct 2022 19:21:24 GMT
ARG ODOO_SHA=f34bc089609c2a7da65f25f29cf4e0218c7af464
# Wed, 12 Oct 2022 19:22:47 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f34bc089609c2a7da65f25f29cf4e0218c7af464
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 Oct 2022 19:22:51 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 12 Oct 2022 19:22:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 Oct 2022 19:22:52 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f34bc089609c2a7da65f25f29cf4e0218c7af464
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 Oct 2022 19:22:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 Oct 2022 19:22:52 GMT
EXPOSE 8069 8071 8072
# Wed, 12 Oct 2022 19:22:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 Oct 2022 19:22:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 Oct 2022 19:22:52 GMT
USER odoo
# Wed, 12 Oct 2022 19:22:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 19:22:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1eb84e6e02a853d9decd11a159b54a0995b7293fa476df2fec218d33b1df6d`  
		Last Modified: Wed, 05 Oct 2022 12:58:29 GMT  
		Size: 220.3 MB (220296502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e514ed12a4b7e196251756d20aa16acbeaf5a3a34f67005bd99c3faa6bf6cfba`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 2.5 MB (2513557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bec1ca6984d8b904d4439a7f235c18d3ab647da175de5faa8ba74a9c232cb8`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 449.2 KB (449160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600f159e804299de6915fa0623c12e0938e07be04a9470823c48191bb7d0efec`  
		Last Modified: Wed, 12 Oct 2022 19:27:03 GMT  
		Size: 294.2 MB (294205351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5b4fea774e431316951574fd4a8b7aaac22fec8039eb18a7ae09ebaa3b59a6`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da1dd2d3ed8d6c79e354d86ed8c603502103ca7eb944ff0f9d788163823c4d3`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57a7274778f6fd9a52fb18ea3d96af0449b88de20f33d91438fcc94f9fe36ff`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b5e08bffe8ddc92a4b0ced0e51b0d58ce45167dc741bf3168a021c4d5d1c20`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:77c4f3784e373614562ab63252db807ab7dbe683faaa88b65e0f519eccdae83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b0eb4010bef8bfab2e430755f62504c4f4b1d97da377411a5dfc07a276737aa5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548887141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8138ed2d21817c3bc4f66ab46911682f46d148341c5add269567dd4ebee1d46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:47:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:47:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:47:42 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:48:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:49:04 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:49:05 GMT
RUN npm install -g rtlcss
# Wed, 12 Oct 2022 19:21:23 GMT
ENV ODOO_VERSION=16.0
# Wed, 12 Oct 2022 19:21:24 GMT
ARG ODOO_RELEASE=20221012
# Wed, 12 Oct 2022 19:21:24 GMT
ARG ODOO_SHA=f34bc089609c2a7da65f25f29cf4e0218c7af464
# Wed, 12 Oct 2022 19:22:47 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f34bc089609c2a7da65f25f29cf4e0218c7af464
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 Oct 2022 19:22:51 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 12 Oct 2022 19:22:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 Oct 2022 19:22:52 GMT
# ARGS: ODOO_RELEASE=20221012 ODOO_SHA=f34bc089609c2a7da65f25f29cf4e0218c7af464
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 Oct 2022 19:22:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 Oct 2022 19:22:52 GMT
EXPOSE 8069 8071 8072
# Wed, 12 Oct 2022 19:22:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 Oct 2022 19:22:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 Oct 2022 19:22:52 GMT
USER odoo
# Wed, 12 Oct 2022 19:22:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 19:22:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1eb84e6e02a853d9decd11a159b54a0995b7293fa476df2fec218d33b1df6d`  
		Last Modified: Wed, 05 Oct 2022 12:58:29 GMT  
		Size: 220.3 MB (220296502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e514ed12a4b7e196251756d20aa16acbeaf5a3a34f67005bd99c3faa6bf6cfba`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 2.5 MB (2513557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bec1ca6984d8b904d4439a7f235c18d3ab647da175de5faa8ba74a9c232cb8`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 449.2 KB (449160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600f159e804299de6915fa0623c12e0938e07be04a9470823c48191bb7d0efec`  
		Last Modified: Wed, 12 Oct 2022 19:27:03 GMT  
		Size: 294.2 MB (294205351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5b4fea774e431316951574fd4a8b7aaac22fec8039eb18a7ae09ebaa3b59a6`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da1dd2d3ed8d6c79e354d86ed8c603502103ca7eb944ff0f9d788163823c4d3`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57a7274778f6fd9a52fb18ea3d96af0449b88de20f33d91438fcc94f9fe36ff`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b5e08bffe8ddc92a4b0ced0e51b0d58ce45167dc741bf3168a021c4d5d1c20`  
		Last Modified: Wed, 12 Oct 2022 19:26:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
