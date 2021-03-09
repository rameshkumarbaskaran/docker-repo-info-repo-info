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
$ docker pull odoo@sha256:87e6aa0f34b7d44e0a7cc0dbd4a51f1a5849f9c959628054436ee2e598b91165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:2eac26a8b85099f73ce84307bf4585810a90d2efdb441210d3156a68c5231f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542518667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0e33d4ca671fcbb6077b500bc2b7cc2ea8e2ceaa096004a47df95b20105db5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 00:29:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Mar 2021 00:29:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Mar 2021 00:29:10 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 00:29:12 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Mar 2021 00:30:33 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Mar 2021 00:30:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 00:30:56 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 00:30:56 GMT
ENV ODOO_VERSION=12.0
# Tue, 09 Mar 2021 00:30:56 GMT
ARG ODOO_RELEASE=20210308
# Tue, 09 Mar 2021 00:30:56 GMT
ARG ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
# Tue, 09 Mar 2021 00:31:58 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Mar 2021 00:32:00 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Mar 2021 00:32:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Mar 2021 00:32:01 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Mar 2021 00:32:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Mar 2021 00:32:01 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Mar 2021 00:32:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Mar 2021 00:32:02 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Mar 2021 00:32:02 GMT
USER odoo
# Tue, 09 Mar 2021 00:32:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Mar 2021 00:32:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bce4654d1660dce28713090b95cceaabd1dc320ac253c15bf6e4b3493d105`  
		Last Modified: Tue, 09 Mar 2021 00:34:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971a9fa7df8c61caaa7b41560ac127134c9103bca96cc2f50559c94de5a81ed0`  
		Last Modified: Tue, 09 Mar 2021 00:34:37 GMT  
		Size: 219.6 MB (219626143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fab37c8ae7265109453608e11ba79adb95fad77c711ff221fa71ffe379768d`  
		Last Modified: Tue, 09 Mar 2021 00:34:11 GMT  
		Size: 2.2 MB (2224036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3192e1fdbf89363e809a023303bafc1ee31e0c7700e3b7744e1ae29f6fb591f7`  
		Last Modified: Tue, 09 Mar 2021 00:34:16 GMT  
		Size: 22.1 MB (22055830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeb16121f05a52e51bc6a021955918025676e4b794a04be01ff00c3acd8ba6e`  
		Last Modified: Tue, 09 Mar 2021 00:34:42 GMT  
		Size: 276.1 MB (276081399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2dad43f81f509d99f8191b7a5880a3e4f459b72782fe34f8b0cf9d819eba37`  
		Last Modified: Tue, 09 Mar 2021 00:34:08 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08d398037a6e9ed8d41c108c358c693d9ed5672241a52b193ddb61c9d95284b`  
		Last Modified: Tue, 09 Mar 2021 00:34:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6841bc0e984ba650f798510d8bbdf886727de923a991feb667d030b79a7b66`  
		Last Modified: Tue, 09 Mar 2021 00:34:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a41ecb5d9397f8c35305fa7237744066314a8921c9712bc7120ba77bd282c`  
		Last Modified: Tue, 09 Mar 2021 00:34:08 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:87e6aa0f34b7d44e0a7cc0dbd4a51f1a5849f9c959628054436ee2e598b91165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:2eac26a8b85099f73ce84307bf4585810a90d2efdb441210d3156a68c5231f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542518667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0e33d4ca671fcbb6077b500bc2b7cc2ea8e2ceaa096004a47df95b20105db5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 00:29:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Mar 2021 00:29:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Mar 2021 00:29:10 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 00:29:12 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Mar 2021 00:30:33 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Mar 2021 00:30:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 00:30:56 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 00:30:56 GMT
ENV ODOO_VERSION=12.0
# Tue, 09 Mar 2021 00:30:56 GMT
ARG ODOO_RELEASE=20210308
# Tue, 09 Mar 2021 00:30:56 GMT
ARG ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
# Tue, 09 Mar 2021 00:31:58 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Mar 2021 00:32:00 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Mar 2021 00:32:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Mar 2021 00:32:01 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Mar 2021 00:32:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Mar 2021 00:32:01 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Mar 2021 00:32:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Mar 2021 00:32:02 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Mar 2021 00:32:02 GMT
USER odoo
# Tue, 09 Mar 2021 00:32:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Mar 2021 00:32:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bce4654d1660dce28713090b95cceaabd1dc320ac253c15bf6e4b3493d105`  
		Last Modified: Tue, 09 Mar 2021 00:34:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971a9fa7df8c61caaa7b41560ac127134c9103bca96cc2f50559c94de5a81ed0`  
		Last Modified: Tue, 09 Mar 2021 00:34:37 GMT  
		Size: 219.6 MB (219626143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fab37c8ae7265109453608e11ba79adb95fad77c711ff221fa71ffe379768d`  
		Last Modified: Tue, 09 Mar 2021 00:34:11 GMT  
		Size: 2.2 MB (2224036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3192e1fdbf89363e809a023303bafc1ee31e0c7700e3b7744e1ae29f6fb591f7`  
		Last Modified: Tue, 09 Mar 2021 00:34:16 GMT  
		Size: 22.1 MB (22055830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeb16121f05a52e51bc6a021955918025676e4b794a04be01ff00c3acd8ba6e`  
		Last Modified: Tue, 09 Mar 2021 00:34:42 GMT  
		Size: 276.1 MB (276081399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2dad43f81f509d99f8191b7a5880a3e4f459b72782fe34f8b0cf9d819eba37`  
		Last Modified: Tue, 09 Mar 2021 00:34:08 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08d398037a6e9ed8d41c108c358c693d9ed5672241a52b193ddb61c9d95284b`  
		Last Modified: Tue, 09 Mar 2021 00:34:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6841bc0e984ba650f798510d8bbdf886727de923a991feb667d030b79a7b66`  
		Last Modified: Tue, 09 Mar 2021 00:34:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a41ecb5d9397f8c35305fa7237744066314a8921c9712bc7120ba77bd282c`  
		Last Modified: Tue, 09 Mar 2021 00:34:08 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:a22c20a4cb3c9c94f67c1757fd99f4ea97a515155845b5670e5c387444b26c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:1bed6d295125fa41abb1e9dee974291af06e88133122ee432664f7eaa90ca90e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532160975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23038f81ad46a12bd58a6b68782187136e77f18d44ea6c03521fbcd1fa6379f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 00:23:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Mar 2021 00:23:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Mar 2021 00:23:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 00:27:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Mar 2021 00:27:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 00:27:50 GMT
RUN npm install -g rtlcss
# Tue, 09 Mar 2021 00:27:50 GMT
ENV ODOO_VERSION=13.0
# Tue, 09 Mar 2021 00:27:50 GMT
ARG ODOO_RELEASE=20210308
# Tue, 09 Mar 2021 00:27:50 GMT
ARG ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
# Tue, 09 Mar 2021 00:28:58 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Mar 2021 00:29:02 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Mar 2021 00:29:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Mar 2021 00:29:03 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Mar 2021 00:29:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Mar 2021 00:29:04 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Mar 2021 00:29:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Mar 2021 00:29:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Mar 2021 00:29:04 GMT
USER odoo
# Tue, 09 Mar 2021 00:29:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Mar 2021 00:29:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6228742a35e385b4b27a11beb8d0531c42faf730e4785d688b293b21788b1c`  
		Last Modified: Tue, 09 Mar 2021 00:33:45 GMT  
		Size: 207.1 MB (207118879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1655ff6dab5aff52f5ed68399b3645b7e5c4ec3c583af1bd27279108f8191`  
		Last Modified: Tue, 09 Mar 2021 00:33:17 GMT  
		Size: 2.3 MB (2345224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cefaf0b83c6cfeda9d497a36c353dfc19ebc8b22a4aaf5cb32bebdda729058b`  
		Last Modified: Tue, 09 Mar 2021 00:33:17 GMT  
		Size: 910.7 KB (910677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eecc5948dbdaf9ed986a8a93f5bc6c5d96a5dc7e9f0a4464be3e558805334c`  
		Last Modified: Tue, 09 Mar 2021 00:33:50 GMT  
		Size: 294.7 MB (294688626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd36ac0b945d7c4f8046effeab54f49ee22cf6f32f9b856a92ebad2e61e661b`  
		Last Modified: Tue, 09 Mar 2021 00:33:14 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02146ea82e13cb943d13f370616b64a06ea79ff393aa922d5b6f91c57145ea41`  
		Last Modified: Tue, 09 Mar 2021 00:33:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bff17b6bd218934634881fb13d412f0d707c9447e3ee05c780b770d0ca532d`  
		Last Modified: Tue, 09 Mar 2021 00:33:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cc36e5ec162a7357656db49e67adaad363cc7980c6ba2717437ad372c27ae`  
		Last Modified: Tue, 09 Mar 2021 00:33:14 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:a22c20a4cb3c9c94f67c1757fd99f4ea97a515155845b5670e5c387444b26c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:1bed6d295125fa41abb1e9dee974291af06e88133122ee432664f7eaa90ca90e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532160975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23038f81ad46a12bd58a6b68782187136e77f18d44ea6c03521fbcd1fa6379f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 00:23:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Mar 2021 00:23:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Mar 2021 00:23:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 00:27:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Mar 2021 00:27:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 00:27:50 GMT
RUN npm install -g rtlcss
# Tue, 09 Mar 2021 00:27:50 GMT
ENV ODOO_VERSION=13.0
# Tue, 09 Mar 2021 00:27:50 GMT
ARG ODOO_RELEASE=20210308
# Tue, 09 Mar 2021 00:27:50 GMT
ARG ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
# Tue, 09 Mar 2021 00:28:58 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Mar 2021 00:29:02 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Mar 2021 00:29:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Mar 2021 00:29:03 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Mar 2021 00:29:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Mar 2021 00:29:04 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Mar 2021 00:29:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Mar 2021 00:29:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Mar 2021 00:29:04 GMT
USER odoo
# Tue, 09 Mar 2021 00:29:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Mar 2021 00:29:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6228742a35e385b4b27a11beb8d0531c42faf730e4785d688b293b21788b1c`  
		Last Modified: Tue, 09 Mar 2021 00:33:45 GMT  
		Size: 207.1 MB (207118879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a1655ff6dab5aff52f5ed68399b3645b7e5c4ec3c583af1bd27279108f8191`  
		Last Modified: Tue, 09 Mar 2021 00:33:17 GMT  
		Size: 2.3 MB (2345224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cefaf0b83c6cfeda9d497a36c353dfc19ebc8b22a4aaf5cb32bebdda729058b`  
		Last Modified: Tue, 09 Mar 2021 00:33:17 GMT  
		Size: 910.7 KB (910677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eecc5948dbdaf9ed986a8a93f5bc6c5d96a5dc7e9f0a4464be3e558805334c`  
		Last Modified: Tue, 09 Mar 2021 00:33:50 GMT  
		Size: 294.7 MB (294688626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd36ac0b945d7c4f8046effeab54f49ee22cf6f32f9b856a92ebad2e61e661b`  
		Last Modified: Tue, 09 Mar 2021 00:33:14 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02146ea82e13cb943d13f370616b64a06ea79ff393aa922d5b6f91c57145ea41`  
		Last Modified: Tue, 09 Mar 2021 00:33:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bff17b6bd218934634881fb13d412f0d707c9447e3ee05c780b770d0ca532d`  
		Last Modified: Tue, 09 Mar 2021 00:33:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cc36e5ec162a7357656db49e67adaad363cc7980c6ba2717437ad372c27ae`  
		Last Modified: Tue, 09 Mar 2021 00:33:14 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:6b557be0d514f70a3d9b47b3971e1ace74d13357fd5f0481ad30f2a5287b7e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:8b0dd2b6e7a62217068d08621e235f60ab5cd49c8ff702f6e0df7043eb1e11b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515256024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb8bd5827fc83870a0559f973d62906b39ffb614f859b59492fa66f48c47190`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 00:23:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Mar 2021 00:23:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Mar 2021 00:23:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 00:24:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Mar 2021 00:25:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 00:25:16 GMT
RUN npm install -g rtlcss
# Tue, 09 Mar 2021 00:25:16 GMT
ENV ODOO_VERSION=14.0
# Tue, 09 Mar 2021 00:25:16 GMT
ARG ODOO_RELEASE=20210308
# Tue, 09 Mar 2021 00:25:17 GMT
ARG ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
# Tue, 09 Mar 2021 00:26:23 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Mar 2021 00:26:27 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Mar 2021 00:26:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Mar 2021 00:26:28 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Mar 2021 00:26:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Mar 2021 00:26:29 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Mar 2021 00:26:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Mar 2021 00:26:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Mar 2021 00:26:29 GMT
USER odoo
# Tue, 09 Mar 2021 00:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Mar 2021 00:26:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f561c16e63035f970ee569dc4fc25d3b85a9402e20fd396d50544d5e04a174`  
		Last Modified: Tue, 09 Mar 2021 00:32:54 GMT  
		Size: 213.2 MB (213158835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6ae58262de86c70fad19033bed3d6af2d5baf6f3d1db65ab3b65b2525782f2`  
		Last Modified: Tue, 09 Mar 2021 00:32:24 GMT  
		Size: 2.3 MB (2348356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebfbb16cdef14db39a68b17b59e9565955d9da46878215e99f89ebbdb0b2254`  
		Last Modified: Tue, 09 Mar 2021 00:32:24 GMT  
		Size: 910.4 KB (910391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b51e5f91c2c1a6b3b35c30a2deb9c84af1fd739c0f92e71cd996922e66edbb`  
		Last Modified: Tue, 09 Mar 2021 00:32:58 GMT  
		Size: 271.7 MB (271740873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b262a287d8514503210e5fe91d4e2a84d3677d7d78306753798c64324c4ddb8`  
		Last Modified: Tue, 09 Mar 2021 00:32:22 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3fe986655ca2149d637d9b5b62bbf0ddddb521a4e4d3f7bf2e4ede98ef8b81`  
		Last Modified: Tue, 09 Mar 2021 00:32:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0394ea30588922a5f7dbdcd2cb1bf2feb4db2df7a499fcd309212f2ec3d3ecd3`  
		Last Modified: Tue, 09 Mar 2021 00:32:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc326a4b530b9d3902489293a3a902394cb1ecab6ee8a011a27045eec77d130f`  
		Last Modified: Tue, 09 Mar 2021 00:32:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:6b557be0d514f70a3d9b47b3971e1ace74d13357fd5f0481ad30f2a5287b7e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:8b0dd2b6e7a62217068d08621e235f60ab5cd49c8ff702f6e0df7043eb1e11b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515256024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb8bd5827fc83870a0559f973d62906b39ffb614f859b59492fa66f48c47190`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 00:23:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Mar 2021 00:23:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Mar 2021 00:23:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 00:24:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Mar 2021 00:25:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 00:25:16 GMT
RUN npm install -g rtlcss
# Tue, 09 Mar 2021 00:25:16 GMT
ENV ODOO_VERSION=14.0
# Tue, 09 Mar 2021 00:25:16 GMT
ARG ODOO_RELEASE=20210308
# Tue, 09 Mar 2021 00:25:17 GMT
ARG ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
# Tue, 09 Mar 2021 00:26:23 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Mar 2021 00:26:27 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Mar 2021 00:26:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Mar 2021 00:26:28 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Mar 2021 00:26:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Mar 2021 00:26:29 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Mar 2021 00:26:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Mar 2021 00:26:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Mar 2021 00:26:29 GMT
USER odoo
# Tue, 09 Mar 2021 00:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Mar 2021 00:26:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f561c16e63035f970ee569dc4fc25d3b85a9402e20fd396d50544d5e04a174`  
		Last Modified: Tue, 09 Mar 2021 00:32:54 GMT  
		Size: 213.2 MB (213158835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6ae58262de86c70fad19033bed3d6af2d5baf6f3d1db65ab3b65b2525782f2`  
		Last Modified: Tue, 09 Mar 2021 00:32:24 GMT  
		Size: 2.3 MB (2348356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebfbb16cdef14db39a68b17b59e9565955d9da46878215e99f89ebbdb0b2254`  
		Last Modified: Tue, 09 Mar 2021 00:32:24 GMT  
		Size: 910.4 KB (910391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b51e5f91c2c1a6b3b35c30a2deb9c84af1fd739c0f92e71cd996922e66edbb`  
		Last Modified: Tue, 09 Mar 2021 00:32:58 GMT  
		Size: 271.7 MB (271740873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b262a287d8514503210e5fe91d4e2a84d3677d7d78306753798c64324c4ddb8`  
		Last Modified: Tue, 09 Mar 2021 00:32:22 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3fe986655ca2149d637d9b5b62bbf0ddddb521a4e4d3f7bf2e4ede98ef8b81`  
		Last Modified: Tue, 09 Mar 2021 00:32:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0394ea30588922a5f7dbdcd2cb1bf2feb4db2df7a499fcd309212f2ec3d3ecd3`  
		Last Modified: Tue, 09 Mar 2021 00:32:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc326a4b530b9d3902489293a3a902394cb1ecab6ee8a011a27045eec77d130f`  
		Last Modified: Tue, 09 Mar 2021 00:32:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:6b557be0d514f70a3d9b47b3971e1ace74d13357fd5f0481ad30f2a5287b7e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:8b0dd2b6e7a62217068d08621e235f60ab5cd49c8ff702f6e0df7043eb1e11b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515256024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb8bd5827fc83870a0559f973d62906b39ffb614f859b59492fa66f48c47190`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 00:23:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Mar 2021 00:23:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Mar 2021 00:23:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 00:24:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Mar 2021 00:25:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 00:25:16 GMT
RUN npm install -g rtlcss
# Tue, 09 Mar 2021 00:25:16 GMT
ENV ODOO_VERSION=14.0
# Tue, 09 Mar 2021 00:25:16 GMT
ARG ODOO_RELEASE=20210308
# Tue, 09 Mar 2021 00:25:17 GMT
ARG ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
# Tue, 09 Mar 2021 00:26:23 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Mar 2021 00:26:27 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Mar 2021 00:26:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Mar 2021 00:26:28 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Mar 2021 00:26:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Mar 2021 00:26:29 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Mar 2021 00:26:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Mar 2021 00:26:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Mar 2021 00:26:29 GMT
USER odoo
# Tue, 09 Mar 2021 00:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Mar 2021 00:26:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f561c16e63035f970ee569dc4fc25d3b85a9402e20fd396d50544d5e04a174`  
		Last Modified: Tue, 09 Mar 2021 00:32:54 GMT  
		Size: 213.2 MB (213158835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6ae58262de86c70fad19033bed3d6af2d5baf6f3d1db65ab3b65b2525782f2`  
		Last Modified: Tue, 09 Mar 2021 00:32:24 GMT  
		Size: 2.3 MB (2348356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebfbb16cdef14db39a68b17b59e9565955d9da46878215e99f89ebbdb0b2254`  
		Last Modified: Tue, 09 Mar 2021 00:32:24 GMT  
		Size: 910.4 KB (910391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b51e5f91c2c1a6b3b35c30a2deb9c84af1fd739c0f92e71cd996922e66edbb`  
		Last Modified: Tue, 09 Mar 2021 00:32:58 GMT  
		Size: 271.7 MB (271740873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b262a287d8514503210e5fe91d4e2a84d3677d7d78306753798c64324c4ddb8`  
		Last Modified: Tue, 09 Mar 2021 00:32:22 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3fe986655ca2149d637d9b5b62bbf0ddddb521a4e4d3f7bf2e4ede98ef8b81`  
		Last Modified: Tue, 09 Mar 2021 00:32:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0394ea30588922a5f7dbdcd2cb1bf2feb4db2df7a499fcd309212f2ec3d3ecd3`  
		Last Modified: Tue, 09 Mar 2021 00:32:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc326a4b530b9d3902489293a3a902394cb1ecab6ee8a011a27045eec77d130f`  
		Last Modified: Tue, 09 Mar 2021 00:32:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
