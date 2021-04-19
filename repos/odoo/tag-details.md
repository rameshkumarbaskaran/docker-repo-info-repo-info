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
$ docker pull odoo@sha256:0ebc224a9393ca2050b027e5532c44758771a258f3fc8afab1882f982fd7ba9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:ebccc19416703a6255628092b53bc537c4cbb91f836f18a04fce66501e5a3a16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542581710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9674f77ff4cde9e4bb9a8c7b5488b1aa2895a4cdbb494a03b8762dffb4c9f26c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:37:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:37:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:37:46 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:37:47 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 10 Apr 2021 12:39:11 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:39:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
ENV ODOO_VERSION=12.0
# Mon, 19 Apr 2021 19:01:47 GMT
ARG ODOO_RELEASE=20210419
# Mon, 19 Apr 2021 19:01:47 GMT
ARG ODOO_SHA=fc2da8b587cdade7a94a51cb251c5cef9ea13fe8
# Mon, 19 Apr 2021 19:02:49 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=fc2da8b587cdade7a94a51cb251c5cef9ea13fe8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 19 Apr 2021 19:02:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 19 Apr 2021 19:02:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 19 Apr 2021 19:02:53 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=fc2da8b587cdade7a94a51cb251c5cef9ea13fe8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 19 Apr 2021 19:02:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Apr 2021 19:02:53 GMT
EXPOSE 8069 8071 8072
# Mon, 19 Apr 2021 19:02:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Apr 2021 19:02:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 19 Apr 2021 19:02:54 GMT
USER odoo
# Mon, 19 Apr 2021 19:02:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Apr 2021 19:02:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf89834cbbd2b3cee3b8a944f6b45e4a1507584664ee0a1b02259590615d59`  
		Last Modified: Sat, 10 Apr 2021 12:42:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b11cee4db50450b66bc29b47f68b86380f02d6097f24e2b69a05dab9b82788`  
		Last Modified: Sat, 10 Apr 2021 12:43:18 GMT  
		Size: 219.6 MB (219645154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98555f4c9e696b99e0a4429cafe8848f74f7baa37c2265bd07bdc5d7ca50ece3`  
		Last Modified: Sat, 10 Apr 2021 12:42:52 GMT  
		Size: 2.2 MB (2224102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd66427a8f8ee5f5e15e695a9171413d51a17fd3fa05b78c6b7b8f7f2b8a259`  
		Last Modified: Sat, 10 Apr 2021 12:42:56 GMT  
		Size: 22.0 MB (22046831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04018f77395a51847550144e02f2a5f0741ff49c0a0eb3abef50dfcc37e3c640`  
		Last Modified: Mon, 19 Apr 2021 19:05:14 GMT  
		Size: 276.1 MB (276134696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647b09e40c85a29f1cd0854d39e6958ee38c8024ac3b5a0bb7245985ed888bba`  
		Last Modified: Mon, 19 Apr 2021 19:04:45 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22399413bd6eddc8ff776c2e93a80009598c960e4ac0b1a4a72887458a3054a`  
		Last Modified: Mon, 19 Apr 2021 19:04:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7607f651150bc1beed62a216171f157d8b1b75c8ea49daf75ebb594f21cb4f5`  
		Last Modified: Mon, 19 Apr 2021 19:04:45 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff91fdf953ad5154f1e92b74644cf3534e9ead7c3ce9903461c181530d4c268e`  
		Last Modified: Mon, 19 Apr 2021 19:04:45 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:0ebc224a9393ca2050b027e5532c44758771a258f3fc8afab1882f982fd7ba9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:ebccc19416703a6255628092b53bc537c4cbb91f836f18a04fce66501e5a3a16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542581710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9674f77ff4cde9e4bb9a8c7b5488b1aa2895a4cdbb494a03b8762dffb4c9f26c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:37:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:37:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:37:46 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:37:47 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 10 Apr 2021 12:39:11 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:39:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
ENV ODOO_VERSION=12.0
# Mon, 19 Apr 2021 19:01:47 GMT
ARG ODOO_RELEASE=20210419
# Mon, 19 Apr 2021 19:01:47 GMT
ARG ODOO_SHA=fc2da8b587cdade7a94a51cb251c5cef9ea13fe8
# Mon, 19 Apr 2021 19:02:49 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=fc2da8b587cdade7a94a51cb251c5cef9ea13fe8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 19 Apr 2021 19:02:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 19 Apr 2021 19:02:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 19 Apr 2021 19:02:53 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=fc2da8b587cdade7a94a51cb251c5cef9ea13fe8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 19 Apr 2021 19:02:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Apr 2021 19:02:53 GMT
EXPOSE 8069 8071 8072
# Mon, 19 Apr 2021 19:02:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Apr 2021 19:02:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 19 Apr 2021 19:02:54 GMT
USER odoo
# Mon, 19 Apr 2021 19:02:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Apr 2021 19:02:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf89834cbbd2b3cee3b8a944f6b45e4a1507584664ee0a1b02259590615d59`  
		Last Modified: Sat, 10 Apr 2021 12:42:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b11cee4db50450b66bc29b47f68b86380f02d6097f24e2b69a05dab9b82788`  
		Last Modified: Sat, 10 Apr 2021 12:43:18 GMT  
		Size: 219.6 MB (219645154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98555f4c9e696b99e0a4429cafe8848f74f7baa37c2265bd07bdc5d7ca50ece3`  
		Last Modified: Sat, 10 Apr 2021 12:42:52 GMT  
		Size: 2.2 MB (2224102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd66427a8f8ee5f5e15e695a9171413d51a17fd3fa05b78c6b7b8f7f2b8a259`  
		Last Modified: Sat, 10 Apr 2021 12:42:56 GMT  
		Size: 22.0 MB (22046831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04018f77395a51847550144e02f2a5f0741ff49c0a0eb3abef50dfcc37e3c640`  
		Last Modified: Mon, 19 Apr 2021 19:05:14 GMT  
		Size: 276.1 MB (276134696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647b09e40c85a29f1cd0854d39e6958ee38c8024ac3b5a0bb7245985ed888bba`  
		Last Modified: Mon, 19 Apr 2021 19:04:45 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22399413bd6eddc8ff776c2e93a80009598c960e4ac0b1a4a72887458a3054a`  
		Last Modified: Mon, 19 Apr 2021 19:04:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7607f651150bc1beed62a216171f157d8b1b75c8ea49daf75ebb594f21cb4f5`  
		Last Modified: Mon, 19 Apr 2021 19:04:45 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff91fdf953ad5154f1e92b74644cf3534e9ead7c3ce9903461c181530d4c268e`  
		Last Modified: Mon, 19 Apr 2021 19:04:45 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:ed8f7b440bd5b5b7b19efb639f3a3a2d733bf213e7529b7999231111b38b3f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:11dab207cee1ea475d8985180f2d79fafafefad76b6f06c98947530b581e1302
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532323409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d2f9856e016b7b84fc05594eea5145c8fec50e4d0bc89f6e7316a4423b2a09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:35:54 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:36:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:36:13 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:36:14 GMT
ENV ODOO_VERSION=13.0
# Mon, 19 Apr 2021 19:00:21 GMT
ARG ODOO_RELEASE=20210419
# Mon, 19 Apr 2021 19:00:22 GMT
ARG ODOO_SHA=ec2a29adc7fafb5e7d42a984898f20d259cd4c7a
# Mon, 19 Apr 2021 19:01:29 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ec2a29adc7fafb5e7d42a984898f20d259cd4c7a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 19 Apr 2021 19:01:33 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 19 Apr 2021 19:01:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 19 Apr 2021 19:01:34 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ec2a29adc7fafb5e7d42a984898f20d259cd4c7a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 19 Apr 2021 19:01:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Apr 2021 19:01:34 GMT
EXPOSE 8069 8071 8072
# Mon, 19 Apr 2021 19:01:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Apr 2021 19:01:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 19 Apr 2021 19:01:35 GMT
USER odoo
# Mon, 19 Apr 2021 19:01:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Apr 2021 19:01:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f81febf0e37dd17e29257f92caf652e1fead27661526fffe25491be70915d3`  
		Last Modified: Sat, 10 Apr 2021 12:42:31 GMT  
		Size: 207.1 MB (207124621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79303e39ab88305c57546603826b66e6eb084ae3937717320b18885c8f73fb60`  
		Last Modified: Sat, 10 Apr 2021 12:42:03 GMT  
		Size: 2.3 MB (2345472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185986373d8432024fd24e5a223928c83785fd54e9527e2380262b64e621206b`  
		Last Modified: Sat, 10 Apr 2021 12:42:06 GMT  
		Size: 896.8 KB (896834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4081d4db154bc3a97e3ddc24b29dcd4a8bbe98382449965ddf7d808d6d647bc1`  
		Last Modified: Mon, 19 Apr 2021 19:04:33 GMT  
		Size: 294.8 MB (294814682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa7fc7c3e23943b865a095004444ab826a4c99e3cb27c2c33f836cbb0acf9a`  
		Last Modified: Mon, 19 Apr 2021 19:04:01 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57683a3e0848868eb5cd58c3af4ad8201979ca68a738fbcad37a3653a586c007`  
		Last Modified: Mon, 19 Apr 2021 19:04:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c38f80add0078f2666ea04e04418c38c24ce02491ce20a89684a98482ae7bc`  
		Last Modified: Mon, 19 Apr 2021 19:04:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf44d736286311f725f0856fa2c00e224be15a298293d31c01da4f392f8540`  
		Last Modified: Mon, 19 Apr 2021 19:04:01 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:ed8f7b440bd5b5b7b19efb639f3a3a2d733bf213e7529b7999231111b38b3f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:11dab207cee1ea475d8985180f2d79fafafefad76b6f06c98947530b581e1302
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532323409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d2f9856e016b7b84fc05594eea5145c8fec50e4d0bc89f6e7316a4423b2a09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:35:54 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:36:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:36:13 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:36:14 GMT
ENV ODOO_VERSION=13.0
# Mon, 19 Apr 2021 19:00:21 GMT
ARG ODOO_RELEASE=20210419
# Mon, 19 Apr 2021 19:00:22 GMT
ARG ODOO_SHA=ec2a29adc7fafb5e7d42a984898f20d259cd4c7a
# Mon, 19 Apr 2021 19:01:29 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ec2a29adc7fafb5e7d42a984898f20d259cd4c7a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 19 Apr 2021 19:01:33 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 19 Apr 2021 19:01:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 19 Apr 2021 19:01:34 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ec2a29adc7fafb5e7d42a984898f20d259cd4c7a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 19 Apr 2021 19:01:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Apr 2021 19:01:34 GMT
EXPOSE 8069 8071 8072
# Mon, 19 Apr 2021 19:01:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Apr 2021 19:01:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 19 Apr 2021 19:01:35 GMT
USER odoo
# Mon, 19 Apr 2021 19:01:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Apr 2021 19:01:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f81febf0e37dd17e29257f92caf652e1fead27661526fffe25491be70915d3`  
		Last Modified: Sat, 10 Apr 2021 12:42:31 GMT  
		Size: 207.1 MB (207124621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79303e39ab88305c57546603826b66e6eb084ae3937717320b18885c8f73fb60`  
		Last Modified: Sat, 10 Apr 2021 12:42:03 GMT  
		Size: 2.3 MB (2345472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185986373d8432024fd24e5a223928c83785fd54e9527e2380262b64e621206b`  
		Last Modified: Sat, 10 Apr 2021 12:42:06 GMT  
		Size: 896.8 KB (896834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4081d4db154bc3a97e3ddc24b29dcd4a8bbe98382449965ddf7d808d6d647bc1`  
		Last Modified: Mon, 19 Apr 2021 19:04:33 GMT  
		Size: 294.8 MB (294814682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa7fc7c3e23943b865a095004444ab826a4c99e3cb27c2c33f836cbb0acf9a`  
		Last Modified: Mon, 19 Apr 2021 19:04:01 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57683a3e0848868eb5cd58c3af4ad8201979ca68a738fbcad37a3653a586c007`  
		Last Modified: Mon, 19 Apr 2021 19:04:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c38f80add0078f2666ea04e04418c38c24ce02491ce20a89684a98482ae7bc`  
		Last Modified: Mon, 19 Apr 2021 19:04:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf44d736286311f725f0856fa2c00e224be15a298293d31c01da4f392f8540`  
		Last Modified: Mon, 19 Apr 2021 19:04:01 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:f30835e99006a7144b967928ada7bb7f4b48c898e0b60d35eafc2ef1886d502c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:3843cbba595af1980893b4d2302172d31f0f4f88593f43f548c842945d853246
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.0 MB (515978544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2884da1c3ed0ab89db7337632d0e67c3458dd226ca703521d413023555d262d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Mon, 19 Apr 2021 18:58:56 GMT
ARG ODOO_RELEASE=20210419
# Mon, 19 Apr 2021 18:58:56 GMT
ARG ODOO_SHA=ae54fd63089d0c4bef5e123fdefed368a76021ab
# Mon, 19 Apr 2021 19:00:00 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ae54fd63089d0c4bef5e123fdefed368a76021ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 19 Apr 2021 19:00:04 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 19 Apr 2021 19:00:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 19 Apr 2021 19:00:05 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ae54fd63089d0c4bef5e123fdefed368a76021ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 19 Apr 2021 19:00:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Apr 2021 19:00:06 GMT
EXPOSE 8069 8071 8072
# Mon, 19 Apr 2021 19:00:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Apr 2021 19:00:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 19 Apr 2021 19:00:06 GMT
USER odoo
# Mon, 19 Apr 2021 19:00:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Apr 2021 19:00:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0f2570e4993a22ff315e68489e01aede30656d1628af600bf5aa3642e1472c`  
		Last Modified: Mon, 19 Apr 2021 19:03:43 GMT  
		Size: 272.4 MB (272421070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3090dbd4d1eea6b4885436204c2022ffd14662c68fa9de432c1bffaaa9194d`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60d0ee9b197ee51149e8209014030755edc35a1b89a28e8b6540addf8ad919d`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed42c1d048c0196a9d3b989bceae19daace6d10959dabff2d8ed6f27aa6243`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f36f958d8a3f11d26c087987b39dce1393a3eb0718a68239009bea49ea359a`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:f30835e99006a7144b967928ada7bb7f4b48c898e0b60d35eafc2ef1886d502c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:3843cbba595af1980893b4d2302172d31f0f4f88593f43f548c842945d853246
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.0 MB (515978544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2884da1c3ed0ab89db7337632d0e67c3458dd226ca703521d413023555d262d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Mon, 19 Apr 2021 18:58:56 GMT
ARG ODOO_RELEASE=20210419
# Mon, 19 Apr 2021 18:58:56 GMT
ARG ODOO_SHA=ae54fd63089d0c4bef5e123fdefed368a76021ab
# Mon, 19 Apr 2021 19:00:00 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ae54fd63089d0c4bef5e123fdefed368a76021ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 19 Apr 2021 19:00:04 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 19 Apr 2021 19:00:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 19 Apr 2021 19:00:05 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ae54fd63089d0c4bef5e123fdefed368a76021ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 19 Apr 2021 19:00:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Apr 2021 19:00:06 GMT
EXPOSE 8069 8071 8072
# Mon, 19 Apr 2021 19:00:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Apr 2021 19:00:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 19 Apr 2021 19:00:06 GMT
USER odoo
# Mon, 19 Apr 2021 19:00:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Apr 2021 19:00:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0f2570e4993a22ff315e68489e01aede30656d1628af600bf5aa3642e1472c`  
		Last Modified: Mon, 19 Apr 2021 19:03:43 GMT  
		Size: 272.4 MB (272421070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3090dbd4d1eea6b4885436204c2022ffd14662c68fa9de432c1bffaaa9194d`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60d0ee9b197ee51149e8209014030755edc35a1b89a28e8b6540addf8ad919d`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed42c1d048c0196a9d3b989bceae19daace6d10959dabff2d8ed6f27aa6243`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f36f958d8a3f11d26c087987b39dce1393a3eb0718a68239009bea49ea359a`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:f30835e99006a7144b967928ada7bb7f4b48c898e0b60d35eafc2ef1886d502c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:3843cbba595af1980893b4d2302172d31f0f4f88593f43f548c842945d853246
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.0 MB (515978544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2884da1c3ed0ab89db7337632d0e67c3458dd226ca703521d413023555d262d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Mon, 19 Apr 2021 18:58:56 GMT
ARG ODOO_RELEASE=20210419
# Mon, 19 Apr 2021 18:58:56 GMT
ARG ODOO_SHA=ae54fd63089d0c4bef5e123fdefed368a76021ab
# Mon, 19 Apr 2021 19:00:00 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ae54fd63089d0c4bef5e123fdefed368a76021ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 19 Apr 2021 19:00:04 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 19 Apr 2021 19:00:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 19 Apr 2021 19:00:05 GMT
# ARGS: ODOO_RELEASE=20210419 ODOO_SHA=ae54fd63089d0c4bef5e123fdefed368a76021ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 19 Apr 2021 19:00:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Apr 2021 19:00:06 GMT
EXPOSE 8069 8071 8072
# Mon, 19 Apr 2021 19:00:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Apr 2021 19:00:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 19 Apr 2021 19:00:06 GMT
USER odoo
# Mon, 19 Apr 2021 19:00:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Apr 2021 19:00:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0f2570e4993a22ff315e68489e01aede30656d1628af600bf5aa3642e1472c`  
		Last Modified: Mon, 19 Apr 2021 19:03:43 GMT  
		Size: 272.4 MB (272421070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3090dbd4d1eea6b4885436204c2022ffd14662c68fa9de432c1bffaaa9194d`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60d0ee9b197ee51149e8209014030755edc35a1b89a28e8b6540addf8ad919d`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed42c1d048c0196a9d3b989bceae19daace6d10959dabff2d8ed6f27aa6243`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f36f958d8a3f11d26c087987b39dce1393a3eb0718a68239009bea49ea359a`  
		Last Modified: Mon, 19 Apr 2021 19:03:11 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
