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
$ docker pull odoo@sha256:c63e9b85a494ae1d394ae9de8e2321f56c01eed5197e5d87a31bd34f271ec7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:40f010eaba53ac9d1d2e26c8167cdb87b0111887e9bd37e3e0e473dbac29d628
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396689198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6c33e27e1a276b78fd6510c6adec7b17ebbfbff8d50663830a97d8ea0c526b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:22:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:22:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:22:07 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:22:10 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 11 Dec 2020 17:23:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:23:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:24:10 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:24:10 GMT
ENV ODOO_VERSION=12.0
# Fri, 18 Dec 2020 19:56:10 GMT
ARG ODOO_RELEASE=20201218
# Fri, 18 Dec 2020 19:56:11 GMT
ARG ODOO_SHA=c26bc7a3df829bf7e01eae0fb54a5c9d1dbe56ab
# Fri, 18 Dec 2020 19:57:20 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=c26bc7a3df829bf7e01eae0fb54a5c9d1dbe56ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Dec 2020 19:57:21 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Dec 2020 19:57:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Dec 2020 19:57:23 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=c26bc7a3df829bf7e01eae0fb54a5c9d1dbe56ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Dec 2020 19:57:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Dec 2020 19:57:24 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Dec 2020 19:57:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Dec 2020 19:57:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Dec 2020 19:57:25 GMT
USER odoo
# Fri, 18 Dec 2020 19:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Dec 2020 19:57:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a5fca80cf5e4be20355b1886a25d710803679f0a7c71ded0c3de6cae19c19d`  
		Last Modified: Fri, 11 Dec 2020 17:27:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99fdce30aebd92be43edc52d36e352ca174d0cf9a2ede367bc7ace614b2746c`  
		Last Modified: Fri, 11 Dec 2020 17:28:27 GMT  
		Size: 219.6 MB (219607697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1f090eb0f54f5b004406240879df2b21117f6e204f42865488fda72dc7d163`  
		Last Modified: Fri, 11 Dec 2020 17:27:24 GMT  
		Size: 2.2 MB (2222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce3bbc0a15d1cc1dad99fd8f34e340d95df6039650826577c8a8ceb35221431`  
		Last Modified: Fri, 11 Dec 2020 17:27:38 GMT  
		Size: 22.1 MB (22069709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec720321086c81c409340aef4c38decf2d67dff62e86f4cf8b3618e3f5c8d07`  
		Last Modified: Fri, 18 Dec 2020 20:00:01 GMT  
		Size: 130.3 MB (130258935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db79354304bf235af83f3d10bae0709e8d98112f922431233d43f01ef8292fd8`  
		Last Modified: Fri, 18 Dec 2020 19:59:34 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d56f6ca456b5705b1ca8fabbeaa75d86f6bc7db6ff48d2d929d0a91c57182d3`  
		Last Modified: Fri, 18 Dec 2020 19:59:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9371022835c0a54067cdb2544da6bfbf64ce6632e1b638d795d6445a9579a9`  
		Last Modified: Fri, 18 Dec 2020 19:59:34 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6745c3a6d506a5e0128a176d39e1101562ddceb8cdb582ded9962bd4715d89`  
		Last Modified: Fri, 18 Dec 2020 19:59:34 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:c63e9b85a494ae1d394ae9de8e2321f56c01eed5197e5d87a31bd34f271ec7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:40f010eaba53ac9d1d2e26c8167cdb87b0111887e9bd37e3e0e473dbac29d628
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396689198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6c33e27e1a276b78fd6510c6adec7b17ebbfbff8d50663830a97d8ea0c526b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:22:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:22:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:22:07 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:22:10 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 11 Dec 2020 17:23:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:23:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:24:10 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:24:10 GMT
ENV ODOO_VERSION=12.0
# Fri, 18 Dec 2020 19:56:10 GMT
ARG ODOO_RELEASE=20201218
# Fri, 18 Dec 2020 19:56:11 GMT
ARG ODOO_SHA=c26bc7a3df829bf7e01eae0fb54a5c9d1dbe56ab
# Fri, 18 Dec 2020 19:57:20 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=c26bc7a3df829bf7e01eae0fb54a5c9d1dbe56ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Dec 2020 19:57:21 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Dec 2020 19:57:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Dec 2020 19:57:23 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=c26bc7a3df829bf7e01eae0fb54a5c9d1dbe56ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Dec 2020 19:57:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Dec 2020 19:57:24 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Dec 2020 19:57:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Dec 2020 19:57:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Dec 2020 19:57:25 GMT
USER odoo
# Fri, 18 Dec 2020 19:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Dec 2020 19:57:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a5fca80cf5e4be20355b1886a25d710803679f0a7c71ded0c3de6cae19c19d`  
		Last Modified: Fri, 11 Dec 2020 17:27:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99fdce30aebd92be43edc52d36e352ca174d0cf9a2ede367bc7ace614b2746c`  
		Last Modified: Fri, 11 Dec 2020 17:28:27 GMT  
		Size: 219.6 MB (219607697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1f090eb0f54f5b004406240879df2b21117f6e204f42865488fda72dc7d163`  
		Last Modified: Fri, 11 Dec 2020 17:27:24 GMT  
		Size: 2.2 MB (2222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce3bbc0a15d1cc1dad99fd8f34e340d95df6039650826577c8a8ceb35221431`  
		Last Modified: Fri, 11 Dec 2020 17:27:38 GMT  
		Size: 22.1 MB (22069709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec720321086c81c409340aef4c38decf2d67dff62e86f4cf8b3618e3f5c8d07`  
		Last Modified: Fri, 18 Dec 2020 20:00:01 GMT  
		Size: 130.3 MB (130258935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db79354304bf235af83f3d10bae0709e8d98112f922431233d43f01ef8292fd8`  
		Last Modified: Fri, 18 Dec 2020 19:59:34 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d56f6ca456b5705b1ca8fabbeaa75d86f6bc7db6ff48d2d929d0a91c57182d3`  
		Last Modified: Fri, 18 Dec 2020 19:59:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9371022835c0a54067cdb2544da6bfbf64ce6632e1b638d795d6445a9579a9`  
		Last Modified: Fri, 18 Dec 2020 19:59:34 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6745c3a6d506a5e0128a176d39e1101562ddceb8cdb582ded9962bd4715d89`  
		Last Modified: Fri, 18 Dec 2020 19:59:34 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:2de9f439cf4e35d9adfe9e5646d9f7f219486364e7ccd496ac885fba16860d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:43e201b148306ab5dd7ac08610b3ae26e5f1a9846c6100254c4b92d0490ac43a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386283878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2207ad6c420e3b3e1a2e75919afbbd8c8b0d875f4937db30abe58355f215dde2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:20:10 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:20:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:20:26 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:20:27 GMT
ENV ODOO_VERSION=13.0
# Fri, 18 Dec 2020 19:54:54 GMT
ARG ODOO_RELEASE=20201218
# Fri, 18 Dec 2020 19:54:54 GMT
ARG ODOO_SHA=44cff0f8fe5b54cdf7887c388dccf7d462790ccc
# Fri, 18 Dec 2020 19:55:53 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=44cff0f8fe5b54cdf7887c388dccf7d462790ccc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Dec 2020 19:55:55 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Dec 2020 19:55:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Dec 2020 19:55:56 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=44cff0f8fe5b54cdf7887c388dccf7d462790ccc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Dec 2020 19:55:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Dec 2020 19:55:56 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Dec 2020 19:55:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Dec 2020 19:55:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Dec 2020 19:55:57 GMT
USER odoo
# Fri, 18 Dec 2020 19:55:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Dec 2020 19:55:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d85901c4050548f6d6f629e8fb1ae22d74aba09c4f622fa69c57c40128bed5`  
		Last Modified: Fri, 11 Dec 2020 17:27:04 GMT  
		Size: 207.1 MB (207077357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e6fcfad7aecb0170d1af106384e043637b3d5f6b51e1fe4f69519e772fe2f`  
		Last Modified: Fri, 11 Dec 2020 17:26:22 GMT  
		Size: 2.3 MB (2343918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681e2f39973b063caa7a47829a5d8bb6cc6a404aeb719d5ffd7974ab79630330`  
		Last Modified: Fri, 11 Dec 2020 17:26:22 GMT  
		Size: 927.4 KB (927358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281bd27eb1f02a310002b952c465a0c7bac22a160ed0a215577534cccd5220cc`  
		Last Modified: Fri, 18 Dec 2020 19:59:28 GMT  
		Size: 148.8 MB (148833548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1292264587e55cbcae3b6e6a7b1f0703f3d7508812f35921583a69768b9c5c2a`  
		Last Modified: Fri, 18 Dec 2020 19:58:53 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aef1c18c2b9723fa466628c9dcf8823795fe58b711cecd8446e9338aa44e58`  
		Last Modified: Fri, 18 Dec 2020 19:58:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081823ff960ce21fe5dc47036527f998e1c50abdaeab4046f484e244918432f7`  
		Last Modified: Fri, 18 Dec 2020 19:58:53 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf3b172cae56819da784c3b83b997cad1817c77d4817b88d4fe1ac5db9aeda4`  
		Last Modified: Fri, 18 Dec 2020 19:58:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:2de9f439cf4e35d9adfe9e5646d9f7f219486364e7ccd496ac885fba16860d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:43e201b148306ab5dd7ac08610b3ae26e5f1a9846c6100254c4b92d0490ac43a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386283878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2207ad6c420e3b3e1a2e75919afbbd8c8b0d875f4937db30abe58355f215dde2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:20:10 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:20:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:20:26 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:20:27 GMT
ENV ODOO_VERSION=13.0
# Fri, 18 Dec 2020 19:54:54 GMT
ARG ODOO_RELEASE=20201218
# Fri, 18 Dec 2020 19:54:54 GMT
ARG ODOO_SHA=44cff0f8fe5b54cdf7887c388dccf7d462790ccc
# Fri, 18 Dec 2020 19:55:53 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=44cff0f8fe5b54cdf7887c388dccf7d462790ccc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Dec 2020 19:55:55 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Dec 2020 19:55:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Dec 2020 19:55:56 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=44cff0f8fe5b54cdf7887c388dccf7d462790ccc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Dec 2020 19:55:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Dec 2020 19:55:56 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Dec 2020 19:55:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Dec 2020 19:55:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Dec 2020 19:55:57 GMT
USER odoo
# Fri, 18 Dec 2020 19:55:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Dec 2020 19:55:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d85901c4050548f6d6f629e8fb1ae22d74aba09c4f622fa69c57c40128bed5`  
		Last Modified: Fri, 11 Dec 2020 17:27:04 GMT  
		Size: 207.1 MB (207077357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e6fcfad7aecb0170d1af106384e043637b3d5f6b51e1fe4f69519e772fe2f`  
		Last Modified: Fri, 11 Dec 2020 17:26:22 GMT  
		Size: 2.3 MB (2343918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681e2f39973b063caa7a47829a5d8bb6cc6a404aeb719d5ffd7974ab79630330`  
		Last Modified: Fri, 11 Dec 2020 17:26:22 GMT  
		Size: 927.4 KB (927358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281bd27eb1f02a310002b952c465a0c7bac22a160ed0a215577534cccd5220cc`  
		Last Modified: Fri, 18 Dec 2020 19:59:28 GMT  
		Size: 148.8 MB (148833548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1292264587e55cbcae3b6e6a7b1f0703f3d7508812f35921583a69768b9c5c2a`  
		Last Modified: Fri, 18 Dec 2020 19:58:53 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aef1c18c2b9723fa466628c9dcf8823795fe58b711cecd8446e9338aa44e58`  
		Last Modified: Fri, 18 Dec 2020 19:58:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081823ff960ce21fe5dc47036527f998e1c50abdaeab4046f484e244918432f7`  
		Last Modified: Fri, 18 Dec 2020 19:58:53 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf3b172cae56819da784c3b83b997cad1817c77d4817b88d4fe1ac5db9aeda4`  
		Last Modified: Fri, 18 Dec 2020 19:58:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:081f8846546ce60f354ec74156acccd673f7b66ad42bbf2a337bec30f7431591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:1a8827774caab07a37eb451014585f9574070da3ec65044746960e513564e013
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.3 MB (404278250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c34e85682c0eec6617af427f7838e9849f21f92a3a240255e0b400c8f4b94d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:17:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:17:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:17:16 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:17:16 GMT
ENV ODOO_VERSION=14.0
# Fri, 18 Dec 2020 19:53:49 GMT
ARG ODOO_RELEASE=20201218
# Fri, 18 Dec 2020 19:53:49 GMT
ARG ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
# Fri, 18 Dec 2020 19:54:43 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Dec 2020 19:54:44 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Dec 2020 19:54:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Dec 2020 19:54:45 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Dec 2020 19:54:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Dec 2020 19:54:46 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Dec 2020 19:54:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Dec 2020 19:54:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Dec 2020 19:54:46 GMT
USER odoo
# Fri, 18 Dec 2020 19:54:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Dec 2020 19:54:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bc76188888637b8d6d4343790322715f6ff67e2f556d95ba4007bba46aa4b4`  
		Last Modified: Fri, 11 Dec 2020 17:26:02 GMT  
		Size: 213.1 MB (213118166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1489eaa0a91c1579cd0b86042b35ce651421b6d4be8baac3ff6f5e28fc88b423`  
		Last Modified: Fri, 11 Dec 2020 17:25:21 GMT  
		Size: 2.3 MB (2346249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8179dcb4a5c98894d38fdcf9748cbea2ad22a70c2b85c8118ca1f2f23e42afe1`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 927.4 KB (927408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec16a7fdd6e0c0f407e3a27fd4cb3d411dbe897989b90e72943f3091c66ddb`  
		Last Modified: Fri, 18 Dec 2020 19:58:46 GMT  
		Size: 160.8 MB (160784729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0ea39d8e51a8daab3dc808a07ffe67161edb7a0a1047941222f9c49578883f`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00114de53a4a62fd509ac73e7c124f80043fab355f6ddfeb8544e3efbd8ee3aa`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c6820d46466f592923c1348b44496861a049aefdbcea8d87c4979dddd7160c`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14f21a099442af06b1adb9bfbb4cb6dd7eeef006b4ca1bf13184da39fe5ac34`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:081f8846546ce60f354ec74156acccd673f7b66ad42bbf2a337bec30f7431591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:1a8827774caab07a37eb451014585f9574070da3ec65044746960e513564e013
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.3 MB (404278250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c34e85682c0eec6617af427f7838e9849f21f92a3a240255e0b400c8f4b94d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:17:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:17:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:17:16 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:17:16 GMT
ENV ODOO_VERSION=14.0
# Fri, 18 Dec 2020 19:53:49 GMT
ARG ODOO_RELEASE=20201218
# Fri, 18 Dec 2020 19:53:49 GMT
ARG ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
# Fri, 18 Dec 2020 19:54:43 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Dec 2020 19:54:44 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Dec 2020 19:54:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Dec 2020 19:54:45 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Dec 2020 19:54:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Dec 2020 19:54:46 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Dec 2020 19:54:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Dec 2020 19:54:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Dec 2020 19:54:46 GMT
USER odoo
# Fri, 18 Dec 2020 19:54:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Dec 2020 19:54:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bc76188888637b8d6d4343790322715f6ff67e2f556d95ba4007bba46aa4b4`  
		Last Modified: Fri, 11 Dec 2020 17:26:02 GMT  
		Size: 213.1 MB (213118166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1489eaa0a91c1579cd0b86042b35ce651421b6d4be8baac3ff6f5e28fc88b423`  
		Last Modified: Fri, 11 Dec 2020 17:25:21 GMT  
		Size: 2.3 MB (2346249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8179dcb4a5c98894d38fdcf9748cbea2ad22a70c2b85c8118ca1f2f23e42afe1`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 927.4 KB (927408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec16a7fdd6e0c0f407e3a27fd4cb3d411dbe897989b90e72943f3091c66ddb`  
		Last Modified: Fri, 18 Dec 2020 19:58:46 GMT  
		Size: 160.8 MB (160784729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0ea39d8e51a8daab3dc808a07ffe67161edb7a0a1047941222f9c49578883f`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00114de53a4a62fd509ac73e7c124f80043fab355f6ddfeb8544e3efbd8ee3aa`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c6820d46466f592923c1348b44496861a049aefdbcea8d87c4979dddd7160c`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14f21a099442af06b1adb9bfbb4cb6dd7eeef006b4ca1bf13184da39fe5ac34`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:081f8846546ce60f354ec74156acccd673f7b66ad42bbf2a337bec30f7431591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:1a8827774caab07a37eb451014585f9574070da3ec65044746960e513564e013
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.3 MB (404278250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c34e85682c0eec6617af427f7838e9849f21f92a3a240255e0b400c8f4b94d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 11 Dec 2020 17:15:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 11 Dec 2020 17:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:17:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 11 Dec 2020 17:17:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:17:16 GMT
RUN npm install -g rtlcss
# Fri, 11 Dec 2020 17:17:16 GMT
ENV ODOO_VERSION=14.0
# Fri, 18 Dec 2020 19:53:49 GMT
ARG ODOO_RELEASE=20201218
# Fri, 18 Dec 2020 19:53:49 GMT
ARG ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
# Fri, 18 Dec 2020 19:54:43 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 18 Dec 2020 19:54:44 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 18 Dec 2020 19:54:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 18 Dec 2020 19:54:45 GMT
# ARGS: ODOO_RELEASE=20201218 ODOO_SHA=cd893ce96b3bf7e3448f2414f4537685f521acd8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 18 Dec 2020 19:54:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 18 Dec 2020 19:54:46 GMT
EXPOSE 8069 8071 8072
# Fri, 18 Dec 2020 19:54:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 18 Dec 2020 19:54:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 18 Dec 2020 19:54:46 GMT
USER odoo
# Fri, 18 Dec 2020 19:54:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Dec 2020 19:54:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bc76188888637b8d6d4343790322715f6ff67e2f556d95ba4007bba46aa4b4`  
		Last Modified: Fri, 11 Dec 2020 17:26:02 GMT  
		Size: 213.1 MB (213118166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1489eaa0a91c1579cd0b86042b35ce651421b6d4be8baac3ff6f5e28fc88b423`  
		Last Modified: Fri, 11 Dec 2020 17:25:21 GMT  
		Size: 2.3 MB (2346249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8179dcb4a5c98894d38fdcf9748cbea2ad22a70c2b85c8118ca1f2f23e42afe1`  
		Last Modified: Fri, 11 Dec 2020 17:25:19 GMT  
		Size: 927.4 KB (927408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec16a7fdd6e0c0f407e3a27fd4cb3d411dbe897989b90e72943f3091c66ddb`  
		Last Modified: Fri, 18 Dec 2020 19:58:46 GMT  
		Size: 160.8 MB (160784729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0ea39d8e51a8daab3dc808a07ffe67161edb7a0a1047941222f9c49578883f`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00114de53a4a62fd509ac73e7c124f80043fab355f6ddfeb8544e3efbd8ee3aa`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c6820d46466f592923c1348b44496861a049aefdbcea8d87c4979dddd7160c`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14f21a099442af06b1adb9bfbb4cb6dd7eeef006b4ca1bf13184da39fe5ac34`  
		Last Modified: Fri, 18 Dec 2020 19:57:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
