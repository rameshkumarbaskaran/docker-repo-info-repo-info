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
$ docker pull odoo@sha256:f56ae8d258a5b8273df6c5f4122b29976b625b59228a98a88e906805869ed479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:6d2b227db55cadd7ed59b6ba26ef357bdd42e27d2d8d421bc2c0cf9f310ff313
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.0 MB (541004030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4b8e58ee6c0348557426763a0e7119bde05a6d7599110b590d93598267fe63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:33:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:33:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:33:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:33:50 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Feb 2021 17:35:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:36:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:16 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:17 GMT
ENV ODOO_VERSION=12.0
# Tue, 09 Feb 2021 17:36:17 GMT
ARG ODOO_RELEASE=20210204
# Tue, 09 Feb 2021 17:36:17 GMT
ARG ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
# Tue, 09 Feb 2021 17:37:26 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Feb 2021 17:37:27 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Feb 2021 17:37:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Feb 2021 17:37:29 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Feb 2021 17:37:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Feb 2021 17:37:29 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Feb 2021 17:37:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Feb 2021 17:37:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Feb 2021 17:37:30 GMT
USER odoo
# Tue, 09 Feb 2021 17:37:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 17:37:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1cabf5609130f825def08a86940a9a06f7025505559b2c7e652b60a9e05005`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab23230155ecde52cbc43dbfe8141ef3dcbfaa6a5e242654c5ff6071e727f0a9`  
		Last Modified: Tue, 09 Feb 2021 17:41:19 GMT  
		Size: 219.6 MB (219611261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ff187134bcc9d0cf0a66450af847efce4bd9dc973a88ae485acff4a4b3df1`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 2.2 MB (2222432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5ca9709c7ca8d1819e6f5e6a2a15591eb75f5cf82ba48c2825cde329116c8`  
		Last Modified: Tue, 09 Feb 2021 17:41:01 GMT  
		Size: 22.1 MB (22055467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9820fa93cef8532ca21c5956234698eded82a5f27e3f97728ffc1e9edaa42d16`  
		Last Modified: Tue, 09 Feb 2021 17:41:37 GMT  
		Size: 274.6 MB (274583638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f54b577651331435321ab86da73f4fcf3a4cb421cff4facedf12beeeb69131`  
		Last Modified: Tue, 09 Feb 2021 17:40:41 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c62cea4c4abcb2548e3cf94d65ffe40a9351c269aa9c490be94d132abf1d91`  
		Last Modified: Tue, 09 Feb 2021 17:40:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c52ac543f67d80e539b6f23a2a96b018c23089557616505ed8f137128f7c8da`  
		Last Modified: Tue, 09 Feb 2021 17:40:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f1f96ab6eaba5490d55ccdff8fba0fa609cecb731c877d720b1f872aed362`  
		Last Modified: Tue, 09 Feb 2021 17:40:41 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:f56ae8d258a5b8273df6c5f4122b29976b625b59228a98a88e906805869ed479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:6d2b227db55cadd7ed59b6ba26ef357bdd42e27d2d8d421bc2c0cf9f310ff313
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.0 MB (541004030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4b8e58ee6c0348557426763a0e7119bde05a6d7599110b590d93598267fe63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:33:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:33:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:33:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:33:50 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Feb 2021 17:35:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:36:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:16 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:17 GMT
ENV ODOO_VERSION=12.0
# Tue, 09 Feb 2021 17:36:17 GMT
ARG ODOO_RELEASE=20210204
# Tue, 09 Feb 2021 17:36:17 GMT
ARG ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
# Tue, 09 Feb 2021 17:37:26 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Feb 2021 17:37:27 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Feb 2021 17:37:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Feb 2021 17:37:29 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Feb 2021 17:37:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Feb 2021 17:37:29 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Feb 2021 17:37:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Feb 2021 17:37:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Feb 2021 17:37:30 GMT
USER odoo
# Tue, 09 Feb 2021 17:37:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 17:37:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1cabf5609130f825def08a86940a9a06f7025505559b2c7e652b60a9e05005`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab23230155ecde52cbc43dbfe8141ef3dcbfaa6a5e242654c5ff6071e727f0a9`  
		Last Modified: Tue, 09 Feb 2021 17:41:19 GMT  
		Size: 219.6 MB (219611261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ff187134bcc9d0cf0a66450af847efce4bd9dc973a88ae485acff4a4b3df1`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 2.2 MB (2222432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5ca9709c7ca8d1819e6f5e6a2a15591eb75f5cf82ba48c2825cde329116c8`  
		Last Modified: Tue, 09 Feb 2021 17:41:01 GMT  
		Size: 22.1 MB (22055467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9820fa93cef8532ca21c5956234698eded82a5f27e3f97728ffc1e9edaa42d16`  
		Last Modified: Tue, 09 Feb 2021 17:41:37 GMT  
		Size: 274.6 MB (274583638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f54b577651331435321ab86da73f4fcf3a4cb421cff4facedf12beeeb69131`  
		Last Modified: Tue, 09 Feb 2021 17:40:41 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c62cea4c4abcb2548e3cf94d65ffe40a9351c269aa9c490be94d132abf1d91`  
		Last Modified: Tue, 09 Feb 2021 17:40:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c52ac543f67d80e539b6f23a2a96b018c23089557616505ed8f137128f7c8da`  
		Last Modified: Tue, 09 Feb 2021 17:40:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f1f96ab6eaba5490d55ccdff8fba0fa609cecb731c877d720b1f872aed362`  
		Last Modified: Tue, 09 Feb 2021 17:40:41 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:f61c5f18d780ca0769ed88c2a2821a9aaae504fd1e4a8a481ec97a9212b96d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:7bea1deae392aca4ff2ef71992594b0f7dc9504c277631a359f1ca8e517bc79f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.7 MB (530664947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a68b5510ddecee9ad9fdfc846191bfb244c528c2814784f6c4cf847508889df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:32:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:32:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:32:12 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:32:12 GMT
ENV ODOO_VERSION=13.0
# Tue, 09 Feb 2021 17:32:12 GMT
ARG ODOO_RELEASE=20210204
# Tue, 09 Feb 2021 17:32:13 GMT
ARG ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
# Tue, 09 Feb 2021 17:33:29 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Feb 2021 17:33:30 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Feb 2021 17:33:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Feb 2021 17:33:31 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Feb 2021 17:33:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Feb 2021 17:33:32 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Feb 2021 17:33:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Feb 2021 17:33:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Feb 2021 17:33:32 GMT
USER odoo
# Tue, 09 Feb 2021 17:33:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 17:33:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df63def913e7acc2a8ee5bbdb8dac5f2449993c30e7aff862b1f01f485f5f2`  
		Last Modified: Tue, 09 Feb 2021 17:40:15 GMT  
		Size: 207.1 MB (207097574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ab203da2fb5d30f709e95af58f20d98a184b7fbc9e8611a5d91717a5fbe1c9`  
		Last Modified: Tue, 09 Feb 2021 17:39:37 GMT  
		Size: 2.3 MB (2343915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16975ddc87358fae6e7b7b9c3809881bdaaf4a63f75c307a3d344c92852557f5`  
		Last Modified: Tue, 09 Feb 2021 17:39:36 GMT  
		Size: 909.0 KB (909031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573117592bb5e9829912ed59c745c3ab0dd143e1fa83e6e6910167b0f2d945f3`  
		Last Modified: Tue, 09 Feb 2021 17:40:35 GMT  
		Size: 293.2 MB (293216886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954037b0a48b6cfd30ccb6cf62ec09bd2712d1b8e72e630047855c7e9cb28c48`  
		Last Modified: Tue, 09 Feb 2021 17:39:34 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78be1208cb064422743bd6fd99641dc3508d72711e9afaadb44963abcd7505ff`  
		Last Modified: Tue, 09 Feb 2021 17:39:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9988d1be9e09723b0e37d894489f83e5df4d0dfef2f9451ed13da9577aba369`  
		Last Modified: Tue, 09 Feb 2021 17:39:34 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e844422d5708ba60165be5847f69886dea4b492682a5528ac8c0066b861e1b9c`  
		Last Modified: Tue, 09 Feb 2021 17:39:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:f61c5f18d780ca0769ed88c2a2821a9aaae504fd1e4a8a481ec97a9212b96d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:7bea1deae392aca4ff2ef71992594b0f7dc9504c277631a359f1ca8e517bc79f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.7 MB (530664947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a68b5510ddecee9ad9fdfc846191bfb244c528c2814784f6c4cf847508889df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:32:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:32:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:32:12 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:32:12 GMT
ENV ODOO_VERSION=13.0
# Tue, 09 Feb 2021 17:32:12 GMT
ARG ODOO_RELEASE=20210204
# Tue, 09 Feb 2021 17:32:13 GMT
ARG ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
# Tue, 09 Feb 2021 17:33:29 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Feb 2021 17:33:30 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Feb 2021 17:33:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Feb 2021 17:33:31 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Feb 2021 17:33:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Feb 2021 17:33:32 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Feb 2021 17:33:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Feb 2021 17:33:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Feb 2021 17:33:32 GMT
USER odoo
# Tue, 09 Feb 2021 17:33:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 17:33:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df63def913e7acc2a8ee5bbdb8dac5f2449993c30e7aff862b1f01f485f5f2`  
		Last Modified: Tue, 09 Feb 2021 17:40:15 GMT  
		Size: 207.1 MB (207097574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ab203da2fb5d30f709e95af58f20d98a184b7fbc9e8611a5d91717a5fbe1c9`  
		Last Modified: Tue, 09 Feb 2021 17:39:37 GMT  
		Size: 2.3 MB (2343915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16975ddc87358fae6e7b7b9c3809881bdaaf4a63f75c307a3d344c92852557f5`  
		Last Modified: Tue, 09 Feb 2021 17:39:36 GMT  
		Size: 909.0 KB (909031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573117592bb5e9829912ed59c745c3ab0dd143e1fa83e6e6910167b0f2d945f3`  
		Last Modified: Tue, 09 Feb 2021 17:40:35 GMT  
		Size: 293.2 MB (293216886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954037b0a48b6cfd30ccb6cf62ec09bd2712d1b8e72e630047855c7e9cb28c48`  
		Last Modified: Tue, 09 Feb 2021 17:39:34 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78be1208cb064422743bd6fd99641dc3508d72711e9afaadb44963abcd7505ff`  
		Last Modified: Tue, 09 Feb 2021 17:39:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9988d1be9e09723b0e37d894489f83e5df4d0dfef2f9451ed13da9577aba369`  
		Last Modified: Tue, 09 Feb 2021 17:39:34 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e844422d5708ba60165be5847f69886dea4b492682a5528ac8c0066b861e1b9c`  
		Last Modified: Tue, 09 Feb 2021 17:39:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:c86f1e31a2184f1205ac947784d54d8fe1bce5bcefa574a62cb555b71a19c46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:ddebf5d6687839331b56d9c64cf2831429c65cd41b373df452d6824f0ebacccb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.0 MB (511001151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c0a83777bd828e3a8f8360a9ab2e8c9693a9283ef5c7b0dc299f01d9c2d3e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Tue, 09 Feb 2021 17:29:18 GMT
ARG ODOO_RELEASE=20210204
# Tue, 09 Feb 2021 17:29:18 GMT
ARG ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
# Tue, 09 Feb 2021 17:30:33 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Feb 2021 17:30:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Feb 2021 17:30:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Feb 2021 17:30:36 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Feb 2021 17:30:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Feb 2021 17:30:37 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Feb 2021 17:30:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Feb 2021 17:30:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Feb 2021 17:30:37 GMT
USER odoo
# Tue, 09 Feb 2021 17:30:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 17:30:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a898f2782afa8cd348b59eb601a7fa0faa1e3d5daa392229041f7d234ad2f0a7`  
		Last Modified: Tue, 09 Feb 2021 17:39:28 GMT  
		Size: 267.5 MB (267496192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a0f63469096ef47e3badda0d84ef75e0a0ef3d8b455632d8354e897710e611`  
		Last Modified: Tue, 09 Feb 2021 17:37:46 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6838bd2119731862abf2af94c7bf146ed0072afa39430ada8ce7be4faa137a6f`  
		Last Modified: Tue, 09 Feb 2021 17:37:47 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4dbeb6ebb72bf5688199c8afb052f2401416936eb822375b7ecd720dd891b3`  
		Last Modified: Tue, 09 Feb 2021 17:37:47 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bad7ef1e443313127014c6a07a7d040e08518d264e0c010191991b67774cc8`  
		Last Modified: Tue, 09 Feb 2021 17:37:46 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:c86f1e31a2184f1205ac947784d54d8fe1bce5bcefa574a62cb555b71a19c46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:ddebf5d6687839331b56d9c64cf2831429c65cd41b373df452d6824f0ebacccb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.0 MB (511001151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c0a83777bd828e3a8f8360a9ab2e8c9693a9283ef5c7b0dc299f01d9c2d3e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Tue, 09 Feb 2021 17:29:18 GMT
ARG ODOO_RELEASE=20210204
# Tue, 09 Feb 2021 17:29:18 GMT
ARG ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
# Tue, 09 Feb 2021 17:30:33 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Feb 2021 17:30:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Feb 2021 17:30:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Feb 2021 17:30:36 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Feb 2021 17:30:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Feb 2021 17:30:37 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Feb 2021 17:30:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Feb 2021 17:30:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Feb 2021 17:30:37 GMT
USER odoo
# Tue, 09 Feb 2021 17:30:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 17:30:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a898f2782afa8cd348b59eb601a7fa0faa1e3d5daa392229041f7d234ad2f0a7`  
		Last Modified: Tue, 09 Feb 2021 17:39:28 GMT  
		Size: 267.5 MB (267496192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a0f63469096ef47e3badda0d84ef75e0a0ef3d8b455632d8354e897710e611`  
		Last Modified: Tue, 09 Feb 2021 17:37:46 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6838bd2119731862abf2af94c7bf146ed0072afa39430ada8ce7be4faa137a6f`  
		Last Modified: Tue, 09 Feb 2021 17:37:47 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4dbeb6ebb72bf5688199c8afb052f2401416936eb822375b7ecd720dd891b3`  
		Last Modified: Tue, 09 Feb 2021 17:37:47 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bad7ef1e443313127014c6a07a7d040e08518d264e0c010191991b67774cc8`  
		Last Modified: Tue, 09 Feb 2021 17:37:46 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:c86f1e31a2184f1205ac947784d54d8fe1bce5bcefa574a62cb555b71a19c46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:ddebf5d6687839331b56d9c64cf2831429c65cd41b373df452d6824f0ebacccb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.0 MB (511001151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c0a83777bd828e3a8f8360a9ab2e8c9693a9283ef5c7b0dc299f01d9c2d3e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Tue, 09 Feb 2021 17:29:18 GMT
ARG ODOO_RELEASE=20210204
# Tue, 09 Feb 2021 17:29:18 GMT
ARG ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
# Tue, 09 Feb 2021 17:30:33 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Feb 2021 17:30:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Feb 2021 17:30:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Feb 2021 17:30:36 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Feb 2021 17:30:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Feb 2021 17:30:37 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Feb 2021 17:30:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Feb 2021 17:30:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Feb 2021 17:30:37 GMT
USER odoo
# Tue, 09 Feb 2021 17:30:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 17:30:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a898f2782afa8cd348b59eb601a7fa0faa1e3d5daa392229041f7d234ad2f0a7`  
		Last Modified: Tue, 09 Feb 2021 17:39:28 GMT  
		Size: 267.5 MB (267496192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a0f63469096ef47e3badda0d84ef75e0a0ef3d8b455632d8354e897710e611`  
		Last Modified: Tue, 09 Feb 2021 17:37:46 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6838bd2119731862abf2af94c7bf146ed0072afa39430ada8ce7be4faa137a6f`  
		Last Modified: Tue, 09 Feb 2021 17:37:47 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4dbeb6ebb72bf5688199c8afb052f2401416936eb822375b7ecd720dd891b3`  
		Last Modified: Tue, 09 Feb 2021 17:37:47 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bad7ef1e443313127014c6a07a7d040e08518d264e0c010191991b67774cc8`  
		Last Modified: Tue, 09 Feb 2021 17:37:46 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
