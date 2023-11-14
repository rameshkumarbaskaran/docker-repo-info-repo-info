<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:59f8897974c973ee284af1693b311886989ca50704c170842f17345ad130e1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:ed3a88ca1f9bb776bfde513bfdedfbbaedc6959abb48ea489d4ff1348acbf74b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563007841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90460214e99cf5875217bd329f5fd1cb889bebd78f175d5d8faf1b2e20292bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 12:03:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Nov 2023 12:04:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 12:04:04 GMT
RUN npm install -g rtlcss
# Wed, 01 Nov 2023 12:04:04 GMT
ENV ODOO_VERSION=15.0
# Wed, 08 Nov 2023 00:42:03 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:42:03 GMT
ARG ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
# Wed, 08 Nov 2023 00:43:16 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:43:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:43:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:43:21 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:43:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:43:21 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:43:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:43:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:43:21 GMT
USER odoo
# Wed, 08 Nov 2023 00:43:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:43:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae4769061fca067a25d337753a857c225301a3391d70dc9c355ec401a1666f9`  
		Last Modified: Wed, 01 Nov 2023 12:09:44 GMT  
		Size: 220.3 MB (220298628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037b076bdf88bd13eb93037e412a84af9179318c033537325a2abb0e21f3437`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 2.6 MB (2624848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09c8bae1e450f33859e0454685d8e83ce199230cdf0487f7b3bca45bccd8a66`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 457.9 KB (457875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6818025799f187b915cf97bc1ac4ddb67a106c478369d5261f233135773734ff`  
		Last Modified: Wed, 08 Nov 2023 00:46:19 GMT  
		Size: 308.2 MB (308206110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9979448ed0ddebc713bddd4719b4941de3c33f6800e2c89f0bcbb7d676e0f96`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae54e00a1e53b4da2bf462000389824becf5ed078fd5667d16bf74a0140aad94`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7209289209c2a643bf58c06e90725e0364c37ec2cb5eebc700aedd075d1589`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9ea5daa95395c0a47e181fcbd6e39d7058e1e42a22122b4c4e25fccc0a5df8`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:59f8897974c973ee284af1693b311886989ca50704c170842f17345ad130e1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:ed3a88ca1f9bb776bfde513bfdedfbbaedc6959abb48ea489d4ff1348acbf74b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563007841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90460214e99cf5875217bd329f5fd1cb889bebd78f175d5d8faf1b2e20292bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 12:03:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Nov 2023 12:04:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 12:04:04 GMT
RUN npm install -g rtlcss
# Wed, 01 Nov 2023 12:04:04 GMT
ENV ODOO_VERSION=15.0
# Wed, 08 Nov 2023 00:42:03 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:42:03 GMT
ARG ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
# Wed, 08 Nov 2023 00:43:16 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:43:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:43:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:43:21 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:43:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:43:21 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:43:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:43:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:43:21 GMT
USER odoo
# Wed, 08 Nov 2023 00:43:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:43:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae4769061fca067a25d337753a857c225301a3391d70dc9c355ec401a1666f9`  
		Last Modified: Wed, 01 Nov 2023 12:09:44 GMT  
		Size: 220.3 MB (220298628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037b076bdf88bd13eb93037e412a84af9179318c033537325a2abb0e21f3437`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 2.6 MB (2624848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09c8bae1e450f33859e0454685d8e83ce199230cdf0487f7b3bca45bccd8a66`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 457.9 KB (457875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6818025799f187b915cf97bc1ac4ddb67a106c478369d5261f233135773734ff`  
		Last Modified: Wed, 08 Nov 2023 00:46:19 GMT  
		Size: 308.2 MB (308206110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9979448ed0ddebc713bddd4719b4941de3c33f6800e2c89f0bcbb7d676e0f96`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae54e00a1e53b4da2bf462000389824becf5ed078fd5667d16bf74a0140aad94`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7209289209c2a643bf58c06e90725e0364c37ec2cb5eebc700aedd075d1589`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9ea5daa95395c0a47e181fcbd6e39d7058e1e42a22122b4c4e25fccc0a5df8`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:b02db1a3a5207ec2dee2245d8321b1a510682fd1a8c617f18314b14eba883fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:050d6909f19797b0113b195dac076d9f9e9d48906c8a9c00b017d4a3162b2f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.1 MB (577148541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e4063887fdfe4a2ffda6523576bbcd058e1040f9a000d336d84f9d7e0c77d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:38:54 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:40:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:40:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:40:19 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:40:19 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:41:41 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:41:45 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:41:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:41:45 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:41:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:41:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:41:46 GMT
USER odoo
# Wed, 08 Nov 2023 00:41:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:41:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3abf7b1c0fb11700caf26b92dbcf9281f5ee88bb7be113dd51e1237f1c4b8`  
		Last Modified: Wed, 08 Nov 2023 00:45:23 GMT  
		Size: 219.6 MB (219607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e024eac15856bbec7f25f475d3c1810249d92b2608024fd861df2de7af7dd`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 2.6 MB (2628109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eee1f11dc9d1c4617dcf3d9bf6d5368df3304931f6c41b3318eb2bf05ef1605`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 459.5 KB (459516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c3322fe74239122fed63bc5d7c0ad8426f1f64b70f8605a7d9bc76b24731bc`  
		Last Modified: Wed, 08 Nov 2023 00:45:34 GMT  
		Size: 323.0 MB (323033428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790686c1cd5cc1e7e382ab129cd19542d38167c0f49b12d62fc499162ba3034b`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e3a6dcb28c4c6bfc8b69508a4e912cfb0d4ccfb03691c3aa654da8b0e4238f`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f8d088b6082f21385081c583e38925e485c4cf273eea4611d603a9c4c5b505`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ddc13242fd0b2e64c6f399370d12edda33f930841d1d805eaf93eba5341c38`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:26c2150d81e20760d93ea2ef38be3c2823814e2ae83382173d68de066426d911
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572792791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015469bef4a58eaa7b4390f7619903866e1a48f66afe18a8b2f3f56aca54fc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 07 Nov 2023 23:48:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Nov 2023 23:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Nov 2023 23:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Nov 2023 23:48:30 GMT
ARG TARGETARCH
# Tue, 07 Nov 2023 23:49:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 07 Nov 2023 23:49:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Nov 2023 23:49:48 GMT
RUN npm install -g rtlcss
# Tue, 07 Nov 2023 23:49:48 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 Nov 2023 00:56:03 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:56:03 GMT
ARG ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
# Tue, 14 Nov 2023 00:57:15 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:57:22 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:57:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:57:22 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:57:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:57:22 GMT
USER odoo
# Tue, 14 Nov 2023 00:57:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:57:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5812a002d612ea362d56834609da19cbf53fb331e9f92b0b4b8d1cdd3b8aa9`  
		Last Modified: Tue, 07 Nov 2023 23:51:50 GMT  
		Size: 216.9 MB (216907690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59eaf6b2e981344b7a4bf54a869a293a9e69d429da23202eed603c8f1f41835`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 2.6 MB (2634000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2aeeb4414cf9678f9200a368d1873d1290880b10ec32b5a9264ae836d479b`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 459.4 KB (459450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdf05cdc5b9b591787678961a1ec1aec071c1057eed23c306d8c0040718da8e`  
		Last Modified: Tue, 14 Nov 2023 00:58:44 GMT  
		Size: 322.7 MB (322725284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b14bf046a1e125c9aac7baff7af0f75345f5268208d4912f510efa3bf78ca1`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0bf7919c61b58c943d6cc0bc1f5767a8b57ababbc7ec2a289f96df06fdcfef`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fef3fc627836546c092799bf908950736a43620096addd06b21433525e99e3`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c64b7c90c1c37cb6c8832b41e9dab9a67a8fb0252dc2e633be3cee0fba0493`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:61b554c5908413812c039093ada2bfc56d219edb693d1d078f4100ca9ab6e226
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591712906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7716f237684cdfd6c1d7303481a77ed2f1b8d845479485ec22000ba725477dbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:09 GMT
ADD file:a935b2993c62bfb1ade6ba0ffcf1f955422f6f76c63a723877d4bca5bb2aff7b in / 
# Wed, 01 Nov 2023 00:22:11 GMT
CMD ["bash"]
# Wed, 08 Nov 2023 00:35:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Nov 2023 00:35:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Nov 2023 00:35:12 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:35:13 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:37:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:38:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:38:10 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:38:10 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:38:10 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:38:11 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:40:18 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:40:33 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:40:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:40:34 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:40:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:40:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:40:35 GMT
USER odoo
# Wed, 08 Nov 2023 00:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:40:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c4a0eee30f72e7c0e9938500fbc7f30b5eb02d04d49bfe7f18a17af1a6d82f81`  
		Last Modified: Wed, 01 Nov 2023 00:26:59 GMT  
		Size: 35.3 MB (35293810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbf24c6962f4383105fa75766afb1694587cd6eee6991d84986cc06060d14b0`  
		Last Modified: Wed, 08 Nov 2023 00:41:30 GMT  
		Size: 228.6 MB (228597689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2525c03537826015f6883a915c56344809b0b4d609d0331aa7496a6133c9a0d4`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 2.9 MB (2874169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f399970742679afbe633c65177cfcac0bc40ea17093cf32acf0175b1c765b8a`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 459.5 KB (459462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13500816d0a55578fb3acde8b75034d7c929fc654ccc114e9d8f1a17d45976b`  
		Last Modified: Wed, 08 Nov 2023 00:41:43 GMT  
		Size: 324.5 MB (324485311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8814df038c86cf9c05085931a40ed23bea1ce5702d854ed276944dcf6191ae`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e316c6ff6941cbe4117491ea563ecfcf91b6176f243de0c30ceacf7939b162`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254fd04082fa3cc5bf8f9ab205f103084858296096f0c626a10d5bba2a18b823`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb744a3bde4cae9e418d9711328d6957a6dea74a5e0eca8ae7e83287b9525e05`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:b02db1a3a5207ec2dee2245d8321b1a510682fd1a8c617f18314b14eba883fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:050d6909f19797b0113b195dac076d9f9e9d48906c8a9c00b017d4a3162b2f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.1 MB (577148541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e4063887fdfe4a2ffda6523576bbcd058e1040f9a000d336d84f9d7e0c77d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:38:54 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:40:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:40:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:40:19 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:40:19 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:41:41 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:41:45 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:41:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:41:45 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:41:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:41:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:41:46 GMT
USER odoo
# Wed, 08 Nov 2023 00:41:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:41:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3abf7b1c0fb11700caf26b92dbcf9281f5ee88bb7be113dd51e1237f1c4b8`  
		Last Modified: Wed, 08 Nov 2023 00:45:23 GMT  
		Size: 219.6 MB (219607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e024eac15856bbec7f25f475d3c1810249d92b2608024fd861df2de7af7dd`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 2.6 MB (2628109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eee1f11dc9d1c4617dcf3d9bf6d5368df3304931f6c41b3318eb2bf05ef1605`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 459.5 KB (459516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c3322fe74239122fed63bc5d7c0ad8426f1f64b70f8605a7d9bc76b24731bc`  
		Last Modified: Wed, 08 Nov 2023 00:45:34 GMT  
		Size: 323.0 MB (323033428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790686c1cd5cc1e7e382ab129cd19542d38167c0f49b12d62fc499162ba3034b`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e3a6dcb28c4c6bfc8b69508a4e912cfb0d4ccfb03691c3aa654da8b0e4238f`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f8d088b6082f21385081c583e38925e485c4cf273eea4611d603a9c4c5b505`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ddc13242fd0b2e64c6f399370d12edda33f930841d1d805eaf93eba5341c38`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:26c2150d81e20760d93ea2ef38be3c2823814e2ae83382173d68de066426d911
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572792791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015469bef4a58eaa7b4390f7619903866e1a48f66afe18a8b2f3f56aca54fc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 07 Nov 2023 23:48:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Nov 2023 23:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Nov 2023 23:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Nov 2023 23:48:30 GMT
ARG TARGETARCH
# Tue, 07 Nov 2023 23:49:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 07 Nov 2023 23:49:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Nov 2023 23:49:48 GMT
RUN npm install -g rtlcss
# Tue, 07 Nov 2023 23:49:48 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 Nov 2023 00:56:03 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:56:03 GMT
ARG ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
# Tue, 14 Nov 2023 00:57:15 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:57:22 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:57:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:57:22 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:57:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:57:22 GMT
USER odoo
# Tue, 14 Nov 2023 00:57:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:57:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5812a002d612ea362d56834609da19cbf53fb331e9f92b0b4b8d1cdd3b8aa9`  
		Last Modified: Tue, 07 Nov 2023 23:51:50 GMT  
		Size: 216.9 MB (216907690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59eaf6b2e981344b7a4bf54a869a293a9e69d429da23202eed603c8f1f41835`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 2.6 MB (2634000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2aeeb4414cf9678f9200a368d1873d1290880b10ec32b5a9264ae836d479b`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 459.4 KB (459450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdf05cdc5b9b591787678961a1ec1aec071c1057eed23c306d8c0040718da8e`  
		Last Modified: Tue, 14 Nov 2023 00:58:44 GMT  
		Size: 322.7 MB (322725284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b14bf046a1e125c9aac7baff7af0f75345f5268208d4912f510efa3bf78ca1`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0bf7919c61b58c943d6cc0bc1f5767a8b57ababbc7ec2a289f96df06fdcfef`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fef3fc627836546c092799bf908950736a43620096addd06b21433525e99e3`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c64b7c90c1c37cb6c8832b41e9dab9a67a8fb0252dc2e633be3cee0fba0493`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:61b554c5908413812c039093ada2bfc56d219edb693d1d078f4100ca9ab6e226
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591712906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7716f237684cdfd6c1d7303481a77ed2f1b8d845479485ec22000ba725477dbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:09 GMT
ADD file:a935b2993c62bfb1ade6ba0ffcf1f955422f6f76c63a723877d4bca5bb2aff7b in / 
# Wed, 01 Nov 2023 00:22:11 GMT
CMD ["bash"]
# Wed, 08 Nov 2023 00:35:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Nov 2023 00:35:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Nov 2023 00:35:12 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:35:13 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:37:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:38:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:38:10 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:38:10 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:38:10 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:38:11 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:40:18 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:40:33 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:40:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:40:34 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:40:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:40:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:40:35 GMT
USER odoo
# Wed, 08 Nov 2023 00:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:40:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c4a0eee30f72e7c0e9938500fbc7f30b5eb02d04d49bfe7f18a17af1a6d82f81`  
		Last Modified: Wed, 01 Nov 2023 00:26:59 GMT  
		Size: 35.3 MB (35293810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbf24c6962f4383105fa75766afb1694587cd6eee6991d84986cc06060d14b0`  
		Last Modified: Wed, 08 Nov 2023 00:41:30 GMT  
		Size: 228.6 MB (228597689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2525c03537826015f6883a915c56344809b0b4d609d0331aa7496a6133c9a0d4`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 2.9 MB (2874169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f399970742679afbe633c65177cfcac0bc40ea17093cf32acf0175b1c765b8a`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 459.5 KB (459462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13500816d0a55578fb3acde8b75034d7c929fc654ccc114e9d8f1a17d45976b`  
		Last Modified: Wed, 08 Nov 2023 00:41:43 GMT  
		Size: 324.5 MB (324485311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8814df038c86cf9c05085931a40ed23bea1ce5702d854ed276944dcf6191ae`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e316c6ff6941cbe4117491ea563ecfcf91b6176f243de0c30ceacf7939b162`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254fd04082fa3cc5bf8f9ab205f103084858296096f0c626a10d5bba2a18b823`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb744a3bde4cae9e418d9711328d6957a6dea74a5e0eca8ae7e83287b9525e05`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:892154cc315087a3576741951d9db38493f322089fecb30db761601efcfcec7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ace6418846e2418f335ebb344cde203804b3c7d7805b2725dcfc9a9add4ca940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587401328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7106e5398bb060deb25fbf804f531529370f2516531f15ff023a807a809a6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 00:55:41 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:55:48 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:55:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:55:49 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:55:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:55:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:55:49 GMT
USER odoo
# Tue, 14 Nov 2023 00:55:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:55:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cce5f2a0c53a04404cd97f574d6ca67a2a85cbd2e66097307815e57487c0a4`  
		Last Modified: Tue, 14 Nov 2023 00:58:02 GMT  
		Size: 322.8 MB (322780729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524cd683dc13eb9d4acc94b4f4f7f8fe90f1ffd93bf20cb717305ed27c3d7309`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94974e1c2b8342a72e8fb852853aa86d67311a9249009ac2d4b3bf9fc8299a24`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1aee512583463453d60c93a2f72efbd2848ae464cea90e3242a994c9bc594a`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb06a82b5f82620d2831d2e5586afc5df36e67401451e0e71b07578a531b270`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:892154cc315087a3576741951d9db38493f322089fecb30db761601efcfcec7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ace6418846e2418f335ebb344cde203804b3c7d7805b2725dcfc9a9add4ca940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587401328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7106e5398bb060deb25fbf804f531529370f2516531f15ff023a807a809a6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 00:55:41 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:55:48 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:55:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:55:49 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:55:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:55:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:55:49 GMT
USER odoo
# Tue, 14 Nov 2023 00:55:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:55:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cce5f2a0c53a04404cd97f574d6ca67a2a85cbd2e66097307815e57487c0a4`  
		Last Modified: Tue, 14 Nov 2023 00:58:02 GMT  
		Size: 322.8 MB (322780729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524cd683dc13eb9d4acc94b4f4f7f8fe90f1ffd93bf20cb717305ed27c3d7309`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94974e1c2b8342a72e8fb852853aa86d67311a9249009ac2d4b3bf9fc8299a24`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1aee512583463453d60c93a2f72efbd2848ae464cea90e3242a994c9bc594a`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb06a82b5f82620d2831d2e5586afc5df36e67401451e0e71b07578a531b270`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:f5c4f7ccde96db79729b90eec1a63078517dfd7326eade4ff0513026fee3ba99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:050d6909f19797b0113b195dac076d9f9e9d48906c8a9c00b017d4a3162b2f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.1 MB (577148541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e4063887fdfe4a2ffda6523576bbcd058e1040f9a000d336d84f9d7e0c77d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:38:54 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:40:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:40:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:40:19 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:40:19 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:41:41 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:41:45 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:41:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:41:45 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:41:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:41:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:41:46 GMT
USER odoo
# Wed, 08 Nov 2023 00:41:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:41:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3abf7b1c0fb11700caf26b92dbcf9281f5ee88bb7be113dd51e1237f1c4b8`  
		Last Modified: Wed, 08 Nov 2023 00:45:23 GMT  
		Size: 219.6 MB (219607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e024eac15856bbec7f25f475d3c1810249d92b2608024fd861df2de7af7dd`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 2.6 MB (2628109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eee1f11dc9d1c4617dcf3d9bf6d5368df3304931f6c41b3318eb2bf05ef1605`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 459.5 KB (459516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c3322fe74239122fed63bc5d7c0ad8426f1f64b70f8605a7d9bc76b24731bc`  
		Last Modified: Wed, 08 Nov 2023 00:45:34 GMT  
		Size: 323.0 MB (323033428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790686c1cd5cc1e7e382ab129cd19542d38167c0f49b12d62fc499162ba3034b`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e3a6dcb28c4c6bfc8b69508a4e912cfb0d4ccfb03691c3aa654da8b0e4238f`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f8d088b6082f21385081c583e38925e485c4cf273eea4611d603a9c4c5b505`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ddc13242fd0b2e64c6f399370d12edda33f930841d1d805eaf93eba5341c38`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ace6418846e2418f335ebb344cde203804b3c7d7805b2725dcfc9a9add4ca940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587401328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7106e5398bb060deb25fbf804f531529370f2516531f15ff023a807a809a6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 00:55:41 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:55:48 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:55:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:55:49 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:55:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:55:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:55:49 GMT
USER odoo
# Tue, 14 Nov 2023 00:55:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:55:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cce5f2a0c53a04404cd97f574d6ca67a2a85cbd2e66097307815e57487c0a4`  
		Last Modified: Tue, 14 Nov 2023 00:58:02 GMT  
		Size: 322.8 MB (322780729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524cd683dc13eb9d4acc94b4f4f7f8fe90f1ffd93bf20cb717305ed27c3d7309`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94974e1c2b8342a72e8fb852853aa86d67311a9249009ac2d4b3bf9fc8299a24`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1aee512583463453d60c93a2f72efbd2848ae464cea90e3242a994c9bc594a`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb06a82b5f82620d2831d2e5586afc5df36e67401451e0e71b07578a531b270`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:61b554c5908413812c039093ada2bfc56d219edb693d1d078f4100ca9ab6e226
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591712906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7716f237684cdfd6c1d7303481a77ed2f1b8d845479485ec22000ba725477dbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:09 GMT
ADD file:a935b2993c62bfb1ade6ba0ffcf1f955422f6f76c63a723877d4bca5bb2aff7b in / 
# Wed, 01 Nov 2023 00:22:11 GMT
CMD ["bash"]
# Wed, 08 Nov 2023 00:35:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Nov 2023 00:35:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Nov 2023 00:35:12 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:35:13 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:37:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:38:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:38:10 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:38:10 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:38:10 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:38:11 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:40:18 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:40:33 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:40:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:40:34 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:40:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:40:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:40:35 GMT
USER odoo
# Wed, 08 Nov 2023 00:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:40:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c4a0eee30f72e7c0e9938500fbc7f30b5eb02d04d49bfe7f18a17af1a6d82f81`  
		Last Modified: Wed, 01 Nov 2023 00:26:59 GMT  
		Size: 35.3 MB (35293810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbf24c6962f4383105fa75766afb1694587cd6eee6991d84986cc06060d14b0`  
		Last Modified: Wed, 08 Nov 2023 00:41:30 GMT  
		Size: 228.6 MB (228597689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2525c03537826015f6883a915c56344809b0b4d609d0331aa7496a6133c9a0d4`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 2.9 MB (2874169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f399970742679afbe633c65177cfcac0bc40ea17093cf32acf0175b1c765b8a`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 459.5 KB (459462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13500816d0a55578fb3acde8b75034d7c929fc654ccc114e9d8f1a17d45976b`  
		Last Modified: Wed, 08 Nov 2023 00:41:43 GMT  
		Size: 324.5 MB (324485311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8814df038c86cf9c05085931a40ed23bea1ce5702d854ed276944dcf6191ae`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e316c6ff6941cbe4117491ea563ecfcf91b6176f243de0c30ceacf7939b162`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254fd04082fa3cc5bf8f9ab205f103084858296096f0c626a10d5bba2a18b823`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb744a3bde4cae9e418d9711328d6957a6dea74a5e0eca8ae7e83287b9525e05`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
