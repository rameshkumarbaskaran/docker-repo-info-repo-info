<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:11`](#odoo11)
-	[`odoo:11.0`](#odoo110)
-	[`odoo:12`](#odoo12)
-	[`odoo:12.0`](#odoo120)
-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:latest`](#odoolatest)

## `odoo:11`

```console
$ docker pull odoo@sha256:7bdc7d1f60e6506b5c0bd771b0006c284e06f59ea5aee32a7a2aceec7ccea36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11` - linux; amd64

```console
$ docker pull odoo@sha256:07a0ad52af6f8280c4e3bd417b49a517c4d948e585ac92686652ceeed010e9ee
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.0 MB (384967593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b203480baf96a2298d952af4a303e1a40d6e53ff9a56ddd21a470f703f2d8165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:31:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 Dec 2019 20:31:52 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 20:31:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 28 Dec 2019 20:33:43 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-vobject             python3-watchdog             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 Dec 2019 20:33:53 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:35:52 GMT
ENV ODOO_VERSION=11.0
# Sat, 28 Dec 2019 20:35:52 GMT
ARG ODOO_RELEASE=20191106
# Sat, 28 Dec 2019 20:35:52 GMT
ARG ODOO_SHA=d6da6c631fb9926c4440f2016d623c37fa38d4ea
# Sat, 28 Dec 2019 20:36:41 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=d6da6c631fb9926c4440f2016d623c37fa38d4ea
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 Dec 2019 20:36:42 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Sat, 28 Dec 2019 20:36:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 Dec 2019 20:36:43 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=d6da6c631fb9926c4440f2016d623c37fa38d4ea
RUN chown odoo /etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:36:44 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=d6da6c631fb9926c4440f2016d623c37fa38d4ea
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Sat, 28 Dec 2019 20:36:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 Dec 2019 20:36:44 GMT
EXPOSE 8069 8071
# Sat, 28 Dec 2019 20:36:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:36:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 Dec 2019 20:36:45 GMT
USER odoo
# Sat, 28 Dec 2019 20:36:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 20:36:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb235ca4180b231aa378f7d9ea5ef403d0756a990ec133fabb5f212ac0f34f`  
		Last Modified: Sat, 28 Dec 2019 20:37:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b51234177bc6b7277430cb5472a8d9425e04724da9fe9deba285a1ecd11816`  
		Last Modified: Sat, 28 Dec 2019 20:38:32 GMT  
		Size: 219.1 MB (219146537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91e4ed0acf4dd4d40899c29df92c1ac4cdd0bc11e7ce90be6f281861261bbe`  
		Last Modified: Sat, 28 Dec 2019 20:37:55 GMT  
		Size: 2.2 MB (2244396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc959fd3d329215291a8a261d9e85ce8c12a5849c68295866b71d8c08847040`  
		Last Modified: Sat, 28 Dec 2019 20:39:20 GMT  
		Size: 141.0 MB (141049328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94876142e668f22e8bd61a81c2334f87969dbf1359e38b150c1f9a9f21c466de`  
		Last Modified: Sat, 28 Dec 2019 20:38:41 GMT  
		Size: 674.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9be2950a4313bbe8d64cf0f9eaa01006e02e0da6fe336910bca39682244934f`  
		Last Modified: Sat, 28 Dec 2019 20:38:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a413a514d3bfbcbd7ea7f34f9ba0135aeecf324f3d5008e5884d56c57398e6f5`  
		Last Modified: Sat, 28 Dec 2019 20:38:41 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493963ad5e0a9d339788dc168c2c48a2a23faafec5c36489175fc40ce7489d25`  
		Last Modified: Sat, 28 Dec 2019 20:38:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98547b38d5756029e79cf8f9869590791c2d78e5fc78878462d17ed13a0128a7`  
		Last Modified: Sat, 28 Dec 2019 20:38:41 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11.0`

```console
$ docker pull odoo@sha256:7bdc7d1f60e6506b5c0bd771b0006c284e06f59ea5aee32a7a2aceec7ccea36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11.0` - linux; amd64

```console
$ docker pull odoo@sha256:07a0ad52af6f8280c4e3bd417b49a517c4d948e585ac92686652ceeed010e9ee
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.0 MB (384967593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b203480baf96a2298d952af4a303e1a40d6e53ff9a56ddd21a470f703f2d8165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:31:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 Dec 2019 20:31:52 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 20:31:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 28 Dec 2019 20:33:43 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-vobject             python3-watchdog             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 Dec 2019 20:33:53 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:35:52 GMT
ENV ODOO_VERSION=11.0
# Sat, 28 Dec 2019 20:35:52 GMT
ARG ODOO_RELEASE=20191106
# Sat, 28 Dec 2019 20:35:52 GMT
ARG ODOO_SHA=d6da6c631fb9926c4440f2016d623c37fa38d4ea
# Sat, 28 Dec 2019 20:36:41 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=d6da6c631fb9926c4440f2016d623c37fa38d4ea
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 Dec 2019 20:36:42 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Sat, 28 Dec 2019 20:36:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 Dec 2019 20:36:43 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=d6da6c631fb9926c4440f2016d623c37fa38d4ea
RUN chown odoo /etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:36:44 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=d6da6c631fb9926c4440f2016d623c37fa38d4ea
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Sat, 28 Dec 2019 20:36:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 Dec 2019 20:36:44 GMT
EXPOSE 8069 8071
# Sat, 28 Dec 2019 20:36:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:36:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 Dec 2019 20:36:45 GMT
USER odoo
# Sat, 28 Dec 2019 20:36:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 20:36:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb235ca4180b231aa378f7d9ea5ef403d0756a990ec133fabb5f212ac0f34f`  
		Last Modified: Sat, 28 Dec 2019 20:37:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b51234177bc6b7277430cb5472a8d9425e04724da9fe9deba285a1ecd11816`  
		Last Modified: Sat, 28 Dec 2019 20:38:32 GMT  
		Size: 219.1 MB (219146537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91e4ed0acf4dd4d40899c29df92c1ac4cdd0bc11e7ce90be6f281861261bbe`  
		Last Modified: Sat, 28 Dec 2019 20:37:55 GMT  
		Size: 2.2 MB (2244396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc959fd3d329215291a8a261d9e85ce8c12a5849c68295866b71d8c08847040`  
		Last Modified: Sat, 28 Dec 2019 20:39:20 GMT  
		Size: 141.0 MB (141049328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94876142e668f22e8bd61a81c2334f87969dbf1359e38b150c1f9a9f21c466de`  
		Last Modified: Sat, 28 Dec 2019 20:38:41 GMT  
		Size: 674.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9be2950a4313bbe8d64cf0f9eaa01006e02e0da6fe336910bca39682244934f`  
		Last Modified: Sat, 28 Dec 2019 20:38:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a413a514d3bfbcbd7ea7f34f9ba0135aeecf324f3d5008e5884d56c57398e6f5`  
		Last Modified: Sat, 28 Dec 2019 20:38:41 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493963ad5e0a9d339788dc168c2c48a2a23faafec5c36489175fc40ce7489d25`  
		Last Modified: Sat, 28 Dec 2019 20:38:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98547b38d5756029e79cf8f9869590791c2d78e5fc78878462d17ed13a0128a7`  
		Last Modified: Sat, 28 Dec 2019 20:38:41 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12`

```console
$ docker pull odoo@sha256:ca2fd0c88b0065c719c60f95037a68d38cc57bf7795f43b7e7d84a2a23f6ef62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:28ee3e13cd403f0e35af460d6070521b0fb6c00161c7fd64a05d670e497c41da
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.1 MB (399121221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1eec67b651e18c673b89c745b29969cae203688e220aaf0cda44413da59dec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:31:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 Dec 2019 20:31:52 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 20:31:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 28 Dec 2019 20:33:43 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-vobject             python3-watchdog             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 Dec 2019 20:33:53 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:34:19 GMT
RUN set -x;    echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && export GNUPGHOME="$(mktemp -d)"     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:34:20 GMT
ENV ODOO_VERSION=12.0
# Sat, 28 Dec 2019 20:34:20 GMT
ARG ODOO_RELEASE=20191106
# Sat, 28 Dec 2019 20:34:20 GMT
ARG ODOO_SHA=8dd3d36bd371b1eb6fbeb9ff7b049c8aea84327c
# Sat, 28 Dec 2019 20:35:36 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=8dd3d36bd371b1eb6fbeb9ff7b049c8aea84327c
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 Dec 2019 20:35:37 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 28 Dec 2019 20:35:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 Dec 2019 20:35:38 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=8dd3d36bd371b1eb6fbeb9ff7b049c8aea84327c
RUN chown odoo /etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:35:39 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=8dd3d36bd371b1eb6fbeb9ff7b049c8aea84327c
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Sat, 28 Dec 2019 20:35:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 Dec 2019 20:35:39 GMT
EXPOSE 8069 8071
# Sat, 28 Dec 2019 20:35:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:35:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 Dec 2019 20:35:40 GMT
USER odoo
# Sat, 28 Dec 2019 20:35:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 20:35:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb235ca4180b231aa378f7d9ea5ef403d0756a990ec133fabb5f212ac0f34f`  
		Last Modified: Sat, 28 Dec 2019 20:37:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b51234177bc6b7277430cb5472a8d9425e04724da9fe9deba285a1ecd11816`  
		Last Modified: Sat, 28 Dec 2019 20:38:32 GMT  
		Size: 219.1 MB (219146537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91e4ed0acf4dd4d40899c29df92c1ac4cdd0bc11e7ce90be6f281861261bbe`  
		Last Modified: Sat, 28 Dec 2019 20:37:55 GMT  
		Size: 2.2 MB (2244396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f824357021b0edd4c708eb534ea0c353b2f6b9206ab774defdc3dbaa97084f`  
		Last Modified: Sat, 28 Dec 2019 20:38:05 GMT  
		Size: 26.5 MB (26548363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ff64c1762011f0525f39841cbc5f32d8fbdce840373bdd32e841abb958a77b`  
		Last Modified: Sat, 28 Dec 2019 20:38:37 GMT  
		Size: 128.7 MB (128654592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e883e358b73f6c8c269daa218d1e4b8bdb360e29fbffd14c335bb332668c7eca`  
		Last Modified: Sat, 28 Dec 2019 20:37:54 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71297401ac468dd5608b03c55d9acc5ffb865cc3ef3d98b3e3698ff0d0add9ed`  
		Last Modified: Sat, 28 Dec 2019 20:37:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f684a5032d1e291b24cdfe1bed0255ef8c2844a7e07aed8657cf2aec5782a95a`  
		Last Modified: Sat, 28 Dec 2019 20:37:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c633c1aa07d7a349b9df0c82d35d7d427646110bff2c0506d717b0cff00c63d`  
		Last Modified: Sat, 28 Dec 2019 20:37:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443518a6b6bd4a892d073dce3ca0bf396755206271ed01343d00da60ac5b7499`  
		Last Modified: Sat, 28 Dec 2019 20:37:53 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:ca2fd0c88b0065c719c60f95037a68d38cc57bf7795f43b7e7d84a2a23f6ef62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:28ee3e13cd403f0e35af460d6070521b0fb6c00161c7fd64a05d670e497c41da
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.1 MB (399121221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1eec67b651e18c673b89c745b29969cae203688e220aaf0cda44413da59dec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:31:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 Dec 2019 20:31:52 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 20:31:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 28 Dec 2019 20:33:43 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-vobject             python3-watchdog             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 Dec 2019 20:33:53 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:34:19 GMT
RUN set -x;    echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && export GNUPGHOME="$(mktemp -d)"     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:34:20 GMT
ENV ODOO_VERSION=12.0
# Sat, 28 Dec 2019 20:34:20 GMT
ARG ODOO_RELEASE=20191106
# Sat, 28 Dec 2019 20:34:20 GMT
ARG ODOO_SHA=8dd3d36bd371b1eb6fbeb9ff7b049c8aea84327c
# Sat, 28 Dec 2019 20:35:36 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=8dd3d36bd371b1eb6fbeb9ff7b049c8aea84327c
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 Dec 2019 20:35:37 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 28 Dec 2019 20:35:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 Dec 2019 20:35:38 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=8dd3d36bd371b1eb6fbeb9ff7b049c8aea84327c
RUN chown odoo /etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:35:39 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=8dd3d36bd371b1eb6fbeb9ff7b049c8aea84327c
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Sat, 28 Dec 2019 20:35:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 Dec 2019 20:35:39 GMT
EXPOSE 8069 8071
# Sat, 28 Dec 2019 20:35:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:35:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 Dec 2019 20:35:40 GMT
USER odoo
# Sat, 28 Dec 2019 20:35:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 20:35:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb235ca4180b231aa378f7d9ea5ef403d0756a990ec133fabb5f212ac0f34f`  
		Last Modified: Sat, 28 Dec 2019 20:37:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b51234177bc6b7277430cb5472a8d9425e04724da9fe9deba285a1ecd11816`  
		Last Modified: Sat, 28 Dec 2019 20:38:32 GMT  
		Size: 219.1 MB (219146537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91e4ed0acf4dd4d40899c29df92c1ac4cdd0bc11e7ce90be6f281861261bbe`  
		Last Modified: Sat, 28 Dec 2019 20:37:55 GMT  
		Size: 2.2 MB (2244396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f824357021b0edd4c708eb534ea0c353b2f6b9206ab774defdc3dbaa97084f`  
		Last Modified: Sat, 28 Dec 2019 20:38:05 GMT  
		Size: 26.5 MB (26548363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ff64c1762011f0525f39841cbc5f32d8fbdce840373bdd32e841abb958a77b`  
		Last Modified: Sat, 28 Dec 2019 20:38:37 GMT  
		Size: 128.7 MB (128654592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e883e358b73f6c8c269daa218d1e4b8bdb360e29fbffd14c335bb332668c7eca`  
		Last Modified: Sat, 28 Dec 2019 20:37:54 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71297401ac468dd5608b03c55d9acc5ffb865cc3ef3d98b3e3698ff0d0add9ed`  
		Last Modified: Sat, 28 Dec 2019 20:37:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f684a5032d1e291b24cdfe1bed0255ef8c2844a7e07aed8657cf2aec5782a95a`  
		Last Modified: Sat, 28 Dec 2019 20:37:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c633c1aa07d7a349b9df0c82d35d7d427646110bff2c0506d717b0cff00c63d`  
		Last Modified: Sat, 28 Dec 2019 20:37:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443518a6b6bd4a892d073dce3ca0bf396755206271ed01343d00da60ac5b7499`  
		Last Modified: Sat, 28 Dec 2019 20:37:53 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:bf92d70646503d0352dc414ccdb541154a1ed190c50aba88dfa3b8208214a7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:baf375103c8e7b95234ba34433f7c6662a4d39d9cafc9fed385a74dc00ae7487
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.0 MB (371965239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ccea1d7411082a0901faee1d9b6747216ca21fc8381849716eb2775408088a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:28:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 Dec 2019 20:28:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 20:30:00 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-vobject             python3-watchdog             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 Dec 2019 20:30:08 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:30:11 GMT
RUN set -x;     npm install -g rtlcss
# Sat, 28 Dec 2019 20:30:11 GMT
ENV ODOO_VERSION=13.0
# Sat, 28 Dec 2019 20:30:12 GMT
ARG ODOO_RELEASE=20191106
# Sat, 28 Dec 2019 20:30:12 GMT
ARG ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
# Sat, 28 Dec 2019 20:31:39 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 Dec 2019 20:31:41 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 28 Dec 2019 20:31:41 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 Dec 2019 20:31:43 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
RUN chown odoo /etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:31:44 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Sat, 28 Dec 2019 20:31:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 Dec 2019 20:31:45 GMT
EXPOSE 8069 8071
# Sat, 28 Dec 2019 20:31:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:31:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 Dec 2019 20:31:45 GMT
USER odoo
# Sat, 28 Dec 2019 20:31:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 20:31:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eb32ae630decd9a2713e769c3bdc1e9a73bdcf896684692000fe48e8420eaa`  
		Last Modified: Sat, 28 Dec 2019 20:37:40 GMT  
		Size: 203.1 MB (203055266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c497cfaef849bb14e872d1c6f31a88f41173a7b8dafe4b9883e908e0910b4`  
		Last Modified: Sat, 28 Dec 2019 20:37:01 GMT  
		Size: 2.2 MB (2227015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d3cdf0ccf61fa2acbac1f853bd44e71c4c2dd77ddda684e4ce12e87718ad5d`  
		Last Modified: Sat, 28 Dec 2019 20:37:01 GMT  
		Size: 1.1 MB (1068139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22ca9894eb2fca8484239a454edd894182b78bd5e9e94699a410f573f78bb7c`  
		Last Modified: Sat, 28 Dec 2019 20:37:48 GMT  
		Size: 138.5 MB (138520049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d8c9a75ca00d8129fa1aaa66402768bd7f5ebe06332adcca36dcbd697bfff9`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb3c2961e0fe461e341e426fb76f13479e587b0bdb908f7bd0c51586b1a7c88`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b98a32836e88ad05baab88eadd36c291fe5d883ac04862115b2aa8c3c60fe4`  
		Last Modified: Sat, 28 Dec 2019 20:36:59 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3e8c93afedb044029141b836e32b519f912f0be9259f05a324e3dbea86998b`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6daead20304b521100f15d682bd4fd6d37d0321536c52e0e1bf3070e89ff0f`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:bf92d70646503d0352dc414ccdb541154a1ed190c50aba88dfa3b8208214a7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:baf375103c8e7b95234ba34433f7c6662a4d39d9cafc9fed385a74dc00ae7487
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.0 MB (371965239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ccea1d7411082a0901faee1d9b6747216ca21fc8381849716eb2775408088a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:28:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 Dec 2019 20:28:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 20:30:00 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-vobject             python3-watchdog             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 Dec 2019 20:30:08 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:30:11 GMT
RUN set -x;     npm install -g rtlcss
# Sat, 28 Dec 2019 20:30:11 GMT
ENV ODOO_VERSION=13.0
# Sat, 28 Dec 2019 20:30:12 GMT
ARG ODOO_RELEASE=20191106
# Sat, 28 Dec 2019 20:30:12 GMT
ARG ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
# Sat, 28 Dec 2019 20:31:39 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 Dec 2019 20:31:41 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 28 Dec 2019 20:31:41 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 Dec 2019 20:31:43 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
RUN chown odoo /etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:31:44 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Sat, 28 Dec 2019 20:31:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 Dec 2019 20:31:45 GMT
EXPOSE 8069 8071
# Sat, 28 Dec 2019 20:31:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:31:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 Dec 2019 20:31:45 GMT
USER odoo
# Sat, 28 Dec 2019 20:31:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 20:31:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eb32ae630decd9a2713e769c3bdc1e9a73bdcf896684692000fe48e8420eaa`  
		Last Modified: Sat, 28 Dec 2019 20:37:40 GMT  
		Size: 203.1 MB (203055266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c497cfaef849bb14e872d1c6f31a88f41173a7b8dafe4b9883e908e0910b4`  
		Last Modified: Sat, 28 Dec 2019 20:37:01 GMT  
		Size: 2.2 MB (2227015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d3cdf0ccf61fa2acbac1f853bd44e71c4c2dd77ddda684e4ce12e87718ad5d`  
		Last Modified: Sat, 28 Dec 2019 20:37:01 GMT  
		Size: 1.1 MB (1068139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22ca9894eb2fca8484239a454edd894182b78bd5e9e94699a410f573f78bb7c`  
		Last Modified: Sat, 28 Dec 2019 20:37:48 GMT  
		Size: 138.5 MB (138520049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d8c9a75ca00d8129fa1aaa66402768bd7f5ebe06332adcca36dcbd697bfff9`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb3c2961e0fe461e341e426fb76f13479e587b0bdb908f7bd0c51586b1a7c88`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b98a32836e88ad05baab88eadd36c291fe5d883ac04862115b2aa8c3c60fe4`  
		Last Modified: Sat, 28 Dec 2019 20:36:59 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3e8c93afedb044029141b836e32b519f912f0be9259f05a324e3dbea86998b`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6daead20304b521100f15d682bd4fd6d37d0321536c52e0e1bf3070e89ff0f`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:bf92d70646503d0352dc414ccdb541154a1ed190c50aba88dfa3b8208214a7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:baf375103c8e7b95234ba34433f7c6662a4d39d9cafc9fed385a74dc00ae7487
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.0 MB (371965239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ccea1d7411082a0901faee1d9b6747216ca21fc8381849716eb2775408088a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:28:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 Dec 2019 20:28:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 20:30:00 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-vobject             python3-watchdog             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 Dec 2019 20:30:08 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:30:11 GMT
RUN set -x;     npm install -g rtlcss
# Sat, 28 Dec 2019 20:30:11 GMT
ENV ODOO_VERSION=13.0
# Sat, 28 Dec 2019 20:30:12 GMT
ARG ODOO_RELEASE=20191106
# Sat, 28 Dec 2019 20:30:12 GMT
ARG ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
# Sat, 28 Dec 2019 20:31:39 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 Dec 2019 20:31:41 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 28 Dec 2019 20:31:41 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 Dec 2019 20:31:43 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
RUN chown odoo /etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:31:44 GMT
# ARGS: ODOO_RELEASE=20191106 ODOO_SHA=b13bec4d20dfe36f1baa923719e37ea6bbe18a7d
RUN mkdir -p /mnt/extra-addons         && chown -R odoo /mnt/extra-addons
# Sat, 28 Dec 2019 20:31:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 Dec 2019 20:31:45 GMT
EXPOSE 8069 8071
# Sat, 28 Dec 2019 20:31:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 Dec 2019 20:31:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 Dec 2019 20:31:45 GMT
USER odoo
# Sat, 28 Dec 2019 20:31:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 20:31:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eb32ae630decd9a2713e769c3bdc1e9a73bdcf896684692000fe48e8420eaa`  
		Last Modified: Sat, 28 Dec 2019 20:37:40 GMT  
		Size: 203.1 MB (203055266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57c497cfaef849bb14e872d1c6f31a88f41173a7b8dafe4b9883e908e0910b4`  
		Last Modified: Sat, 28 Dec 2019 20:37:01 GMT  
		Size: 2.2 MB (2227015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d3cdf0ccf61fa2acbac1f853bd44e71c4c2dd77ddda684e4ce12e87718ad5d`  
		Last Modified: Sat, 28 Dec 2019 20:37:01 GMT  
		Size: 1.1 MB (1068139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22ca9894eb2fca8484239a454edd894182b78bd5e9e94699a410f573f78bb7c`  
		Last Modified: Sat, 28 Dec 2019 20:37:48 GMT  
		Size: 138.5 MB (138520049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d8c9a75ca00d8129fa1aaa66402768bd7f5ebe06332adcca36dcbd697bfff9`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb3c2961e0fe461e341e426fb76f13479e587b0bdb908f7bd0c51586b1a7c88`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b98a32836e88ad05baab88eadd36c291fe5d883ac04862115b2aa8c3c60fe4`  
		Last Modified: Sat, 28 Dec 2019 20:36:59 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3e8c93afedb044029141b836e32b519f912f0be9259f05a324e3dbea86998b`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6daead20304b521100f15d682bd4fd6d37d0321536c52e0e1bf3070e89ff0f`  
		Last Modified: Sat, 28 Dec 2019 20:37:00 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
