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
$ docker pull odoo@sha256:20a1a574fd6c29907b3060b32bd962432bc57c35525c73610915b099fa52a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:cd0e8da8149ba66d8aa749075e8274917fec14e6b4ca3c7b92e3c97fd58a20ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.1 MB (531093726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd1926dd34f5e419f83cbadcf4ae41328cfbe7040752c67611e12024d941908`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:22:13 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 25 Oct 2022 04:22:13 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 25 Oct 2022 04:22:13 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:23:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 25 Oct 2022 04:23:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:23:58 GMT
RUN npm install -g rtlcss
# Tue, 25 Oct 2022 04:23:58 GMT
ENV ODOO_VERSION=14.0
# Wed, 26 Oct 2022 06:25:51 GMT
ARG ODOO_RELEASE=20221025
# Wed, 26 Oct 2022 06:25:51 GMT
ARG ODOO_SHA=3be24ed710e51041a1b23d2ae55408077572cc5a
# Wed, 26 Oct 2022 06:27:14 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=3be24ed710e51041a1b23d2ae55408077572cc5a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Oct 2022 06:27:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Oct 2022 06:27:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Oct 2022 06:27:19 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=3be24ed710e51041a1b23d2ae55408077572cc5a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Oct 2022 06:27:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Oct 2022 06:27:19 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Oct 2022 06:27:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Oct 2022 06:27:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Oct 2022 06:27:19 GMT
USER odoo
# Wed, 26 Oct 2022 06:27:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 06:27:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faac7a4e46b306b96418e8946e9ba17e1fb320a1ae730c993241aafaf249b5d1`  
		Last Modified: Tue, 25 Oct 2022 04:27:49 GMT  
		Size: 213.2 MB (213185702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7011c07b6707d10ea804fe3b27f6772b3cea5b67c0ebb2933a79d1b4b7e123`  
		Last Modified: Tue, 25 Oct 2022 04:27:27 GMT  
		Size: 13.5 MB (13528969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254861bde8dbcd4ddf95d713137dde2c44d43eb2c907ea71665ee05060d6071`  
		Last Modified: Tue, 25 Oct 2022 04:27:24 GMT  
		Size: 453.8 KB (453804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a229c5ac47cf7f359902b45f5f868f167ad72c9faf9e82262c595033370605`  
		Last Modified: Wed, 26 Oct 2022 06:29:46 GMT  
		Size: 276.8 MB (276781952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27325f691f5fe06745e1d50e2468f7db41ad267fc10cf1095705fe34aec6e35b`  
		Last Modified: Wed, 26 Oct 2022 06:29:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b80ca83207710765c8d7bcf54e3cdc692a59658d9b0eebd24147e4f3e07bf1a`  
		Last Modified: Wed, 26 Oct 2022 06:29:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928a13802c8846e9378a07c350d3ec2afe77e684d711cb0275c397c5afa030bc`  
		Last Modified: Wed, 26 Oct 2022 06:29:13 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4fd49896a7ff7692babd3dfaacbaf833ef55db44b441250b94be4bbc079baa`  
		Last Modified: Wed, 26 Oct 2022 06:29:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:20a1a574fd6c29907b3060b32bd962432bc57c35525c73610915b099fa52a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:cd0e8da8149ba66d8aa749075e8274917fec14e6b4ca3c7b92e3c97fd58a20ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.1 MB (531093726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd1926dd34f5e419f83cbadcf4ae41328cfbe7040752c67611e12024d941908`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:22:13 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 25 Oct 2022 04:22:13 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 25 Oct 2022 04:22:13 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:23:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 25 Oct 2022 04:23:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:23:58 GMT
RUN npm install -g rtlcss
# Tue, 25 Oct 2022 04:23:58 GMT
ENV ODOO_VERSION=14.0
# Wed, 26 Oct 2022 06:25:51 GMT
ARG ODOO_RELEASE=20221025
# Wed, 26 Oct 2022 06:25:51 GMT
ARG ODOO_SHA=3be24ed710e51041a1b23d2ae55408077572cc5a
# Wed, 26 Oct 2022 06:27:14 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=3be24ed710e51041a1b23d2ae55408077572cc5a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Oct 2022 06:27:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Oct 2022 06:27:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Oct 2022 06:27:19 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=3be24ed710e51041a1b23d2ae55408077572cc5a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Oct 2022 06:27:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Oct 2022 06:27:19 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Oct 2022 06:27:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Oct 2022 06:27:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Oct 2022 06:27:19 GMT
USER odoo
# Wed, 26 Oct 2022 06:27:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 06:27:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faac7a4e46b306b96418e8946e9ba17e1fb320a1ae730c993241aafaf249b5d1`  
		Last Modified: Tue, 25 Oct 2022 04:27:49 GMT  
		Size: 213.2 MB (213185702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7011c07b6707d10ea804fe3b27f6772b3cea5b67c0ebb2933a79d1b4b7e123`  
		Last Modified: Tue, 25 Oct 2022 04:27:27 GMT  
		Size: 13.5 MB (13528969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254861bde8dbcd4ddf95d713137dde2c44d43eb2c907ea71665ee05060d6071`  
		Last Modified: Tue, 25 Oct 2022 04:27:24 GMT  
		Size: 453.8 KB (453804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a229c5ac47cf7f359902b45f5f868f167ad72c9faf9e82262c595033370605`  
		Last Modified: Wed, 26 Oct 2022 06:29:46 GMT  
		Size: 276.8 MB (276781952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27325f691f5fe06745e1d50e2468f7db41ad267fc10cf1095705fe34aec6e35b`  
		Last Modified: Wed, 26 Oct 2022 06:29:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b80ca83207710765c8d7bcf54e3cdc692a59658d9b0eebd24147e4f3e07bf1a`  
		Last Modified: Wed, 26 Oct 2022 06:29:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928a13802c8846e9378a07c350d3ec2afe77e684d711cb0275c397c5afa030bc`  
		Last Modified: Wed, 26 Oct 2022 06:29:13 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4fd49896a7ff7692babd3dfaacbaf833ef55db44b441250b94be4bbc079baa`  
		Last Modified: Wed, 26 Oct 2022 06:29:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:eedac055e1ea22f16300b6c8ff7fa37b9813a44cd12c74abca73f266fc2410f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:d80933a740fce3473d52ddbff78a4228119fcd3c6ddeca856b2d589d7ad4fa5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 MB (559031182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b5afea584e99d5c34319006bbc8f306e84f6cd2a974dc942702e41ba361784`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:17:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 25 Oct 2022 04:17:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 25 Oct 2022 04:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:18:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 25 Oct 2022 04:18:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:18:54 GMT
RUN npm install -g rtlcss
# Tue, 25 Oct 2022 04:20:35 GMT
ENV ODOO_VERSION=15.0
# Wed, 26 Oct 2022 06:24:13 GMT
ARG ODOO_RELEASE=20221025
# Wed, 26 Oct 2022 06:24:13 GMT
ARG ODOO_SHA=923fdec85ac9a4230fc93af00d12d8911a0613b4
# Wed, 26 Oct 2022 06:25:28 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=923fdec85ac9a4230fc93af00d12d8911a0613b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Oct 2022 06:25:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Oct 2022 06:25:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Oct 2022 06:25:33 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=923fdec85ac9a4230fc93af00d12d8911a0613b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Oct 2022 06:25:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Oct 2022 06:25:34 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Oct 2022 06:25:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Oct 2022 06:25:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Oct 2022 06:25:34 GMT
USER odoo
# Wed, 26 Oct 2022 06:25:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 06:25:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f207492967abb893017aed63de26947bc26869c41cb3ae43d047964a3f68abbe`  
		Last Modified: Tue, 25 Oct 2022 04:26:18 GMT  
		Size: 220.3 MB (220299448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034ca3be8a4120921abf777d526b8d64a15bfde37777c39a62f8c4934362a209`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 2.6 MB (2582213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260a86372800d03191e4df8077b594ccd6ea0f53bbc9f7f306cd191796d9f641`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 449.8 KB (449767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4128bdbb4fe72c8ed3e9d9b713c20d0bae1357d419ebf75beceda072cefc348`  
		Last Modified: Wed, 26 Oct 2022 06:29:03 GMT  
		Size: 304.3 MB (304277251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d112c7e3585a0b560df18d78d114b4535ab174294ffa0fa0592d8dc694ddaea`  
		Last Modified: Wed, 26 Oct 2022 06:28:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9181a2eac45a7f219f0e2daf10144440ffc2b1e673d892e3d82a13ecb453c3`  
		Last Modified: Wed, 26 Oct 2022 06:28:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d7c6afd6794832aac6b908431866b755a877e7f60b7e14b3f71926400a958b`  
		Last Modified: Wed, 26 Oct 2022 06:28:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b9ce9af0177ba2820a2312e843d537e6a574242f5727c1b7a5006bce66f318`  
		Last Modified: Wed, 26 Oct 2022 06:28:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:eedac055e1ea22f16300b6c8ff7fa37b9813a44cd12c74abca73f266fc2410f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:d80933a740fce3473d52ddbff78a4228119fcd3c6ddeca856b2d589d7ad4fa5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 MB (559031182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b5afea584e99d5c34319006bbc8f306e84f6cd2a974dc942702e41ba361784`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:17:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 25 Oct 2022 04:17:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 25 Oct 2022 04:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:18:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 25 Oct 2022 04:18:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:18:54 GMT
RUN npm install -g rtlcss
# Tue, 25 Oct 2022 04:20:35 GMT
ENV ODOO_VERSION=15.0
# Wed, 26 Oct 2022 06:24:13 GMT
ARG ODOO_RELEASE=20221025
# Wed, 26 Oct 2022 06:24:13 GMT
ARG ODOO_SHA=923fdec85ac9a4230fc93af00d12d8911a0613b4
# Wed, 26 Oct 2022 06:25:28 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=923fdec85ac9a4230fc93af00d12d8911a0613b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Oct 2022 06:25:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Oct 2022 06:25:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Oct 2022 06:25:33 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=923fdec85ac9a4230fc93af00d12d8911a0613b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Oct 2022 06:25:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Oct 2022 06:25:34 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Oct 2022 06:25:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Oct 2022 06:25:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Oct 2022 06:25:34 GMT
USER odoo
# Wed, 26 Oct 2022 06:25:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 06:25:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f207492967abb893017aed63de26947bc26869c41cb3ae43d047964a3f68abbe`  
		Last Modified: Tue, 25 Oct 2022 04:26:18 GMT  
		Size: 220.3 MB (220299448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034ca3be8a4120921abf777d526b8d64a15bfde37777c39a62f8c4934362a209`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 2.6 MB (2582213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260a86372800d03191e4df8077b594ccd6ea0f53bbc9f7f306cd191796d9f641`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 449.8 KB (449767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4128bdbb4fe72c8ed3e9d9b713c20d0bae1357d419ebf75beceda072cefc348`  
		Last Modified: Wed, 26 Oct 2022 06:29:03 GMT  
		Size: 304.3 MB (304277251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d112c7e3585a0b560df18d78d114b4535ab174294ffa0fa0592d8dc694ddaea`  
		Last Modified: Wed, 26 Oct 2022 06:28:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9181a2eac45a7f219f0e2daf10144440ffc2b1e673d892e3d82a13ecb453c3`  
		Last Modified: Wed, 26 Oct 2022 06:28:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d7c6afd6794832aac6b908431866b755a877e7f60b7e14b3f71926400a958b`  
		Last Modified: Wed, 26 Oct 2022 06:28:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b9ce9af0177ba2820a2312e843d537e6a574242f5727c1b7a5006bce66f318`  
		Last Modified: Wed, 26 Oct 2022 06:28:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:5d353ed08eb21b8d429be1c4229a2eaeeb407e6145ed673da722f9f7b724b586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:c017ef1787fd424ab33f625a1ff1747e2bfb13108c5df64f28a4332c17c8e0e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.0 MB (553983628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8743a7cf22b57ec613ae59b38065348694de4ca8569da9ed3cbae657527526`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:17:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 25 Oct 2022 04:17:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 25 Oct 2022 04:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:18:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 25 Oct 2022 04:18:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:18:54 GMT
RUN npm install -g rtlcss
# Tue, 25 Oct 2022 04:18:54 GMT
ENV ODOO_VERSION=16.0
# Wed, 26 Oct 2022 06:22:35 GMT
ARG ODOO_RELEASE=20221025
# Wed, 26 Oct 2022 06:22:35 GMT
ARG ODOO_SHA=b05756b507d2bdad65a0d76f88b0a90719ff0e44
# Wed, 26 Oct 2022 06:24:02 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=b05756b507d2bdad65a0d76f88b0a90719ff0e44
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Oct 2022 06:24:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Oct 2022 06:24:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Oct 2022 06:24:07 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=b05756b507d2bdad65a0d76f88b0a90719ff0e44
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Oct 2022 06:24:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Oct 2022 06:24:07 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Oct 2022 06:24:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Oct 2022 06:24:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Oct 2022 06:24:07 GMT
USER odoo
# Wed, 26 Oct 2022 06:24:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 06:24:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f207492967abb893017aed63de26947bc26869c41cb3ae43d047964a3f68abbe`  
		Last Modified: Tue, 25 Oct 2022 04:26:18 GMT  
		Size: 220.3 MB (220299448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034ca3be8a4120921abf777d526b8d64a15bfde37777c39a62f8c4934362a209`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 2.6 MB (2582213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260a86372800d03191e4df8077b594ccd6ea0f53bbc9f7f306cd191796d9f641`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 449.8 KB (449767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f72a8d5a48f543fe523cf8d057a54d8564b446b438d9aeb7542c12ed03aab75`  
		Last Modified: Wed, 26 Oct 2022 06:28:15 GMT  
		Size: 299.2 MB (299229699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395fa08e93880cdb3f6647af8eb2f38b23e3d387a89c3c5124ca95e85cfde1`  
		Last Modified: Wed, 26 Oct 2022 06:27:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b3b9157cce830b742cbe8417c7a52e76d1aa91caf7d73d1309270550a0272`  
		Last Modified: Wed, 26 Oct 2022 06:27:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3eb5e358cd3c87599b25c54f92ab4bc28a8eab166a2f3462d6ea685b09e871`  
		Last Modified: Wed, 26 Oct 2022 06:27:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05964d2f29fc46fb2327013d0a9fcc3abfa10cc64d5b74f3047678c226477bdf`  
		Last Modified: Wed, 26 Oct 2022 06:27:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:5d353ed08eb21b8d429be1c4229a2eaeeb407e6145ed673da722f9f7b724b586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:c017ef1787fd424ab33f625a1ff1747e2bfb13108c5df64f28a4332c17c8e0e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.0 MB (553983628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8743a7cf22b57ec613ae59b38065348694de4ca8569da9ed3cbae657527526`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:17:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 25 Oct 2022 04:17:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 25 Oct 2022 04:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:18:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 25 Oct 2022 04:18:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:18:54 GMT
RUN npm install -g rtlcss
# Tue, 25 Oct 2022 04:18:54 GMT
ENV ODOO_VERSION=16.0
# Wed, 26 Oct 2022 06:22:35 GMT
ARG ODOO_RELEASE=20221025
# Wed, 26 Oct 2022 06:22:35 GMT
ARG ODOO_SHA=b05756b507d2bdad65a0d76f88b0a90719ff0e44
# Wed, 26 Oct 2022 06:24:02 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=b05756b507d2bdad65a0d76f88b0a90719ff0e44
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Oct 2022 06:24:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Oct 2022 06:24:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Oct 2022 06:24:07 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=b05756b507d2bdad65a0d76f88b0a90719ff0e44
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Oct 2022 06:24:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Oct 2022 06:24:07 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Oct 2022 06:24:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Oct 2022 06:24:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Oct 2022 06:24:07 GMT
USER odoo
# Wed, 26 Oct 2022 06:24:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 06:24:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f207492967abb893017aed63de26947bc26869c41cb3ae43d047964a3f68abbe`  
		Last Modified: Tue, 25 Oct 2022 04:26:18 GMT  
		Size: 220.3 MB (220299448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034ca3be8a4120921abf777d526b8d64a15bfde37777c39a62f8c4934362a209`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 2.6 MB (2582213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260a86372800d03191e4df8077b594ccd6ea0f53bbc9f7f306cd191796d9f641`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 449.8 KB (449767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f72a8d5a48f543fe523cf8d057a54d8564b446b438d9aeb7542c12ed03aab75`  
		Last Modified: Wed, 26 Oct 2022 06:28:15 GMT  
		Size: 299.2 MB (299229699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395fa08e93880cdb3f6647af8eb2f38b23e3d387a89c3c5124ca95e85cfde1`  
		Last Modified: Wed, 26 Oct 2022 06:27:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b3b9157cce830b742cbe8417c7a52e76d1aa91caf7d73d1309270550a0272`  
		Last Modified: Wed, 26 Oct 2022 06:27:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3eb5e358cd3c87599b25c54f92ab4bc28a8eab166a2f3462d6ea685b09e871`  
		Last Modified: Wed, 26 Oct 2022 06:27:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05964d2f29fc46fb2327013d0a9fcc3abfa10cc64d5b74f3047678c226477bdf`  
		Last Modified: Wed, 26 Oct 2022 06:27:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:5d353ed08eb21b8d429be1c4229a2eaeeb407e6145ed673da722f9f7b724b586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:c017ef1787fd424ab33f625a1ff1747e2bfb13108c5df64f28a4332c17c8e0e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.0 MB (553983628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8743a7cf22b57ec613ae59b38065348694de4ca8569da9ed3cbae657527526`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:17:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 25 Oct 2022 04:17:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 25 Oct 2022 04:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:18:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 25 Oct 2022 04:18:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:18:54 GMT
RUN npm install -g rtlcss
# Tue, 25 Oct 2022 04:18:54 GMT
ENV ODOO_VERSION=16.0
# Wed, 26 Oct 2022 06:22:35 GMT
ARG ODOO_RELEASE=20221025
# Wed, 26 Oct 2022 06:22:35 GMT
ARG ODOO_SHA=b05756b507d2bdad65a0d76f88b0a90719ff0e44
# Wed, 26 Oct 2022 06:24:02 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=b05756b507d2bdad65a0d76f88b0a90719ff0e44
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Oct 2022 06:24:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Oct 2022 06:24:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Oct 2022 06:24:07 GMT
# ARGS: ODOO_RELEASE=20221025 ODOO_SHA=b05756b507d2bdad65a0d76f88b0a90719ff0e44
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Oct 2022 06:24:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Oct 2022 06:24:07 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Oct 2022 06:24:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Oct 2022 06:24:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Oct 2022 06:24:07 GMT
USER odoo
# Wed, 26 Oct 2022 06:24:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 06:24:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f207492967abb893017aed63de26947bc26869c41cb3ae43d047964a3f68abbe`  
		Last Modified: Tue, 25 Oct 2022 04:26:18 GMT  
		Size: 220.3 MB (220299448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034ca3be8a4120921abf777d526b8d64a15bfde37777c39a62f8c4934362a209`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 2.6 MB (2582213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260a86372800d03191e4df8077b594ccd6ea0f53bbc9f7f306cd191796d9f641`  
		Last Modified: Tue, 25 Oct 2022 04:25:51 GMT  
		Size: 449.8 KB (449767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f72a8d5a48f543fe523cf8d057a54d8564b446b438d9aeb7542c12ed03aab75`  
		Last Modified: Wed, 26 Oct 2022 06:28:15 GMT  
		Size: 299.2 MB (299229699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395fa08e93880cdb3f6647af8eb2f38b23e3d387a89c3c5124ca95e85cfde1`  
		Last Modified: Wed, 26 Oct 2022 06:27:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b3b9157cce830b742cbe8417c7a52e76d1aa91caf7d73d1309270550a0272`  
		Last Modified: Wed, 26 Oct 2022 06:27:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3eb5e358cd3c87599b25c54f92ab4bc28a8eab166a2f3462d6ea685b09e871`  
		Last Modified: Wed, 26 Oct 2022 06:27:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05964d2f29fc46fb2327013d0a9fcc3abfa10cc64d5b74f3047678c226477bdf`  
		Last Modified: Wed, 26 Oct 2022 06:27:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
