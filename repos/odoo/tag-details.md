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
$ docker pull odoo@sha256:dab83ec3cbb74638ce523cc50845f030b2c951fc55d8b92435c2d00b8fae6b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:6197b276a3ea4958dd144ee9d2ebd5a7649f6d605f61ff0a2bdb9552960ebbc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 MB (396780667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d981578b834eb77e7453294ec8b13e2e2a4d828a7beadcc9a805cc83d0dc61a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:55:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:55:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:55:53 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:55:54 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 12 Jan 2021 00:57:36 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:57:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:58:00 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:58:00 GMT
ENV ODOO_VERSION=12.0
# Tue, 12 Jan 2021 00:58:01 GMT
ARG ODOO_RELEASE=20210111
# Tue, 12 Jan 2021 00:58:01 GMT
ARG ODOO_SHA=73dd74d0185588fbe052471217b28c1f796a542c
# Tue, 12 Jan 2021 00:58:46 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=73dd74d0185588fbe052471217b28c1f796a542c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jan 2021 00:58:47 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 12 Jan 2021 00:58:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jan 2021 00:58:48 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=73dd74d0185588fbe052471217b28c1f796a542c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jan 2021 00:58:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jan 2021 00:58:49 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jan 2021 00:58:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jan 2021 00:58:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jan 2021 00:58:49 GMT
USER odoo
# Tue, 12 Jan 2021 00:58:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 00:58:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144f7caa9bd25e2b72d1da03a44c4586ddda32d8ec266504d0d1f30dea2a258e`  
		Last Modified: Tue, 12 Jan 2021 01:01:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f19c61dd7d315c35e54a26918c3cd5063439d4351dde65b8241346417d9f526`  
		Last Modified: Tue, 12 Jan 2021 01:01:36 GMT  
		Size: 219.6 MB (219610747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5a45cdf8624c5c0646079590cea4c6a7938e46dde1b2377a4353a59614c975`  
		Last Modified: Tue, 12 Jan 2021 01:01:05 GMT  
		Size: 2.2 MB (2222454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de80d7b651bc767ace9dafdb74e322d2fc4ca04b271eb8cd5f8d1b1346518171`  
		Last Modified: Tue, 12 Jan 2021 01:01:13 GMT  
		Size: 22.1 MB (22080263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd473675d1bf29c2e8b8d384fb8325a382f93b27b408cb4b4f6aecefbde720`  
		Last Modified: Tue, 12 Jan 2021 01:01:40 GMT  
		Size: 130.3 MB (130335961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a668c69d0d05128c81075624f2eb2de3f68c956d8374d86664a0c71e516e819e`  
		Last Modified: Tue, 12 Jan 2021 01:01:03 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6f36783bd54e79225235c883a6eb719f118cd12149500d87d03bc10e849d26`  
		Last Modified: Tue, 12 Jan 2021 01:01:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad57769956c83d9317b6c553a4377bc980d91c3b8990784133cca5399aaeb0c1`  
		Last Modified: Tue, 12 Jan 2021 01:01:02 GMT  
		Size: 596.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99063d53665a195eda5b6493e93373ba9cde962ed7b9da3b71c12f0f98e0e3ee`  
		Last Modified: Tue, 12 Jan 2021 01:01:02 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:dab83ec3cbb74638ce523cc50845f030b2c951fc55d8b92435c2d00b8fae6b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:6197b276a3ea4958dd144ee9d2ebd5a7649f6d605f61ff0a2bdb9552960ebbc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 MB (396780667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d981578b834eb77e7453294ec8b13e2e2a4d828a7beadcc9a805cc83d0dc61a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:55:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:55:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:55:53 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:55:54 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 12 Jan 2021 00:57:36 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:57:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:58:00 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:58:00 GMT
ENV ODOO_VERSION=12.0
# Tue, 12 Jan 2021 00:58:01 GMT
ARG ODOO_RELEASE=20210111
# Tue, 12 Jan 2021 00:58:01 GMT
ARG ODOO_SHA=73dd74d0185588fbe052471217b28c1f796a542c
# Tue, 12 Jan 2021 00:58:46 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=73dd74d0185588fbe052471217b28c1f796a542c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jan 2021 00:58:47 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 12 Jan 2021 00:58:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jan 2021 00:58:48 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=73dd74d0185588fbe052471217b28c1f796a542c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jan 2021 00:58:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jan 2021 00:58:49 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jan 2021 00:58:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jan 2021 00:58:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jan 2021 00:58:49 GMT
USER odoo
# Tue, 12 Jan 2021 00:58:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 00:58:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144f7caa9bd25e2b72d1da03a44c4586ddda32d8ec266504d0d1f30dea2a258e`  
		Last Modified: Tue, 12 Jan 2021 01:01:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f19c61dd7d315c35e54a26918c3cd5063439d4351dde65b8241346417d9f526`  
		Last Modified: Tue, 12 Jan 2021 01:01:36 GMT  
		Size: 219.6 MB (219610747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5a45cdf8624c5c0646079590cea4c6a7938e46dde1b2377a4353a59614c975`  
		Last Modified: Tue, 12 Jan 2021 01:01:05 GMT  
		Size: 2.2 MB (2222454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de80d7b651bc767ace9dafdb74e322d2fc4ca04b271eb8cd5f8d1b1346518171`  
		Last Modified: Tue, 12 Jan 2021 01:01:13 GMT  
		Size: 22.1 MB (22080263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd473675d1bf29c2e8b8d384fb8325a382f93b27b408cb4b4f6aecefbde720`  
		Last Modified: Tue, 12 Jan 2021 01:01:40 GMT  
		Size: 130.3 MB (130335961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a668c69d0d05128c81075624f2eb2de3f68c956d8374d86664a0c71e516e819e`  
		Last Modified: Tue, 12 Jan 2021 01:01:03 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6f36783bd54e79225235c883a6eb719f118cd12149500d87d03bc10e849d26`  
		Last Modified: Tue, 12 Jan 2021 01:01:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad57769956c83d9317b6c553a4377bc980d91c3b8990784133cca5399aaeb0c1`  
		Last Modified: Tue, 12 Jan 2021 01:01:02 GMT  
		Size: 596.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99063d53665a195eda5b6493e93373ba9cde962ed7b9da3b71c12f0f98e0e3ee`  
		Last Modified: Tue, 12 Jan 2021 01:01:02 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:a2527ce503ab191319fef840f94dc9b4c03d81fe8fac72209c763be43444cc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:c595663dbbceefbcb980d08fec0d42f280e6c257060000c7c074d8560378121f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386410117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3114b53eb98e19b39d716a0d6383e5ea076c39ed0cb775d85ee14d9b858a8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:54:32 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:54:43 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:54:43 GMT
ENV ODOO_VERSION=13.0
# Tue, 12 Jan 2021 00:54:43 GMT
ARG ODOO_RELEASE=20210111
# Tue, 12 Jan 2021 00:54:43 GMT
ARG ODOO_SHA=0d5d6cac754a61713d9a6e0bb226a51fee70941b
# Tue, 12 Jan 2021 00:55:39 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=0d5d6cac754a61713d9a6e0bb226a51fee70941b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jan 2021 00:55:40 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 12 Jan 2021 00:55:40 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jan 2021 00:55:41 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=0d5d6cac754a61713d9a6e0bb226a51fee70941b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jan 2021 00:55:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jan 2021 00:55:42 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jan 2021 00:55:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jan 2021 00:55:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jan 2021 00:55:42 GMT
USER odoo
# Tue, 12 Jan 2021 00:55:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 00:55:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbc8150f914f7dfd3a86c36b11e2952c897d2730354c258e267ac557063299c`  
		Last Modified: Tue, 12 Jan 2021 01:00:49 GMT  
		Size: 207.1 MB (207075553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1747c1263d10944107d89956ecb6fe0a0ae422613398fbf0a0dd89bd1d2c93`  
		Last Modified: Tue, 12 Jan 2021 01:00:10 GMT  
		Size: 2.3 MB (2343766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc37aeea17bfe20046e96480e4e1f4790b31b216198d11c48ed495e8a2bf97`  
		Last Modified: Tue, 12 Jan 2021 01:00:10 GMT  
		Size: 929.3 KB (929297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93626b4cf1c6d4a3f5a361bd6e1e4e924bf5713af4b26e02c81cab5ab87d1bbb`  
		Last Modified: Tue, 12 Jan 2021 01:00:55 GMT  
		Size: 149.0 MB (148951036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381dfb3e18aea2b50a12fe3b72c9968d1aa39178602a75c0d92588e7564facb9`  
		Last Modified: Tue, 12 Jan 2021 01:00:07 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520205d9795e134cc0396ccebbd758e9ae69b079aaeb3cd938f72d4c83f6dd5f`  
		Last Modified: Tue, 12 Jan 2021 01:00:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a7343c615f13a9a5710e1893009a3f5b3aad4ec2cc37aabf660709a59e2acf`  
		Last Modified: Tue, 12 Jan 2021 01:00:08 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103e3ea1103726e61a1aa9457a85253356d2aabf4d30197d3dfa556a9af2924f`  
		Last Modified: Tue, 12 Jan 2021 01:00:08 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:a2527ce503ab191319fef840f94dc9b4c03d81fe8fac72209c763be43444cc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:c595663dbbceefbcb980d08fec0d42f280e6c257060000c7c074d8560378121f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386410117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3114b53eb98e19b39d716a0d6383e5ea076c39ed0cb775d85ee14d9b858a8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:54:32 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:54:43 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:54:43 GMT
ENV ODOO_VERSION=13.0
# Tue, 12 Jan 2021 00:54:43 GMT
ARG ODOO_RELEASE=20210111
# Tue, 12 Jan 2021 00:54:43 GMT
ARG ODOO_SHA=0d5d6cac754a61713d9a6e0bb226a51fee70941b
# Tue, 12 Jan 2021 00:55:39 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=0d5d6cac754a61713d9a6e0bb226a51fee70941b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jan 2021 00:55:40 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 12 Jan 2021 00:55:40 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jan 2021 00:55:41 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=0d5d6cac754a61713d9a6e0bb226a51fee70941b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jan 2021 00:55:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jan 2021 00:55:42 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jan 2021 00:55:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jan 2021 00:55:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jan 2021 00:55:42 GMT
USER odoo
# Tue, 12 Jan 2021 00:55:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 00:55:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbc8150f914f7dfd3a86c36b11e2952c897d2730354c258e267ac557063299c`  
		Last Modified: Tue, 12 Jan 2021 01:00:49 GMT  
		Size: 207.1 MB (207075553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1747c1263d10944107d89956ecb6fe0a0ae422613398fbf0a0dd89bd1d2c93`  
		Last Modified: Tue, 12 Jan 2021 01:00:10 GMT  
		Size: 2.3 MB (2343766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc37aeea17bfe20046e96480e4e1f4790b31b216198d11c48ed495e8a2bf97`  
		Last Modified: Tue, 12 Jan 2021 01:00:10 GMT  
		Size: 929.3 KB (929297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93626b4cf1c6d4a3f5a361bd6e1e4e924bf5713af4b26e02c81cab5ab87d1bbb`  
		Last Modified: Tue, 12 Jan 2021 01:00:55 GMT  
		Size: 149.0 MB (148951036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381dfb3e18aea2b50a12fe3b72c9968d1aa39178602a75c0d92588e7564facb9`  
		Last Modified: Tue, 12 Jan 2021 01:00:07 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520205d9795e134cc0396ccebbd758e9ae69b079aaeb3cd938f72d4c83f6dd5f`  
		Last Modified: Tue, 12 Jan 2021 01:00:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a7343c615f13a9a5710e1893009a3f5b3aad4ec2cc37aabf660709a59e2acf`  
		Last Modified: Tue, 12 Jan 2021 01:00:08 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103e3ea1103726e61a1aa9457a85253356d2aabf4d30197d3dfa556a9af2924f`  
		Last Modified: Tue, 12 Jan 2021 01:00:08 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:b4b86dae5253cfa1c6423960c302ccc9805833133aa5ce6146f60da3b9a2db6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:23ccd7deac2664336b94543e3f2653631f0c8e2a562ffa15812805c7ef899827
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404727642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3863e3e905e5d0e56a7bd66e2aa65885e241759b2001a20a65e59aad4fceeba4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:51:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:51:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:52:01 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:52:02 GMT
ENV ODOO_VERSION=14.0
# Tue, 12 Jan 2021 00:52:02 GMT
ARG ODOO_RELEASE=20210111
# Tue, 12 Jan 2021 00:52:02 GMT
ARG ODOO_SHA=dc97e990bfabf167159a16fbf7437f7490bab46b
# Tue, 12 Jan 2021 00:53:04 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=dc97e990bfabf167159a16fbf7437f7490bab46b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jan 2021 00:53:05 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 12 Jan 2021 00:53:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jan 2021 00:53:07 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=dc97e990bfabf167159a16fbf7437f7490bab46b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jan 2021 00:53:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jan 2021 00:53:07 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jan 2021 00:53:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jan 2021 00:53:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jan 2021 00:53:08 GMT
USER odoo
# Tue, 12 Jan 2021 00:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 00:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab3d9c87ea56d61be174c3af26ba561264a3c4a33447aa043ca3556ac5773a`  
		Last Modified: Tue, 12 Jan 2021 00:59:47 GMT  
		Size: 213.1 MB (213119359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80c09c10568e31cea43092e745e65e1ca21e5760faa0946402879a9af67c35`  
		Last Modified: Tue, 12 Jan 2021 00:59:09 GMT  
		Size: 2.3 MB (2346263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce3bc0bd27d17449f9993b0ee55b39ba3098120132f2723ce7cef93ca0f3a4d`  
		Last Modified: Tue, 12 Jan 2021 00:59:10 GMT  
		Size: 929.2 KB (929195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf9cd3f8f09ebe3a9675e8fb73554b7e5292ad441ca5abfa3735be41be73d7e`  
		Last Modified: Tue, 12 Jan 2021 00:59:57 GMT  
		Size: 161.2 MB (161222355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768e25cfb48d24741dfe8cfb156bcb9dbb9580cc1b0e440115bd95bb2ffe99a6`  
		Last Modified: Tue, 12 Jan 2021 00:59:09 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2379efa85d34259e2e933692b01ff3d7cec697ab32c549c135ddb16597d115`  
		Last Modified: Tue, 12 Jan 2021 00:59:08 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f33e45556037d4250bd90c4e4664f74b614c47636492c82d96bceaeba406d3c`  
		Last Modified: Tue, 12 Jan 2021 00:59:08 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700ec892db510f0ed1d7de5dddf0a0e50cdb75c7afb60dc23bcaa10f6a9f8984`  
		Last Modified: Tue, 12 Jan 2021 00:59:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:b4b86dae5253cfa1c6423960c302ccc9805833133aa5ce6146f60da3b9a2db6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:23ccd7deac2664336b94543e3f2653631f0c8e2a562ffa15812805c7ef899827
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404727642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3863e3e905e5d0e56a7bd66e2aa65885e241759b2001a20a65e59aad4fceeba4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:51:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:51:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:52:01 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:52:02 GMT
ENV ODOO_VERSION=14.0
# Tue, 12 Jan 2021 00:52:02 GMT
ARG ODOO_RELEASE=20210111
# Tue, 12 Jan 2021 00:52:02 GMT
ARG ODOO_SHA=dc97e990bfabf167159a16fbf7437f7490bab46b
# Tue, 12 Jan 2021 00:53:04 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=dc97e990bfabf167159a16fbf7437f7490bab46b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jan 2021 00:53:05 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 12 Jan 2021 00:53:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jan 2021 00:53:07 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=dc97e990bfabf167159a16fbf7437f7490bab46b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jan 2021 00:53:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jan 2021 00:53:07 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jan 2021 00:53:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jan 2021 00:53:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jan 2021 00:53:08 GMT
USER odoo
# Tue, 12 Jan 2021 00:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 00:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab3d9c87ea56d61be174c3af26ba561264a3c4a33447aa043ca3556ac5773a`  
		Last Modified: Tue, 12 Jan 2021 00:59:47 GMT  
		Size: 213.1 MB (213119359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80c09c10568e31cea43092e745e65e1ca21e5760faa0946402879a9af67c35`  
		Last Modified: Tue, 12 Jan 2021 00:59:09 GMT  
		Size: 2.3 MB (2346263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce3bc0bd27d17449f9993b0ee55b39ba3098120132f2723ce7cef93ca0f3a4d`  
		Last Modified: Tue, 12 Jan 2021 00:59:10 GMT  
		Size: 929.2 KB (929195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf9cd3f8f09ebe3a9675e8fb73554b7e5292ad441ca5abfa3735be41be73d7e`  
		Last Modified: Tue, 12 Jan 2021 00:59:57 GMT  
		Size: 161.2 MB (161222355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768e25cfb48d24741dfe8cfb156bcb9dbb9580cc1b0e440115bd95bb2ffe99a6`  
		Last Modified: Tue, 12 Jan 2021 00:59:09 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2379efa85d34259e2e933692b01ff3d7cec697ab32c549c135ddb16597d115`  
		Last Modified: Tue, 12 Jan 2021 00:59:08 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f33e45556037d4250bd90c4e4664f74b614c47636492c82d96bceaeba406d3c`  
		Last Modified: Tue, 12 Jan 2021 00:59:08 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700ec892db510f0ed1d7de5dddf0a0e50cdb75c7afb60dc23bcaa10f6a9f8984`  
		Last Modified: Tue, 12 Jan 2021 00:59:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:b4b86dae5253cfa1c6423960c302ccc9805833133aa5ce6146f60da3b9a2db6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:23ccd7deac2664336b94543e3f2653631f0c8e2a562ffa15812805c7ef899827
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404727642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3863e3e905e5d0e56a7bd66e2aa65885e241759b2001a20a65e59aad4fceeba4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:51:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:51:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:52:01 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:52:02 GMT
ENV ODOO_VERSION=14.0
# Tue, 12 Jan 2021 00:52:02 GMT
ARG ODOO_RELEASE=20210111
# Tue, 12 Jan 2021 00:52:02 GMT
ARG ODOO_SHA=dc97e990bfabf167159a16fbf7437f7490bab46b
# Tue, 12 Jan 2021 00:53:04 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=dc97e990bfabf167159a16fbf7437f7490bab46b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jan 2021 00:53:05 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 12 Jan 2021 00:53:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jan 2021 00:53:07 GMT
# ARGS: ODOO_RELEASE=20210111 ODOO_SHA=dc97e990bfabf167159a16fbf7437f7490bab46b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jan 2021 00:53:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jan 2021 00:53:07 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jan 2021 00:53:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jan 2021 00:53:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jan 2021 00:53:08 GMT
USER odoo
# Tue, 12 Jan 2021 00:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 00:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab3d9c87ea56d61be174c3af26ba561264a3c4a33447aa043ca3556ac5773a`  
		Last Modified: Tue, 12 Jan 2021 00:59:47 GMT  
		Size: 213.1 MB (213119359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80c09c10568e31cea43092e745e65e1ca21e5760faa0946402879a9af67c35`  
		Last Modified: Tue, 12 Jan 2021 00:59:09 GMT  
		Size: 2.3 MB (2346263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce3bc0bd27d17449f9993b0ee55b39ba3098120132f2723ce7cef93ca0f3a4d`  
		Last Modified: Tue, 12 Jan 2021 00:59:10 GMT  
		Size: 929.2 KB (929195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf9cd3f8f09ebe3a9675e8fb73554b7e5292ad441ca5abfa3735be41be73d7e`  
		Last Modified: Tue, 12 Jan 2021 00:59:57 GMT  
		Size: 161.2 MB (161222355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768e25cfb48d24741dfe8cfb156bcb9dbb9580cc1b0e440115bd95bb2ffe99a6`  
		Last Modified: Tue, 12 Jan 2021 00:59:09 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2379efa85d34259e2e933692b01ff3d7cec697ab32c549c135ddb16597d115`  
		Last Modified: Tue, 12 Jan 2021 00:59:08 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f33e45556037d4250bd90c4e4664f74b614c47636492c82d96bceaeba406d3c`  
		Last Modified: Tue, 12 Jan 2021 00:59:08 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700ec892db510f0ed1d7de5dddf0a0e50cdb75c7afb60dc23bcaa10f6a9f8984`  
		Last Modified: Tue, 12 Jan 2021 00:59:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
