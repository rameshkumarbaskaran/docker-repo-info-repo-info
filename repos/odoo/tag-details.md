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
$ docker pull odoo@sha256:3c0b65cd9f630ce79c8e8088b6ca46a6dda0ed9ffaec48dba12ebef9567484f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:708d4e1cf59b91d1438ffed2e91a58d957a95ba453c90fb99d798784d766bc19
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396633727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e54fae6cce1b0d5e0b2fe3a38fe8278e14865b017757cb0c4d76ebfae01a1f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:52:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:52:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:52:34 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 12:52:36 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 10 Sep 2020 12:54:27 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 10 Sep 2020 12:54:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:54:50 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:54:51 GMT
ENV ODOO_VERSION=12.0
# Fri, 02 Oct 2020 21:43:12 GMT
ARG ODOO_RELEASE=20201002
# Fri, 02 Oct 2020 21:43:13 GMT
ARG ODOO_SHA=c0412c5a5e45d010aed165107d513b4e6e1b2f5f
# Fri, 02 Oct 2020 21:44:14 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=c0412c5a5e45d010aed165107d513b4e6e1b2f5f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Oct 2020 21:44:16 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 02 Oct 2020 21:44:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Oct 2020 21:44:18 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=c0412c5a5e45d010aed165107d513b4e6e1b2f5f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Oct 2020 21:44:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Oct 2020 21:44:18 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Oct 2020 21:44:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Oct 2020 21:44:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Oct 2020 21:44:20 GMT
USER odoo
# Fri, 02 Oct 2020 21:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 21:44:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56086b9aed3618fa49ce55fed84ad357d06f45b40509bd912a7952de116fa05b`  
		Last Modified: Thu, 10 Sep 2020 12:57:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460ce2e8a64c8ca25c6101e91b65de99f96d69bd737b6595c8f0ff7029bcdb54`  
		Last Modified: Thu, 10 Sep 2020 12:58:47 GMT  
		Size: 219.6 MB (219609382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0257fe8743d13038cee80f5a656715c65086b5b0ce8e2a87f75f4293cd01b3`  
		Last Modified: Thu, 10 Sep 2020 12:57:58 GMT  
		Size: 2.3 MB (2337725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4793f99106c9a03175078660d27f4a87519096c2bdf5b4158f02ca27111b5c4`  
		Last Modified: Thu, 10 Sep 2020 12:58:16 GMT  
		Size: 22.3 MB (22256625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf929d93b79fb67daf176d0de1cf031bec1a57626d586769f17855a405b89c8`  
		Last Modified: Fri, 02 Oct 2020 21:47:23 GMT  
		Size: 129.9 MB (129905088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f2797c818ae603a3917c616626719b06b7884bb4e8093e51b3c43be5dc3ea6`  
		Last Modified: Fri, 02 Oct 2020 21:46:45 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b88157b6e75aed262aa9e38dcbdeeaf22ce47cb2f1f293c95d89c4f66ca8101`  
		Last Modified: Fri, 02 Oct 2020 21:46:45 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b31428f25ea74fabe98190d719253593a212b45a0c9f7c99dd6fb0051637b`  
		Last Modified: Fri, 02 Oct 2020 21:46:44 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed7dec9a74da8c4bb9a385ee28896c7ffca9f7c3b6349920409dc7b35b135eb`  
		Last Modified: Fri, 02 Oct 2020 21:46:44 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:3c0b65cd9f630ce79c8e8088b6ca46a6dda0ed9ffaec48dba12ebef9567484f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:708d4e1cf59b91d1438ffed2e91a58d957a95ba453c90fb99d798784d766bc19
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396633727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e54fae6cce1b0d5e0b2fe3a38fe8278e14865b017757cb0c4d76ebfae01a1f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:52:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:52:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:52:34 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 12:52:36 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 10 Sep 2020 12:54:27 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 10 Sep 2020 12:54:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:54:50 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:54:51 GMT
ENV ODOO_VERSION=12.0
# Fri, 02 Oct 2020 21:43:12 GMT
ARG ODOO_RELEASE=20201002
# Fri, 02 Oct 2020 21:43:13 GMT
ARG ODOO_SHA=c0412c5a5e45d010aed165107d513b4e6e1b2f5f
# Fri, 02 Oct 2020 21:44:14 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=c0412c5a5e45d010aed165107d513b4e6e1b2f5f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Oct 2020 21:44:16 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 02 Oct 2020 21:44:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Oct 2020 21:44:18 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=c0412c5a5e45d010aed165107d513b4e6e1b2f5f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Oct 2020 21:44:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Oct 2020 21:44:18 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Oct 2020 21:44:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Oct 2020 21:44:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Oct 2020 21:44:20 GMT
USER odoo
# Fri, 02 Oct 2020 21:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 21:44:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56086b9aed3618fa49ce55fed84ad357d06f45b40509bd912a7952de116fa05b`  
		Last Modified: Thu, 10 Sep 2020 12:57:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460ce2e8a64c8ca25c6101e91b65de99f96d69bd737b6595c8f0ff7029bcdb54`  
		Last Modified: Thu, 10 Sep 2020 12:58:47 GMT  
		Size: 219.6 MB (219609382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0257fe8743d13038cee80f5a656715c65086b5b0ce8e2a87f75f4293cd01b3`  
		Last Modified: Thu, 10 Sep 2020 12:57:58 GMT  
		Size: 2.3 MB (2337725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4793f99106c9a03175078660d27f4a87519096c2bdf5b4158f02ca27111b5c4`  
		Last Modified: Thu, 10 Sep 2020 12:58:16 GMT  
		Size: 22.3 MB (22256625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf929d93b79fb67daf176d0de1cf031bec1a57626d586769f17855a405b89c8`  
		Last Modified: Fri, 02 Oct 2020 21:47:23 GMT  
		Size: 129.9 MB (129905088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f2797c818ae603a3917c616626719b06b7884bb4e8093e51b3c43be5dc3ea6`  
		Last Modified: Fri, 02 Oct 2020 21:46:45 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b88157b6e75aed262aa9e38dcbdeeaf22ce47cb2f1f293c95d89c4f66ca8101`  
		Last Modified: Fri, 02 Oct 2020 21:46:45 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b31428f25ea74fabe98190d719253593a212b45a0c9f7c99dd6fb0051637b`  
		Last Modified: Fri, 02 Oct 2020 21:46:44 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed7dec9a74da8c4bb9a385ee28896c7ffca9f7c3b6349920409dc7b35b135eb`  
		Last Modified: Fri, 02 Oct 2020 21:46:44 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:2b73cce7069b120558fdea8f16c4f507a01215cccd45fa071445b567335c9d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:c4bb4edef83475cf271f8841b3fa28201d2301b1de55af6cee9407e55734f963
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.7 MB (382732057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6819cd414a384a8ffa3bfb78f4094fecf397dfb4bd5d1860fbcaad92a433fc11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:49:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:49:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:49:31 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 12:50:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 10 Sep 2020 12:50:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:50:59 GMT
RUN npm install -g rtlcss
# Thu, 10 Sep 2020 12:50:59 GMT
ENV ODOO_VERSION=13.0
# Fri, 02 Oct 2020 21:41:11 GMT
ARG ODOO_RELEASE=20201002
# Fri, 02 Oct 2020 21:41:11 GMT
ARG ODOO_SHA=4df562a3f643c42e90c4c648128dafd98d73f887
# Fri, 02 Oct 2020 21:42:46 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=4df562a3f643c42e90c4c648128dafd98d73f887
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Oct 2020 21:42:48 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 02 Oct 2020 21:42:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Oct 2020 21:42:50 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=4df562a3f643c42e90c4c648128dafd98d73f887
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Oct 2020 21:42:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Oct 2020 21:42:51 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Oct 2020 21:42:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Oct 2020 21:42:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Oct 2020 21:42:52 GMT
USER odoo
# Fri, 02 Oct 2020 21:42:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 21:42:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c2c464f6195f22f9d5287694068d70f208f664cebd88823a71779448bcbfa9`  
		Last Modified: Thu, 10 Sep 2020 12:57:41 GMT  
		Size: 204.1 MB (204054893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaa85eb54a1a8603e92f874b58a604507cbfe1eab02040736f9c4ff171bfe82`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 2.3 MB (2337739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe33153083cfe1763194a3e50a1d17c86450dd6cd294c5138327a733ded54a`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 1.1 MB (1100454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9d9fe484e295e7b4a43fea9ddc24de93537b9c7031cf296760a684455c0688`  
		Last Modified: Fri, 02 Oct 2020 21:46:38 GMT  
		Size: 148.1 MB (148144401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50b1a90b59199f0f8a3eaa95c685e446fcadfca66bc2c541d1ea3141a485cb`  
		Last Modified: Fri, 02 Oct 2020 21:45:47 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9462af57f87d691b3b6911747602ed8a9b40305d28f082c559f7118ef84aea`  
		Last Modified: Fri, 02 Oct 2020 21:45:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a574dc5ee1d544c6f3eb43156984dc970956aeaa905671733ffe5fad2d030e6`  
		Last Modified: Fri, 02 Oct 2020 21:45:47 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479038d5dd6e99b529aca17ae1690b4b21ae07ce36dc578ca5234493297f2671`  
		Last Modified: Fri, 02 Oct 2020 21:45:48 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:2b73cce7069b120558fdea8f16c4f507a01215cccd45fa071445b567335c9d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:c4bb4edef83475cf271f8841b3fa28201d2301b1de55af6cee9407e55734f963
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.7 MB (382732057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6819cd414a384a8ffa3bfb78f4094fecf397dfb4bd5d1860fbcaad92a433fc11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:49:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:49:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:49:31 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 12:50:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 10 Sep 2020 12:50:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:50:59 GMT
RUN npm install -g rtlcss
# Thu, 10 Sep 2020 12:50:59 GMT
ENV ODOO_VERSION=13.0
# Fri, 02 Oct 2020 21:41:11 GMT
ARG ODOO_RELEASE=20201002
# Fri, 02 Oct 2020 21:41:11 GMT
ARG ODOO_SHA=4df562a3f643c42e90c4c648128dafd98d73f887
# Fri, 02 Oct 2020 21:42:46 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=4df562a3f643c42e90c4c648128dafd98d73f887
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Oct 2020 21:42:48 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 02 Oct 2020 21:42:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Oct 2020 21:42:50 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=4df562a3f643c42e90c4c648128dafd98d73f887
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Oct 2020 21:42:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Oct 2020 21:42:51 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Oct 2020 21:42:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Oct 2020 21:42:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Oct 2020 21:42:52 GMT
USER odoo
# Fri, 02 Oct 2020 21:42:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 21:42:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c2c464f6195f22f9d5287694068d70f208f664cebd88823a71779448bcbfa9`  
		Last Modified: Thu, 10 Sep 2020 12:57:41 GMT  
		Size: 204.1 MB (204054893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaa85eb54a1a8603e92f874b58a604507cbfe1eab02040736f9c4ff171bfe82`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 2.3 MB (2337739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe33153083cfe1763194a3e50a1d17c86450dd6cd294c5138327a733ded54a`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 1.1 MB (1100454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9d9fe484e295e7b4a43fea9ddc24de93537b9c7031cf296760a684455c0688`  
		Last Modified: Fri, 02 Oct 2020 21:46:38 GMT  
		Size: 148.1 MB (148144401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50b1a90b59199f0f8a3eaa95c685e446fcadfca66bc2c541d1ea3141a485cb`  
		Last Modified: Fri, 02 Oct 2020 21:45:47 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9462af57f87d691b3b6911747602ed8a9b40305d28f082c559f7118ef84aea`  
		Last Modified: Fri, 02 Oct 2020 21:45:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a574dc5ee1d544c6f3eb43156984dc970956aeaa905671733ffe5fad2d030e6`  
		Last Modified: Fri, 02 Oct 2020 21:45:47 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479038d5dd6e99b529aca17ae1690b4b21ae07ce36dc578ca5234493297f2671`  
		Last Modified: Fri, 02 Oct 2020 21:45:48 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:fccc13945d62704dde11bf91d232acd360c85d2e4268f6ee26d0b4eedf20ffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:6f4a949423210174856cfdf998ad18732300bf093c4b8484b1b4edcc9fbc67da
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389168484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c5f844039b4f7950d2cb02f75e6547c9eff4fcb960943db4fb6a0e852fd491`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:49:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:49:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:49:31 GMT
ENV LANG=C.UTF-8
# Fri, 02 Oct 2020 21:39:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb     && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Oct 2020 21:39:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Oct 2020 21:39:28 GMT
RUN npm install -g rtlcss
# Fri, 02 Oct 2020 21:39:28 GMT
ENV ODOO_VERSION=14.0
# Fri, 02 Oct 2020 21:39:28 GMT
ARG ODOO_RELEASE=20201002
# Fri, 02 Oct 2020 21:39:28 GMT
ARG ODOO_SHA=70917e1db8d100c791f31afbfcd782dd026bd4c9
# Fri, 02 Oct 2020 21:40:47 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=70917e1db8d100c791f31afbfcd782dd026bd4c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Oct 2020 21:40:49 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 02 Oct 2020 21:40:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Oct 2020 21:40:51 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=70917e1db8d100c791f31afbfcd782dd026bd4c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Oct 2020 21:40:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Oct 2020 21:40:52 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Oct 2020 21:40:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Oct 2020 21:40:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Oct 2020 21:40:53 GMT
USER odoo
# Fri, 02 Oct 2020 21:40:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 21:40:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918cd4aaeb69f3c828531962c0a4f69cbab65f3d22c4289db77087aa80581735`  
		Last Modified: Fri, 02 Oct 2020 21:45:39 GMT  
		Size: 210.1 MB (210103756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fcced63569e31089b82f73fbfea1199b4041d35b97dfc63c59a8d5c8e631b`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 2.4 MB (2435828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955db14828467740f3a3a069d5a2cb95a3823644a018c5b5aa1fd49ae7fcdb7d`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 1.1 MB (1111094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017e349353bc459654a1cce76c0a565f41da6297e7edf13b64a4486cb7203347`  
		Last Modified: Fri, 02 Oct 2020 21:45:41 GMT  
		Size: 148.4 MB (148423239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d71f13db1c6ca72d807ffcd7b71d22513c65606d17a6df7dc78b40e2ae76ae5`  
		Last Modified: Fri, 02 Oct 2020 21:44:36 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d377fe6745e0cdfeaac46b0acb9b3a4baaba914eaaaa8804dfd11bbf6bb515`  
		Last Modified: Fri, 02 Oct 2020 21:44:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16781d5c37efcef4bf1c88b72722d53790b91cffb3f0e74fab79f6643abb2c4`  
		Last Modified: Fri, 02 Oct 2020 21:44:37 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b885b58a509716736b769d8717a56e63196dacad2793e3a9fc80265b1546ab`  
		Last Modified: Fri, 02 Oct 2020 21:44:37 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:fccc13945d62704dde11bf91d232acd360c85d2e4268f6ee26d0b4eedf20ffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:6f4a949423210174856cfdf998ad18732300bf093c4b8484b1b4edcc9fbc67da
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389168484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c5f844039b4f7950d2cb02f75e6547c9eff4fcb960943db4fb6a0e852fd491`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:49:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:49:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:49:31 GMT
ENV LANG=C.UTF-8
# Fri, 02 Oct 2020 21:39:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb     && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Oct 2020 21:39:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Oct 2020 21:39:28 GMT
RUN npm install -g rtlcss
# Fri, 02 Oct 2020 21:39:28 GMT
ENV ODOO_VERSION=14.0
# Fri, 02 Oct 2020 21:39:28 GMT
ARG ODOO_RELEASE=20201002
# Fri, 02 Oct 2020 21:39:28 GMT
ARG ODOO_SHA=70917e1db8d100c791f31afbfcd782dd026bd4c9
# Fri, 02 Oct 2020 21:40:47 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=70917e1db8d100c791f31afbfcd782dd026bd4c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Oct 2020 21:40:49 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 02 Oct 2020 21:40:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Oct 2020 21:40:51 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=70917e1db8d100c791f31afbfcd782dd026bd4c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Oct 2020 21:40:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Oct 2020 21:40:52 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Oct 2020 21:40:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Oct 2020 21:40:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Oct 2020 21:40:53 GMT
USER odoo
# Fri, 02 Oct 2020 21:40:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 21:40:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918cd4aaeb69f3c828531962c0a4f69cbab65f3d22c4289db77087aa80581735`  
		Last Modified: Fri, 02 Oct 2020 21:45:39 GMT  
		Size: 210.1 MB (210103756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fcced63569e31089b82f73fbfea1199b4041d35b97dfc63c59a8d5c8e631b`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 2.4 MB (2435828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955db14828467740f3a3a069d5a2cb95a3823644a018c5b5aa1fd49ae7fcdb7d`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 1.1 MB (1111094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017e349353bc459654a1cce76c0a565f41da6297e7edf13b64a4486cb7203347`  
		Last Modified: Fri, 02 Oct 2020 21:45:41 GMT  
		Size: 148.4 MB (148423239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d71f13db1c6ca72d807ffcd7b71d22513c65606d17a6df7dc78b40e2ae76ae5`  
		Last Modified: Fri, 02 Oct 2020 21:44:36 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d377fe6745e0cdfeaac46b0acb9b3a4baaba914eaaaa8804dfd11bbf6bb515`  
		Last Modified: Fri, 02 Oct 2020 21:44:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16781d5c37efcef4bf1c88b72722d53790b91cffb3f0e74fab79f6643abb2c4`  
		Last Modified: Fri, 02 Oct 2020 21:44:37 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b885b58a509716736b769d8717a56e63196dacad2793e3a9fc80265b1546ab`  
		Last Modified: Fri, 02 Oct 2020 21:44:37 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:fccc13945d62704dde11bf91d232acd360c85d2e4268f6ee26d0b4eedf20ffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:6f4a949423210174856cfdf998ad18732300bf093c4b8484b1b4edcc9fbc67da
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389168484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c5f844039b4f7950d2cb02f75e6547c9eff4fcb960943db4fb6a0e852fd491`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:49:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:49:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:49:31 GMT
ENV LANG=C.UTF-8
# Fri, 02 Oct 2020 21:39:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb     && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Oct 2020 21:39:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Oct 2020 21:39:28 GMT
RUN npm install -g rtlcss
# Fri, 02 Oct 2020 21:39:28 GMT
ENV ODOO_VERSION=14.0
# Fri, 02 Oct 2020 21:39:28 GMT
ARG ODOO_RELEASE=20201002
# Fri, 02 Oct 2020 21:39:28 GMT
ARG ODOO_SHA=70917e1db8d100c791f31afbfcd782dd026bd4c9
# Fri, 02 Oct 2020 21:40:47 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=70917e1db8d100c791f31afbfcd782dd026bd4c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Oct 2020 21:40:49 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 02 Oct 2020 21:40:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Oct 2020 21:40:51 GMT
# ARGS: ODOO_RELEASE=20201002 ODOO_SHA=70917e1db8d100c791f31afbfcd782dd026bd4c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Oct 2020 21:40:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Oct 2020 21:40:52 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Oct 2020 21:40:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Oct 2020 21:40:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Oct 2020 21:40:53 GMT
USER odoo
# Fri, 02 Oct 2020 21:40:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Oct 2020 21:40:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918cd4aaeb69f3c828531962c0a4f69cbab65f3d22c4289db77087aa80581735`  
		Last Modified: Fri, 02 Oct 2020 21:45:39 GMT  
		Size: 210.1 MB (210103756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fcced63569e31089b82f73fbfea1199b4041d35b97dfc63c59a8d5c8e631b`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 2.4 MB (2435828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955db14828467740f3a3a069d5a2cb95a3823644a018c5b5aa1fd49ae7fcdb7d`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 1.1 MB (1111094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017e349353bc459654a1cce76c0a565f41da6297e7edf13b64a4486cb7203347`  
		Last Modified: Fri, 02 Oct 2020 21:45:41 GMT  
		Size: 148.4 MB (148423239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d71f13db1c6ca72d807ffcd7b71d22513c65606d17a6df7dc78b40e2ae76ae5`  
		Last Modified: Fri, 02 Oct 2020 21:44:36 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d377fe6745e0cdfeaac46b0acb9b3a4baaba914eaaaa8804dfd11bbf6bb515`  
		Last Modified: Fri, 02 Oct 2020 21:44:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16781d5c37efcef4bf1c88b72722d53790b91cffb3f0e74fab79f6643abb2c4`  
		Last Modified: Fri, 02 Oct 2020 21:44:37 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b885b58a509716736b769d8717a56e63196dacad2793e3a9fc80265b1546ab`  
		Last Modified: Fri, 02 Oct 2020 21:44:37 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
