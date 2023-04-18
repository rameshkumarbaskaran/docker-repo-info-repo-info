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
$ docker pull odoo@sha256:a06df8ba597d5c6c3ae05f8c6de07b83e69398ecd9550aeeaa09feaff9687467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:6f74392d7e7dcc24304273a7afca94476696e245c30d1f576c4b82304f855194
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532258780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e6ad388b8af9496732d210d134fbeea5f92823d9237aa5b742c771a6b01443`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:25 GMT
ADD file:e614539607055bdbde0cc1a94ef9783fe3627c8553ef1b21071ecb5c27ea27e4 in / 
# Wed, 12 Apr 2023 00:20:26 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:58:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 Apr 2023 08:58:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 Apr 2023 08:58:51 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 09:00:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 Apr 2023 09:00:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:00:29 GMT
RUN npm install -g rtlcss
# Wed, 12 Apr 2023 09:00:30 GMT
ENV ODOO_VERSION=14.0
# Tue, 18 Apr 2023 18:22:59 GMT
ARG ODOO_RELEASE=20230418
# Tue, 18 Apr 2023 18:22:59 GMT
ARG ODOO_SHA=328906b0728ba10b19ce1ef5c4d98caba2fb38dd
# Tue, 18 Apr 2023 18:24:20 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=328906b0728ba10b19ce1ef5c4d98caba2fb38dd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 Apr 2023 18:24:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 18 Apr 2023 18:24:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 Apr 2023 18:24:25 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=328906b0728ba10b19ce1ef5c4d98caba2fb38dd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 Apr 2023 18:24:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Apr 2023 18:24:25 GMT
EXPOSE 8069 8071 8072
# Tue, 18 Apr 2023 18:24:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Apr 2023 18:24:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 Apr 2023 18:24:25 GMT
USER odoo
# Tue, 18 Apr 2023 18:24:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Apr 2023 18:24:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9fbefa3370776b7ec7633cf07efc14cc24e0c0cd53893ad0e7e3f44ffdc1bedb`  
		Last Modified: Wed, 12 Apr 2023 00:24:22 GMT  
		Size: 27.1 MB (27138920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe00d75581d1741b260047f82ac192a761c24b6c2d68e527e4a0de334335aa31`  
		Last Modified: Wed, 12 Apr 2023 09:04:00 GMT  
		Size: 213.2 MB (213203787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41383b72b69d61dc58305cf803eb49130c28b9c3978783268058f107ef8f2c35`  
		Last Modified: Wed, 12 Apr 2023 09:03:39 GMT  
		Size: 13.5 MB (13517731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6cb4d73ac452284f4e76b99129bce0d2ad7863d895cfd103f629d01b3b1e38`  
		Last Modified: Wed, 12 Apr 2023 09:03:37 GMT  
		Size: 453.9 KB (453862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c95701281f01ec724f6aaef37a46306d9f155c2ee2a80f2d72f8658b2bce8f`  
		Last Modified: Tue, 18 Apr 2023 18:26:44 GMT  
		Size: 277.9 MB (277942021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7877abbdd4d98a694dc1dee041444b2b9fe5406a024b6a25f7a0d893eda7cf32`  
		Last Modified: Tue, 18 Apr 2023 18:26:14 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5b86a82f8c74e307ecb1fd9f27b6a2884cd7dda83c346070322627e4535780`  
		Last Modified: Tue, 18 Apr 2023 18:26:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fc6e0abd65bec48c47f61e5b9f3b564e8bea7a623056cbb9e92204812b421b`  
		Last Modified: Tue, 18 Apr 2023 18:26:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb2c3b7428b4447f8c2aca1d909a8c41253610fad09a852a96a783af1433044`  
		Last Modified: Tue, 18 Apr 2023 18:26:14 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:a06df8ba597d5c6c3ae05f8c6de07b83e69398ecd9550aeeaa09feaff9687467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:6f74392d7e7dcc24304273a7afca94476696e245c30d1f576c4b82304f855194
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532258780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e6ad388b8af9496732d210d134fbeea5f92823d9237aa5b742c771a6b01443`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:25 GMT
ADD file:e614539607055bdbde0cc1a94ef9783fe3627c8553ef1b21071ecb5c27ea27e4 in / 
# Wed, 12 Apr 2023 00:20:26 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:58:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 Apr 2023 08:58:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 Apr 2023 08:58:51 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 09:00:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 Apr 2023 09:00:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:00:29 GMT
RUN npm install -g rtlcss
# Wed, 12 Apr 2023 09:00:30 GMT
ENV ODOO_VERSION=14.0
# Tue, 18 Apr 2023 18:22:59 GMT
ARG ODOO_RELEASE=20230418
# Tue, 18 Apr 2023 18:22:59 GMT
ARG ODOO_SHA=328906b0728ba10b19ce1ef5c4d98caba2fb38dd
# Tue, 18 Apr 2023 18:24:20 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=328906b0728ba10b19ce1ef5c4d98caba2fb38dd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 Apr 2023 18:24:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 18 Apr 2023 18:24:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 Apr 2023 18:24:25 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=328906b0728ba10b19ce1ef5c4d98caba2fb38dd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 Apr 2023 18:24:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Apr 2023 18:24:25 GMT
EXPOSE 8069 8071 8072
# Tue, 18 Apr 2023 18:24:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Apr 2023 18:24:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 Apr 2023 18:24:25 GMT
USER odoo
# Tue, 18 Apr 2023 18:24:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Apr 2023 18:24:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9fbefa3370776b7ec7633cf07efc14cc24e0c0cd53893ad0e7e3f44ffdc1bedb`  
		Last Modified: Wed, 12 Apr 2023 00:24:22 GMT  
		Size: 27.1 MB (27138920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe00d75581d1741b260047f82ac192a761c24b6c2d68e527e4a0de334335aa31`  
		Last Modified: Wed, 12 Apr 2023 09:04:00 GMT  
		Size: 213.2 MB (213203787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41383b72b69d61dc58305cf803eb49130c28b9c3978783268058f107ef8f2c35`  
		Last Modified: Wed, 12 Apr 2023 09:03:39 GMT  
		Size: 13.5 MB (13517731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6cb4d73ac452284f4e76b99129bce0d2ad7863d895cfd103f629d01b3b1e38`  
		Last Modified: Wed, 12 Apr 2023 09:03:37 GMT  
		Size: 453.9 KB (453862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c95701281f01ec724f6aaef37a46306d9f155c2ee2a80f2d72f8658b2bce8f`  
		Last Modified: Tue, 18 Apr 2023 18:26:44 GMT  
		Size: 277.9 MB (277942021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7877abbdd4d98a694dc1dee041444b2b9fe5406a024b6a25f7a0d893eda7cf32`  
		Last Modified: Tue, 18 Apr 2023 18:26:14 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5b86a82f8c74e307ecb1fd9f27b6a2884cd7dda83c346070322627e4535780`  
		Last Modified: Tue, 18 Apr 2023 18:26:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fc6e0abd65bec48c47f61e5b9f3b564e8bea7a623056cbb9e92204812b421b`  
		Last Modified: Tue, 18 Apr 2023 18:26:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb2c3b7428b4447f8c2aca1d909a8c41253610fad09a852a96a783af1433044`  
		Last Modified: Tue, 18 Apr 2023 18:26:14 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:af7c2772e34213f68ad60b8f8c78b5d424c5697f2b43382e69f80d3adf02511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:a7a3a31cd222a70bacb417188dfc860f2ca081df228d8c253b28b7df7d57a062
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.7 MB (560728221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bedd82a301040837c840db0913d4f791f49c7df83274ac60943951fb19e5a36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:54:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 Apr 2023 08:54:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 Apr 2023 08:54:35 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 08:55:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 Apr 2023 08:55:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:55:54 GMT
RUN npm install -g rtlcss
# Wed, 12 Apr 2023 08:57:28 GMT
ENV ODOO_VERSION=15.0
# Tue, 18 Apr 2023 18:21:36 GMT
ARG ODOO_RELEASE=20230418
# Tue, 18 Apr 2023 18:21:36 GMT
ARG ODOO_SHA=429b040f5ac5dd1b0c55d1ea7cb7063645479a8e
# Tue, 18 Apr 2023 18:22:48 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=429b040f5ac5dd1b0c55d1ea7cb7063645479a8e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 Apr 2023 18:22:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 18 Apr 2023 18:22:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 Apr 2023 18:22:52 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=429b040f5ac5dd1b0c55d1ea7cb7063645479a8e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 Apr 2023 18:22:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Apr 2023 18:22:53 GMT
EXPOSE 8069 8071 8072
# Tue, 18 Apr 2023 18:22:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Apr 2023 18:22:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 Apr 2023 18:22:53 GMT
USER odoo
# Tue, 18 Apr 2023 18:22:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Apr 2023 18:22:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc072a51e9ff1e113fd7d7e6e812f69acee46b65fdb5e60e6a6977ab04867f8f`  
		Last Modified: Wed, 12 Apr 2023 09:02:33 GMT  
		Size: 220.3 MB (220298412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea2cf4d76c14443a63296eecd70cd09a9af720ca062d516b3f41535b435edf2`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 2.6 MB (2575214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfcc7225c9d8a7756bbe895737596be4bb564e0e7223b89b59cd40b96d7735b`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 449.3 KB (449266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915b78997d0a5f2405f4299ecaace26944241eb7127f500288a201f130e44fe4`  
		Last Modified: Tue, 18 Apr 2023 18:26:06 GMT  
		Size: 306.0 MB (305984640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d794b96855e85fe30712f9f8ff14fd01999543a5d7799082b73559b087895ba9`  
		Last Modified: Tue, 18 Apr 2023 18:25:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118a41f54cf5cb795aef402315b6b8705b9932f36736a80b084c78d807fa37d7`  
		Last Modified: Tue, 18 Apr 2023 18:25:32 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381ff343423818eac49babf76a309dab65d122c057836002b331f89ac11c4bc2`  
		Last Modified: Tue, 18 Apr 2023 18:25:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296a1c5a24fb295bb04bfa81643a3783e56042b5a662ece098ab7aafcd077a90`  
		Last Modified: Tue, 18 Apr 2023 18:25:32 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:af7c2772e34213f68ad60b8f8c78b5d424c5697f2b43382e69f80d3adf02511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:a7a3a31cd222a70bacb417188dfc860f2ca081df228d8c253b28b7df7d57a062
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.7 MB (560728221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bedd82a301040837c840db0913d4f791f49c7df83274ac60943951fb19e5a36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:54:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 Apr 2023 08:54:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 Apr 2023 08:54:35 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 08:55:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 Apr 2023 08:55:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:55:54 GMT
RUN npm install -g rtlcss
# Wed, 12 Apr 2023 08:57:28 GMT
ENV ODOO_VERSION=15.0
# Tue, 18 Apr 2023 18:21:36 GMT
ARG ODOO_RELEASE=20230418
# Tue, 18 Apr 2023 18:21:36 GMT
ARG ODOO_SHA=429b040f5ac5dd1b0c55d1ea7cb7063645479a8e
# Tue, 18 Apr 2023 18:22:48 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=429b040f5ac5dd1b0c55d1ea7cb7063645479a8e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 Apr 2023 18:22:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 18 Apr 2023 18:22:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 Apr 2023 18:22:52 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=429b040f5ac5dd1b0c55d1ea7cb7063645479a8e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 Apr 2023 18:22:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Apr 2023 18:22:53 GMT
EXPOSE 8069 8071 8072
# Tue, 18 Apr 2023 18:22:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Apr 2023 18:22:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 Apr 2023 18:22:53 GMT
USER odoo
# Tue, 18 Apr 2023 18:22:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Apr 2023 18:22:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc072a51e9ff1e113fd7d7e6e812f69acee46b65fdb5e60e6a6977ab04867f8f`  
		Last Modified: Wed, 12 Apr 2023 09:02:33 GMT  
		Size: 220.3 MB (220298412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea2cf4d76c14443a63296eecd70cd09a9af720ca062d516b3f41535b435edf2`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 2.6 MB (2575214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfcc7225c9d8a7756bbe895737596be4bb564e0e7223b89b59cd40b96d7735b`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 449.3 KB (449266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915b78997d0a5f2405f4299ecaace26944241eb7127f500288a201f130e44fe4`  
		Last Modified: Tue, 18 Apr 2023 18:26:06 GMT  
		Size: 306.0 MB (305984640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d794b96855e85fe30712f9f8ff14fd01999543a5d7799082b73559b087895ba9`  
		Last Modified: Tue, 18 Apr 2023 18:25:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118a41f54cf5cb795aef402315b6b8705b9932f36736a80b084c78d807fa37d7`  
		Last Modified: Tue, 18 Apr 2023 18:25:32 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381ff343423818eac49babf76a309dab65d122c057836002b331f89ac11c4bc2`  
		Last Modified: Tue, 18 Apr 2023 18:25:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296a1c5a24fb295bb04bfa81643a3783e56042b5a662ece098ab7aafcd077a90`  
		Last Modified: Tue, 18 Apr 2023 18:25:32 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:453479c2ed3cff851bf0c459c467c797bb2ee1e515e627f120010f987f5ef020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:636600e317649d1a59ea2b8a37ba786df212edf104114181ac9e4df89c911531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.4 MB (569441359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8360dbb2cb54bb0f92adb610db7aef2287b64c4f32ef254451b352ba1ae426`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:54:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 Apr 2023 08:54:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 Apr 2023 08:54:35 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 08:55:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 Apr 2023 08:55:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:55:54 GMT
RUN npm install -g rtlcss
# Wed, 12 Apr 2023 08:55:54 GMT
ENV ODOO_VERSION=16.0
# Tue, 18 Apr 2023 18:19:58 GMT
ARG ODOO_RELEASE=20230418
# Tue, 18 Apr 2023 18:19:58 GMT
ARG ODOO_SHA=0a06b542c7cca901ff0c10439f948ac4645e319a
# Tue, 18 Apr 2023 18:21:30 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=0a06b542c7cca901ff0c10439f948ac4645e319a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 Apr 2023 18:21:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 18 Apr 2023 18:21:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 Apr 2023 18:21:33 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=0a06b542c7cca901ff0c10439f948ac4645e319a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 Apr 2023 18:21:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Apr 2023 18:21:33 GMT
EXPOSE 8069 8071 8072
# Tue, 18 Apr 2023 18:21:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Apr 2023 18:21:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 Apr 2023 18:21:33 GMT
USER odoo
# Tue, 18 Apr 2023 18:21:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Apr 2023 18:21:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc072a51e9ff1e113fd7d7e6e812f69acee46b65fdb5e60e6a6977ab04867f8f`  
		Last Modified: Wed, 12 Apr 2023 09:02:33 GMT  
		Size: 220.3 MB (220298412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea2cf4d76c14443a63296eecd70cd09a9af720ca062d516b3f41535b435edf2`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 2.6 MB (2575214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfcc7225c9d8a7756bbe895737596be4bb564e0e7223b89b59cd40b96d7735b`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 449.3 KB (449266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8410c47f132d58d0a086b6a94c0b61238de6e6757e2d822ba38f924ee90883`  
		Last Modified: Tue, 18 Apr 2023 18:25:22 GMT  
		Size: 314.7 MB (314697775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc3a9409befe84c59a88d9593db54719b00f3ae42c9a98ba55d3664d373e6fd`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c7e6ebd96d3dd924c7b60cb245dac1f21c23a2edef5699ce84a04eb81c924`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577e7a80785434d1fcc670588688651c88b9d80516c674fcb30a80ba55412ce7`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b8678c336f8dc6462cb9f36b8a540d303d32a9fcbd244b2947d13c2eeac09f`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:453479c2ed3cff851bf0c459c467c797bb2ee1e515e627f120010f987f5ef020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:636600e317649d1a59ea2b8a37ba786df212edf104114181ac9e4df89c911531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.4 MB (569441359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8360dbb2cb54bb0f92adb610db7aef2287b64c4f32ef254451b352ba1ae426`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:54:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 Apr 2023 08:54:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 Apr 2023 08:54:35 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 08:55:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 Apr 2023 08:55:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:55:54 GMT
RUN npm install -g rtlcss
# Wed, 12 Apr 2023 08:55:54 GMT
ENV ODOO_VERSION=16.0
# Tue, 18 Apr 2023 18:19:58 GMT
ARG ODOO_RELEASE=20230418
# Tue, 18 Apr 2023 18:19:58 GMT
ARG ODOO_SHA=0a06b542c7cca901ff0c10439f948ac4645e319a
# Tue, 18 Apr 2023 18:21:30 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=0a06b542c7cca901ff0c10439f948ac4645e319a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 Apr 2023 18:21:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 18 Apr 2023 18:21:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 Apr 2023 18:21:33 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=0a06b542c7cca901ff0c10439f948ac4645e319a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 Apr 2023 18:21:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Apr 2023 18:21:33 GMT
EXPOSE 8069 8071 8072
# Tue, 18 Apr 2023 18:21:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Apr 2023 18:21:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 Apr 2023 18:21:33 GMT
USER odoo
# Tue, 18 Apr 2023 18:21:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Apr 2023 18:21:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc072a51e9ff1e113fd7d7e6e812f69acee46b65fdb5e60e6a6977ab04867f8f`  
		Last Modified: Wed, 12 Apr 2023 09:02:33 GMT  
		Size: 220.3 MB (220298412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea2cf4d76c14443a63296eecd70cd09a9af720ca062d516b3f41535b435edf2`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 2.6 MB (2575214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfcc7225c9d8a7756bbe895737596be4bb564e0e7223b89b59cd40b96d7735b`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 449.3 KB (449266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8410c47f132d58d0a086b6a94c0b61238de6e6757e2d822ba38f924ee90883`  
		Last Modified: Tue, 18 Apr 2023 18:25:22 GMT  
		Size: 314.7 MB (314697775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc3a9409befe84c59a88d9593db54719b00f3ae42c9a98ba55d3664d373e6fd`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c7e6ebd96d3dd924c7b60cb245dac1f21c23a2edef5699ce84a04eb81c924`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577e7a80785434d1fcc670588688651c88b9d80516c674fcb30a80ba55412ce7`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b8678c336f8dc6462cb9f36b8a540d303d32a9fcbd244b2947d13c2eeac09f`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:453479c2ed3cff851bf0c459c467c797bb2ee1e515e627f120010f987f5ef020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:636600e317649d1a59ea2b8a37ba786df212edf104114181ac9e4df89c911531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.4 MB (569441359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8360dbb2cb54bb0f92adb610db7aef2287b64c4f32ef254451b352ba1ae426`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:54:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 Apr 2023 08:54:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 Apr 2023 08:54:35 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 08:55:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 Apr 2023 08:55:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:55:54 GMT
RUN npm install -g rtlcss
# Wed, 12 Apr 2023 08:55:54 GMT
ENV ODOO_VERSION=16.0
# Tue, 18 Apr 2023 18:19:58 GMT
ARG ODOO_RELEASE=20230418
# Tue, 18 Apr 2023 18:19:58 GMT
ARG ODOO_SHA=0a06b542c7cca901ff0c10439f948ac4645e319a
# Tue, 18 Apr 2023 18:21:30 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=0a06b542c7cca901ff0c10439f948ac4645e319a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 Apr 2023 18:21:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 18 Apr 2023 18:21:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 Apr 2023 18:21:33 GMT
# ARGS: ODOO_RELEASE=20230418 ODOO_SHA=0a06b542c7cca901ff0c10439f948ac4645e319a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 Apr 2023 18:21:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Apr 2023 18:21:33 GMT
EXPOSE 8069 8071 8072
# Tue, 18 Apr 2023 18:21:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Apr 2023 18:21:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 Apr 2023 18:21:33 GMT
USER odoo
# Tue, 18 Apr 2023 18:21:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Apr 2023 18:21:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc072a51e9ff1e113fd7d7e6e812f69acee46b65fdb5e60e6a6977ab04867f8f`  
		Last Modified: Wed, 12 Apr 2023 09:02:33 GMT  
		Size: 220.3 MB (220298412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea2cf4d76c14443a63296eecd70cd09a9af720ca062d516b3f41535b435edf2`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 2.6 MB (2575214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfcc7225c9d8a7756bbe895737596be4bb564e0e7223b89b59cd40b96d7735b`  
		Last Modified: Wed, 12 Apr 2023 09:02:09 GMT  
		Size: 449.3 KB (449266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8410c47f132d58d0a086b6a94c0b61238de6e6757e2d822ba38f924ee90883`  
		Last Modified: Tue, 18 Apr 2023 18:25:22 GMT  
		Size: 314.7 MB (314697775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc3a9409befe84c59a88d9593db54719b00f3ae42c9a98ba55d3664d373e6fd`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c7e6ebd96d3dd924c7b60cb245dac1f21c23a2edef5699ce84a04eb81c924`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577e7a80785434d1fcc670588688651c88b9d80516c674fcb30a80ba55412ce7`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b8678c336f8dc6462cb9f36b8a540d303d32a9fcbd244b2947d13c2eeac09f`  
		Last Modified: Tue, 18 Apr 2023 18:24:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
