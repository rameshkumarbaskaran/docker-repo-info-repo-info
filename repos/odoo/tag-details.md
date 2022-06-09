<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:latest`](#odoolatest)

## `odoo:13`

```console
$ docker pull odoo@sha256:04fef2741a63d04dd897d77b7c6e2cb68951f2ad8c858c4156dff941d07bd099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:8172416d193d10ef707e9e8cd5e8bc241bb5ec8ee6c4fa61dfba6f719a2e1ee1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540106795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d908ecd4c11118bf67e530808c1bd3e8b005e370f75d9154e525e39d2e91e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:05:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:05:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:05:50 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:05:51 GMT
ENV ODOO_VERSION=13.0
# Thu, 09 Jun 2022 17:23:27 GMT
ARG ODOO_RELEASE=20220609
# Thu, 09 Jun 2022 17:23:27 GMT
ARG ODOO_SHA=bda7f94b0e8fb8bad3ff46db1ea1ca6928757533
# Thu, 09 Jun 2022 17:24:47 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=bda7f94b0e8fb8bad3ff46db1ea1ca6928757533
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 09 Jun 2022 17:24:51 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 09 Jun 2022 17:24:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 09 Jun 2022 17:24:51 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=bda7f94b0e8fb8bad3ff46db1ea1ca6928757533
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 09 Jun 2022 17:24:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Jun 2022 17:24:52 GMT
EXPOSE 8069 8071 8072
# Thu, 09 Jun 2022 17:24:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Jun 2022 17:24:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 09 Jun 2022 17:24:52 GMT
USER odoo
# Thu, 09 Jun 2022 17:24:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Jun 2022 17:24:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c79567322b70756577efd1f8dcfa0263c984e263011e9803a7cda6aba5173a5`  
		Last Modified: Sat, 28 May 2022 12:09:33 GMT  
		Size: 207.1 MB (207143382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a85e75296e74df756190aea4b584b8e8697311966131e1f25a32ab750c6a6c`  
		Last Modified: Sat, 28 May 2022 12:09:11 GMT  
		Size: 13.4 MB (13442815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3489e5884bd67ef88e775a66acb08289f084239dc3fc159caa11154b5f40f2`  
		Last Modified: Sat, 28 May 2022 12:09:08 GMT  
		Size: 480.5 KB (480504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8fd9b0159d413bd33deb24a38e4ebf2ac9968908f45f3eecdb9685428826ad`  
		Last Modified: Thu, 09 Jun 2022 17:27:20 GMT  
		Size: 291.9 MB (291897486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4e760cb83fe70259cc440c48df9fe604a0a84d96c82954cd679a2e01420060`  
		Last Modified: Thu, 09 Jun 2022 17:26:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b719ad13b3873ac0239435ed43e215fb811eab0fb099472d4293b216c033d7`  
		Last Modified: Thu, 09 Jun 2022 17:26:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852ecf2169d22f141d9abbe53cfb5edb3535bea2942ecb1ae2af7ea42ff23f1a`  
		Last Modified: Thu, 09 Jun 2022 17:26:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc71052ec405bb81812bbbcdab2cd604ae5e31d5fe1555981b0be49eb8fbee1f`  
		Last Modified: Thu, 09 Jun 2022 17:26:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:04fef2741a63d04dd897d77b7c6e2cb68951f2ad8c858c4156dff941d07bd099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:8172416d193d10ef707e9e8cd5e8bc241bb5ec8ee6c4fa61dfba6f719a2e1ee1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540106795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d908ecd4c11118bf67e530808c1bd3e8b005e370f75d9154e525e39d2e91e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:05:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:05:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:05:50 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:05:51 GMT
ENV ODOO_VERSION=13.0
# Thu, 09 Jun 2022 17:23:27 GMT
ARG ODOO_RELEASE=20220609
# Thu, 09 Jun 2022 17:23:27 GMT
ARG ODOO_SHA=bda7f94b0e8fb8bad3ff46db1ea1ca6928757533
# Thu, 09 Jun 2022 17:24:47 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=bda7f94b0e8fb8bad3ff46db1ea1ca6928757533
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 09 Jun 2022 17:24:51 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 09 Jun 2022 17:24:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 09 Jun 2022 17:24:51 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=bda7f94b0e8fb8bad3ff46db1ea1ca6928757533
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 09 Jun 2022 17:24:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Jun 2022 17:24:52 GMT
EXPOSE 8069 8071 8072
# Thu, 09 Jun 2022 17:24:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Jun 2022 17:24:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 09 Jun 2022 17:24:52 GMT
USER odoo
# Thu, 09 Jun 2022 17:24:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Jun 2022 17:24:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c79567322b70756577efd1f8dcfa0263c984e263011e9803a7cda6aba5173a5`  
		Last Modified: Sat, 28 May 2022 12:09:33 GMT  
		Size: 207.1 MB (207143382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a85e75296e74df756190aea4b584b8e8697311966131e1f25a32ab750c6a6c`  
		Last Modified: Sat, 28 May 2022 12:09:11 GMT  
		Size: 13.4 MB (13442815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3489e5884bd67ef88e775a66acb08289f084239dc3fc159caa11154b5f40f2`  
		Last Modified: Sat, 28 May 2022 12:09:08 GMT  
		Size: 480.5 KB (480504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8fd9b0159d413bd33deb24a38e4ebf2ac9968908f45f3eecdb9685428826ad`  
		Last Modified: Thu, 09 Jun 2022 17:27:20 GMT  
		Size: 291.9 MB (291897486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4e760cb83fe70259cc440c48df9fe604a0a84d96c82954cd679a2e01420060`  
		Last Modified: Thu, 09 Jun 2022 17:26:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b719ad13b3873ac0239435ed43e215fb811eab0fb099472d4293b216c033d7`  
		Last Modified: Thu, 09 Jun 2022 17:26:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852ecf2169d22f141d9abbe53cfb5edb3535bea2942ecb1ae2af7ea42ff23f1a`  
		Last Modified: Thu, 09 Jun 2022 17:26:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc71052ec405bb81812bbbcdab2cd604ae5e31d5fe1555981b0be49eb8fbee1f`  
		Last Modified: Thu, 09 Jun 2022 17:26:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:dd9fe1c3102a5d58d0955439ad33c840e10f029a6b8aa22097af70370949bc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:66e7705fde3d2c1948411b481d6a322620c9b43798bdbae4219fbe9c74cc9a5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.3 MB (530313619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b8d503807542b8832204c6e2c346e83e8aa5be75e11be66adf088b2cf2c263`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:02:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:03:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:03:12 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:03:12 GMT
ENV ODOO_VERSION=14.0
# Thu, 09 Jun 2022 17:22:04 GMT
ARG ODOO_RELEASE=20220609
# Thu, 09 Jun 2022 17:22:04 GMT
ARG ODOO_SHA=9587d138e05cac1d41cfb467adc6c034e842ca55
# Thu, 09 Jun 2022 17:23:19 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=9587d138e05cac1d41cfb467adc6c034e842ca55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 09 Jun 2022 17:23:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 09 Jun 2022 17:23:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 09 Jun 2022 17:23:23 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=9587d138e05cac1d41cfb467adc6c034e842ca55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 09 Jun 2022 17:23:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Jun 2022 17:23:24 GMT
EXPOSE 8069 8071 8072
# Thu, 09 Jun 2022 17:23:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Jun 2022 17:23:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 09 Jun 2022 17:23:24 GMT
USER odoo
# Thu, 09 Jun 2022 17:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Jun 2022 17:23:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608dd6a1d283847f2f81e849d0bc623071e8222593eee6db00992e4b10b89700`  
		Last Modified: Sat, 28 May 2022 12:08:49 GMT  
		Size: 213.2 MB (213182131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca95c4836277ec91a64f63d069fe261f1155cd52d36b779818dc11814d993346`  
		Last Modified: Sat, 28 May 2022 12:08:27 GMT  
		Size: 13.4 MB (13445276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee21d359e137fb4b2d1a88d7964e3d51382ec95d462e59aea10e50328972a92`  
		Last Modified: Sat, 28 May 2022 12:08:24 GMT  
		Size: 480.4 KB (480424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660931180b9c73a1cdf913738aa4f47d752e887367bc938f28e26b16cdd6d006`  
		Last Modified: Thu, 09 Jun 2022 17:26:38 GMT  
		Size: 276.1 MB (276063182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f928ce1ffc0d7783b45ace225870f2b90ebf28e63ffdc8d28deffb44ec81c1`  
		Last Modified: Thu, 09 Jun 2022 17:26:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05aa24a6ff133f6c09d87ffac46b1946ee5ff6c95645ec0cce56818c89321d4f`  
		Last Modified: Thu, 09 Jun 2022 17:26:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17d0fb0d7b8bc86a859d79162ee64fe7ecb84324a8f69fa09a860c698e75f83`  
		Last Modified: Thu, 09 Jun 2022 17:26:05 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8facaac7c67b683e7c75125fd2073e767f175830264c765c5f3971a1c0fd40db`  
		Last Modified: Thu, 09 Jun 2022 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:dd9fe1c3102a5d58d0955439ad33c840e10f029a6b8aa22097af70370949bc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:66e7705fde3d2c1948411b481d6a322620c9b43798bdbae4219fbe9c74cc9a5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.3 MB (530313619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b8d503807542b8832204c6e2c346e83e8aa5be75e11be66adf088b2cf2c263`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:02:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:03:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:03:12 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:03:12 GMT
ENV ODOO_VERSION=14.0
# Thu, 09 Jun 2022 17:22:04 GMT
ARG ODOO_RELEASE=20220609
# Thu, 09 Jun 2022 17:22:04 GMT
ARG ODOO_SHA=9587d138e05cac1d41cfb467adc6c034e842ca55
# Thu, 09 Jun 2022 17:23:19 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=9587d138e05cac1d41cfb467adc6c034e842ca55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 09 Jun 2022 17:23:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 09 Jun 2022 17:23:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 09 Jun 2022 17:23:23 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=9587d138e05cac1d41cfb467adc6c034e842ca55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 09 Jun 2022 17:23:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Jun 2022 17:23:24 GMT
EXPOSE 8069 8071 8072
# Thu, 09 Jun 2022 17:23:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Jun 2022 17:23:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 09 Jun 2022 17:23:24 GMT
USER odoo
# Thu, 09 Jun 2022 17:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Jun 2022 17:23:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608dd6a1d283847f2f81e849d0bc623071e8222593eee6db00992e4b10b89700`  
		Last Modified: Sat, 28 May 2022 12:08:49 GMT  
		Size: 213.2 MB (213182131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca95c4836277ec91a64f63d069fe261f1155cd52d36b779818dc11814d993346`  
		Last Modified: Sat, 28 May 2022 12:08:27 GMT  
		Size: 13.4 MB (13445276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee21d359e137fb4b2d1a88d7964e3d51382ec95d462e59aea10e50328972a92`  
		Last Modified: Sat, 28 May 2022 12:08:24 GMT  
		Size: 480.4 KB (480424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660931180b9c73a1cdf913738aa4f47d752e887367bc938f28e26b16cdd6d006`  
		Last Modified: Thu, 09 Jun 2022 17:26:38 GMT  
		Size: 276.1 MB (276063182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f928ce1ffc0d7783b45ace225870f2b90ebf28e63ffdc8d28deffb44ec81c1`  
		Last Modified: Thu, 09 Jun 2022 17:26:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05aa24a6ff133f6c09d87ffac46b1946ee5ff6c95645ec0cce56818c89321d4f`  
		Last Modified: Thu, 09 Jun 2022 17:26:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17d0fb0d7b8bc86a859d79162ee64fe7ecb84324a8f69fa09a860c698e75f83`  
		Last Modified: Thu, 09 Jun 2022 17:26:05 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8facaac7c67b683e7c75125fd2073e767f175830264c765c5f3971a1c0fd40db`  
		Last Modified: Thu, 09 Jun 2022 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:920c92a83e4296fd9784feaba81e8fbca6ede2287d5632c809acb9c736c9d4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:ecb1104978782145a545e14c133bc105f5da850ac9fbf736974647299804a6cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555587862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8625290a8058ee8cd7c24ece1cf6444f1c4a6f3fd3b62974470e4c81de5b1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Thu, 09 Jun 2022 17:19:56 GMT
ARG ODOO_RELEASE=20220609
# Thu, 09 Jun 2022 17:19:56 GMT
ARG ODOO_SHA=5e30aa22df2239ecf42092b48fedcef72a98ed54
# Thu, 09 Jun 2022 17:21:56 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=5e30aa22df2239ecf42092b48fedcef72a98ed54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 09 Jun 2022 17:22:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 09 Jun 2022 17:22:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 09 Jun 2022 17:22:01 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=5e30aa22df2239ecf42092b48fedcef72a98ed54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 09 Jun 2022 17:22:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Jun 2022 17:22:01 GMT
EXPOSE 8069 8071 8072
# Thu, 09 Jun 2022 17:22:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Jun 2022 17:22:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 09 Jun 2022 17:22:01 GMT
USER odoo
# Thu, 09 Jun 2022 17:22:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Jun 2022 17:22:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e84c5a753af1624f828e4b558f0cf93ad16cfcbaf8340c6af7e5159887976e8`  
		Last Modified: Thu, 09 Jun 2022 17:25:51 GMT  
		Size: 300.9 MB (300910267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81629cb1c41be6a55ef6fd82773fa097b36199bef366cedaab9ad567ef3ee5c0`  
		Last Modified: Thu, 09 Jun 2022 17:25:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4154443c1361ed1053f4759849e67ddc8dc00658b5699487711547d1d57315`  
		Last Modified: Thu, 09 Jun 2022 17:25:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d65d5eb87fa89f35dcc527ef6cca7e1b0129c7a5c4192a2432eae334ab6005`  
		Last Modified: Thu, 09 Jun 2022 17:25:17 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab343bdb929dfac34335fce48e30baeb4de4e63e28b5f26165da5ae94012aa34`  
		Last Modified: Thu, 09 Jun 2022 17:25:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:920c92a83e4296fd9784feaba81e8fbca6ede2287d5632c809acb9c736c9d4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:ecb1104978782145a545e14c133bc105f5da850ac9fbf736974647299804a6cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555587862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8625290a8058ee8cd7c24ece1cf6444f1c4a6f3fd3b62974470e4c81de5b1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Thu, 09 Jun 2022 17:19:56 GMT
ARG ODOO_RELEASE=20220609
# Thu, 09 Jun 2022 17:19:56 GMT
ARG ODOO_SHA=5e30aa22df2239ecf42092b48fedcef72a98ed54
# Thu, 09 Jun 2022 17:21:56 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=5e30aa22df2239ecf42092b48fedcef72a98ed54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 09 Jun 2022 17:22:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 09 Jun 2022 17:22:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 09 Jun 2022 17:22:01 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=5e30aa22df2239ecf42092b48fedcef72a98ed54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 09 Jun 2022 17:22:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Jun 2022 17:22:01 GMT
EXPOSE 8069 8071 8072
# Thu, 09 Jun 2022 17:22:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Jun 2022 17:22:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 09 Jun 2022 17:22:01 GMT
USER odoo
# Thu, 09 Jun 2022 17:22:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Jun 2022 17:22:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e84c5a753af1624f828e4b558f0cf93ad16cfcbaf8340c6af7e5159887976e8`  
		Last Modified: Thu, 09 Jun 2022 17:25:51 GMT  
		Size: 300.9 MB (300910267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81629cb1c41be6a55ef6fd82773fa097b36199bef366cedaab9ad567ef3ee5c0`  
		Last Modified: Thu, 09 Jun 2022 17:25:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4154443c1361ed1053f4759849e67ddc8dc00658b5699487711547d1d57315`  
		Last Modified: Thu, 09 Jun 2022 17:25:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d65d5eb87fa89f35dcc527ef6cca7e1b0129c7a5c4192a2432eae334ab6005`  
		Last Modified: Thu, 09 Jun 2022 17:25:17 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab343bdb929dfac34335fce48e30baeb4de4e63e28b5f26165da5ae94012aa34`  
		Last Modified: Thu, 09 Jun 2022 17:25:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:920c92a83e4296fd9784feaba81e8fbca6ede2287d5632c809acb9c736c9d4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:ecb1104978782145a545e14c133bc105f5da850ac9fbf736974647299804a6cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555587862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8625290a8058ee8cd7c24ece1cf6444f1c4a6f3fd3b62974470e4c81de5b1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Thu, 09 Jun 2022 17:19:56 GMT
ARG ODOO_RELEASE=20220609
# Thu, 09 Jun 2022 17:19:56 GMT
ARG ODOO_SHA=5e30aa22df2239ecf42092b48fedcef72a98ed54
# Thu, 09 Jun 2022 17:21:56 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=5e30aa22df2239ecf42092b48fedcef72a98ed54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 09 Jun 2022 17:22:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 09 Jun 2022 17:22:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 09 Jun 2022 17:22:01 GMT
# ARGS: ODOO_RELEASE=20220609 ODOO_SHA=5e30aa22df2239ecf42092b48fedcef72a98ed54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 09 Jun 2022 17:22:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Jun 2022 17:22:01 GMT
EXPOSE 8069 8071 8072
# Thu, 09 Jun 2022 17:22:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Jun 2022 17:22:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 09 Jun 2022 17:22:01 GMT
USER odoo
# Thu, 09 Jun 2022 17:22:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Jun 2022 17:22:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e84c5a753af1624f828e4b558f0cf93ad16cfcbaf8340c6af7e5159887976e8`  
		Last Modified: Thu, 09 Jun 2022 17:25:51 GMT  
		Size: 300.9 MB (300910267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81629cb1c41be6a55ef6fd82773fa097b36199bef366cedaab9ad567ef3ee5c0`  
		Last Modified: Thu, 09 Jun 2022 17:25:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4154443c1361ed1053f4759849e67ddc8dc00658b5699487711547d1d57315`  
		Last Modified: Thu, 09 Jun 2022 17:25:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d65d5eb87fa89f35dcc527ef6cca7e1b0129c7a5c4192a2432eae334ab6005`  
		Last Modified: Thu, 09 Jun 2022 17:25:17 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab343bdb929dfac34335fce48e30baeb4de4e63e28b5f26165da5ae94012aa34`  
		Last Modified: Thu, 09 Jun 2022 17:25:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
