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
$ docker pull odoo@sha256:e08a0ce6c4b428cbe1ca618f086e890e6a982f1afe39db923fcc6be966802ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11` - linux; amd64

```console
$ docker pull odoo@sha256:3500bae0159752b4b82f054f49ba2b2688eed5f7b4cb2a837c0038904c7043db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385946558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc306783466042e41bb3e7fe37d710159e4381262acc177a6b857994797bad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:04:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 31 Mar 2020 04:04:32 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 04:04:33 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 31 Mar 2020 04:07:18 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 31 Mar 2020 04:07:32 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:09:32 GMT
ENV ODOO_VERSION=11.0
# Tue, 31 Mar 2020 04:09:32 GMT
ARG ODOO_RELEASE=20200121
# Tue, 31 Mar 2020 04:09:32 GMT
ARG ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
# Tue, 31 Mar 2020 04:13:11 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 Mar 2020 04:13:13 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Tue, 31 Mar 2020 04:13:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 Mar 2020 04:13:15 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 Mar 2020 04:13:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 Mar 2020 04:13:15 GMT
EXPOSE 8069 8071
# Tue, 31 Mar 2020 04:13:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 Mar 2020 04:13:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 Mar 2020 04:13:16 GMT
USER odoo
# Tue, 31 Mar 2020 04:13:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 04:13:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716f278f189e7d52251649c3ee018dda0bd5ae8a3e46501dba1026c6c25bdb77`  
		Last Modified: Tue, 31 Mar 2020 04:14:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1372a7b3be5b21deec35a974816d7348490522f302e3d1201f7e0739ea5377d0`  
		Last Modified: Tue, 31 Mar 2020 04:15:23 GMT  
		Size: 219.7 MB (219650632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcade1a85f327efac717341f4f7b4c7ffa1c79427f32ce8e71dce59e873b1eba`  
		Last Modified: Tue, 31 Mar 2020 04:14:48 GMT  
		Size: 2.3 MB (2346281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f35e6104d10c04ac1cb963569cc5ba9ec6edc31d8316f6f0d592f85db14d98f`  
		Last Modified: Tue, 31 Mar 2020 04:15:57 GMT  
		Size: 141.4 MB (141433636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceac2eb74ea4bbb8ae75e7bdefc3597cdeb7fecfe26fe90bac5d2639f6756f`  
		Last Modified: Tue, 31 Mar 2020 04:15:28 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9cc1b8e411ea64de7a0150d79fe72d9cc101feb4fd27496acd482a9273e707`  
		Last Modified: Tue, 31 Mar 2020 04:15:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271bc3f8b066510cd9d5f1e9982d0c10e5c1ad6dc774159be7b9bcf716effe78`  
		Last Modified: Tue, 31 Mar 2020 04:15:28 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc030d8b473d8444b850d0290f48aff9e45bb1e0923d801a8aa95266c0f589db`  
		Last Modified: Tue, 31 Mar 2020 04:15:28 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11.0`

```console
$ docker pull odoo@sha256:e08a0ce6c4b428cbe1ca618f086e890e6a982f1afe39db923fcc6be966802ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11.0` - linux; amd64

```console
$ docker pull odoo@sha256:3500bae0159752b4b82f054f49ba2b2688eed5f7b4cb2a837c0038904c7043db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385946558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc306783466042e41bb3e7fe37d710159e4381262acc177a6b857994797bad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:04:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 31 Mar 2020 04:04:32 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 04:04:33 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 31 Mar 2020 04:07:18 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 31 Mar 2020 04:07:32 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:09:32 GMT
ENV ODOO_VERSION=11.0
# Tue, 31 Mar 2020 04:09:32 GMT
ARG ODOO_RELEASE=20200121
# Tue, 31 Mar 2020 04:09:32 GMT
ARG ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
# Tue, 31 Mar 2020 04:13:11 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 Mar 2020 04:13:13 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Tue, 31 Mar 2020 04:13:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 Mar 2020 04:13:15 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 Mar 2020 04:13:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 Mar 2020 04:13:15 GMT
EXPOSE 8069 8071
# Tue, 31 Mar 2020 04:13:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 Mar 2020 04:13:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 Mar 2020 04:13:16 GMT
USER odoo
# Tue, 31 Mar 2020 04:13:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 04:13:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716f278f189e7d52251649c3ee018dda0bd5ae8a3e46501dba1026c6c25bdb77`  
		Last Modified: Tue, 31 Mar 2020 04:14:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1372a7b3be5b21deec35a974816d7348490522f302e3d1201f7e0739ea5377d0`  
		Last Modified: Tue, 31 Mar 2020 04:15:23 GMT  
		Size: 219.7 MB (219650632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcade1a85f327efac717341f4f7b4c7ffa1c79427f32ce8e71dce59e873b1eba`  
		Last Modified: Tue, 31 Mar 2020 04:14:48 GMT  
		Size: 2.3 MB (2346281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f35e6104d10c04ac1cb963569cc5ba9ec6edc31d8316f6f0d592f85db14d98f`  
		Last Modified: Tue, 31 Mar 2020 04:15:57 GMT  
		Size: 141.4 MB (141433636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ceac2eb74ea4bbb8ae75e7bdefc3597cdeb7fecfe26fe90bac5d2639f6756f`  
		Last Modified: Tue, 31 Mar 2020 04:15:28 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9cc1b8e411ea64de7a0150d79fe72d9cc101feb4fd27496acd482a9273e707`  
		Last Modified: Tue, 31 Mar 2020 04:15:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271bc3f8b066510cd9d5f1e9982d0c10e5c1ad6dc774159be7b9bcf716effe78`  
		Last Modified: Tue, 31 Mar 2020 04:15:28 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc030d8b473d8444b850d0290f48aff9e45bb1e0923d801a8aa95266c0f589db`  
		Last Modified: Tue, 31 Mar 2020 04:15:28 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12`

```console
$ docker pull odoo@sha256:bf86bb33b9b06adcd06efbb96422f3450c23f7b716f9ef8f5a5dd49d515885ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:88cc016ea24e76ba9ebc8147e0f2247a85fb783b81436de334198f3865388440
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.9 MB (399884726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b367fc436346f6db067a498da657943dca452b292b3d6f59a8b15f4acc03a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:04:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 31 Mar 2020 04:04:32 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 04:04:33 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 31 Mar 2020 04:07:18 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 31 Mar 2020 04:07:32 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:07:56 GMT
RUN set -x;    echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && export GNUPGHOME="$(mktemp -d)"     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:07:56 GMT
ENV ODOO_VERSION=12.0
# Tue, 31 Mar 2020 04:07:57 GMT
ARG ODOO_RELEASE=20200121
# Tue, 31 Mar 2020 04:07:57 GMT
ARG ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
# Tue, 31 Mar 2020 04:09:15 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 Mar 2020 04:09:16 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 31 Mar 2020 04:09:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 Mar 2020 04:09:17 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 Mar 2020 04:09:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 Mar 2020 04:09:17 GMT
EXPOSE 8069 8071
# Tue, 31 Mar 2020 04:09:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 Mar 2020 04:09:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 Mar 2020 04:09:18 GMT
USER odoo
# Tue, 31 Mar 2020 04:09:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 04:09:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716f278f189e7d52251649c3ee018dda0bd5ae8a3e46501dba1026c6c25bdb77`  
		Last Modified: Tue, 31 Mar 2020 04:14:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1372a7b3be5b21deec35a974816d7348490522f302e3d1201f7e0739ea5377d0`  
		Last Modified: Tue, 31 Mar 2020 04:15:23 GMT  
		Size: 219.7 MB (219650632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcade1a85f327efac717341f4f7b4c7ffa1c79427f32ce8e71dce59e873b1eba`  
		Last Modified: Tue, 31 Mar 2020 04:14:48 GMT  
		Size: 2.3 MB (2346281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e423264d8270dd16b5ac77f3f68977fee6190a8206503a27c923784c75aebf`  
		Last Modified: Tue, 31 Mar 2020 04:14:56 GMT  
		Size: 26.6 MB (26578294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b313eb8248b486b811780d8d2a7ba38427d3bfe606aec3a325f653faedfb032c`  
		Last Modified: Tue, 31 Mar 2020 04:15:22 GMT  
		Size: 128.8 MB (128793515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c982842c04be9abef173cebccdb964896a674d7e9e9f5f5242a111461c7b7321`  
		Last Modified: Tue, 31 Mar 2020 04:14:46 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175e27441e58dcf1c25486d6f511171223378b37df6a1ff6c2e1e8fbaa41e18`  
		Last Modified: Tue, 31 Mar 2020 04:14:46 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb7606e77b2266b5c961b41575dffe380d4af7da7a0e3e9062e30f136a52752`  
		Last Modified: Tue, 31 Mar 2020 04:14:46 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb09cebb7fbda495cd8998947ac09776879e542b59fcb50aea0d09f145e819db`  
		Last Modified: Tue, 31 Mar 2020 04:14:46 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:bf86bb33b9b06adcd06efbb96422f3450c23f7b716f9ef8f5a5dd49d515885ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:88cc016ea24e76ba9ebc8147e0f2247a85fb783b81436de334198f3865388440
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.9 MB (399884726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b367fc436346f6db067a498da657943dca452b292b3d6f59a8b15f4acc03a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:04:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 31 Mar 2020 04:04:32 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 04:04:33 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 31 Mar 2020 04:07:18 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 31 Mar 2020 04:07:32 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:07:56 GMT
RUN set -x;    echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && export GNUPGHOME="$(mktemp -d)"     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:07:56 GMT
ENV ODOO_VERSION=12.0
# Tue, 31 Mar 2020 04:07:57 GMT
ARG ODOO_RELEASE=20200121
# Tue, 31 Mar 2020 04:07:57 GMT
ARG ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
# Tue, 31 Mar 2020 04:09:15 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 Mar 2020 04:09:16 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 31 Mar 2020 04:09:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 Mar 2020 04:09:17 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 Mar 2020 04:09:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 Mar 2020 04:09:17 GMT
EXPOSE 8069 8071
# Tue, 31 Mar 2020 04:09:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 Mar 2020 04:09:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 Mar 2020 04:09:18 GMT
USER odoo
# Tue, 31 Mar 2020 04:09:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 04:09:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716f278f189e7d52251649c3ee018dda0bd5ae8a3e46501dba1026c6c25bdb77`  
		Last Modified: Tue, 31 Mar 2020 04:14:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1372a7b3be5b21deec35a974816d7348490522f302e3d1201f7e0739ea5377d0`  
		Last Modified: Tue, 31 Mar 2020 04:15:23 GMT  
		Size: 219.7 MB (219650632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcade1a85f327efac717341f4f7b4c7ffa1c79427f32ce8e71dce59e873b1eba`  
		Last Modified: Tue, 31 Mar 2020 04:14:48 GMT  
		Size: 2.3 MB (2346281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e423264d8270dd16b5ac77f3f68977fee6190a8206503a27c923784c75aebf`  
		Last Modified: Tue, 31 Mar 2020 04:14:56 GMT  
		Size: 26.6 MB (26578294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b313eb8248b486b811780d8d2a7ba38427d3bfe606aec3a325f653faedfb032c`  
		Last Modified: Tue, 31 Mar 2020 04:15:22 GMT  
		Size: 128.8 MB (128793515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c982842c04be9abef173cebccdb964896a674d7e9e9f5f5242a111461c7b7321`  
		Last Modified: Tue, 31 Mar 2020 04:14:46 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175e27441e58dcf1c25486d6f511171223378b37df6a1ff6c2e1e8fbaa41e18`  
		Last Modified: Tue, 31 Mar 2020 04:14:46 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb7606e77b2266b5c961b41575dffe380d4af7da7a0e3e9062e30f136a52752`  
		Last Modified: Tue, 31 Mar 2020 04:14:46 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb09cebb7fbda495cd8998947ac09776879e542b59fcb50aea0d09f145e819db`  
		Last Modified: Tue, 31 Mar 2020 04:14:46 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:e5a4733e99ac2bbfb5a45dc18ddb4aa6419c46ba9174fc5b1642e20b2ab0a1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:3491c33af3989c1b7b624e5e17b3298f33d9f1c28035715681ef0204c30a65a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.4 MB (376397097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f547a7a4c1f2715995bb9722403e94129e6f68c60fc894861682fa5f92285706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:01:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 31 Mar 2020 04:01:00 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 04:02:33 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 31 Mar 2020 04:02:45 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:02:50 GMT
RUN set -x;     npm install -g rtlcss
# Tue, 31 Mar 2020 04:02:51 GMT
ENV ODOO_VERSION=13.0
# Tue, 31 Mar 2020 04:02:51 GMT
ARG ODOO_RELEASE=20200121
# Tue, 31 Mar 2020 04:02:51 GMT
ARG ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
# Tue, 31 Mar 2020 04:04:11 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 Mar 2020 04:04:13 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 31 Mar 2020 04:04:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 Mar 2020 04:04:15 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 Mar 2020 04:04:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 Mar 2020 04:04:15 GMT
EXPOSE 8069 8071
# Tue, 31 Mar 2020 04:04:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 Mar 2020 04:04:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 Mar 2020 04:04:16 GMT
USER odoo
# Tue, 31 Mar 2020 04:04:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 04:04:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7075ed407fc9f7da2b7eeec4bb67cecb1c74d191d5ec07f93677d16017043e2`  
		Last Modified: Tue, 31 Mar 2020 04:14:36 GMT  
		Size: 203.6 MB (203559197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcba7648a2ee187728f9fe05ef76ae6372ff633f754b3f0b967ced94b32869e`  
		Last Modified: Tue, 31 Mar 2020 04:13:42 GMT  
		Size: 2.3 MB (2332527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e7f1d05f24bb1e4bd87f8ce71daaa4bf39bcaae92ba0398a18818f41a8e406`  
		Last Modified: Tue, 31 Mar 2020 04:13:41 GMT  
		Size: 1.1 MB (1086097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef581070ef713deb946275e977f0930686ead23255b5971abd49f397c2e47ec`  
		Last Modified: Tue, 31 Mar 2020 04:14:39 GMT  
		Size: 142.3 MB (142325014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2556215a8963862f7f301294913ceaf4e8afab9638ae5c0072d72bfb566b1c`  
		Last Modified: Tue, 31 Mar 2020 04:13:40 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a3b61b574e9657b6c1c736a016fae773baf0a4b1a38cebc6abcc8bde2b77d`  
		Last Modified: Tue, 31 Mar 2020 04:13:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080ef099b45f5388b501670b4bd342db4efff4539c7277be793a784a82604db6`  
		Last Modified: Tue, 31 Mar 2020 04:13:40 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff511e68776648b4d7a0b11050e4083ed05860111991f89ddc1572b251cf663`  
		Last Modified: Tue, 31 Mar 2020 04:13:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:e5a4733e99ac2bbfb5a45dc18ddb4aa6419c46ba9174fc5b1642e20b2ab0a1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:3491c33af3989c1b7b624e5e17b3298f33d9f1c28035715681ef0204c30a65a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.4 MB (376397097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f547a7a4c1f2715995bb9722403e94129e6f68c60fc894861682fa5f92285706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:01:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 31 Mar 2020 04:01:00 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 04:02:33 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 31 Mar 2020 04:02:45 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:02:50 GMT
RUN set -x;     npm install -g rtlcss
# Tue, 31 Mar 2020 04:02:51 GMT
ENV ODOO_VERSION=13.0
# Tue, 31 Mar 2020 04:02:51 GMT
ARG ODOO_RELEASE=20200121
# Tue, 31 Mar 2020 04:02:51 GMT
ARG ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
# Tue, 31 Mar 2020 04:04:11 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 Mar 2020 04:04:13 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 31 Mar 2020 04:04:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 Mar 2020 04:04:15 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 Mar 2020 04:04:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 Mar 2020 04:04:15 GMT
EXPOSE 8069 8071
# Tue, 31 Mar 2020 04:04:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 Mar 2020 04:04:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 Mar 2020 04:04:16 GMT
USER odoo
# Tue, 31 Mar 2020 04:04:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 04:04:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7075ed407fc9f7da2b7eeec4bb67cecb1c74d191d5ec07f93677d16017043e2`  
		Last Modified: Tue, 31 Mar 2020 04:14:36 GMT  
		Size: 203.6 MB (203559197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcba7648a2ee187728f9fe05ef76ae6372ff633f754b3f0b967ced94b32869e`  
		Last Modified: Tue, 31 Mar 2020 04:13:42 GMT  
		Size: 2.3 MB (2332527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e7f1d05f24bb1e4bd87f8ce71daaa4bf39bcaae92ba0398a18818f41a8e406`  
		Last Modified: Tue, 31 Mar 2020 04:13:41 GMT  
		Size: 1.1 MB (1086097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef581070ef713deb946275e977f0930686ead23255b5971abd49f397c2e47ec`  
		Last Modified: Tue, 31 Mar 2020 04:14:39 GMT  
		Size: 142.3 MB (142325014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2556215a8963862f7f301294913ceaf4e8afab9638ae5c0072d72bfb566b1c`  
		Last Modified: Tue, 31 Mar 2020 04:13:40 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a3b61b574e9657b6c1c736a016fae773baf0a4b1a38cebc6abcc8bde2b77d`  
		Last Modified: Tue, 31 Mar 2020 04:13:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080ef099b45f5388b501670b4bd342db4efff4539c7277be793a784a82604db6`  
		Last Modified: Tue, 31 Mar 2020 04:13:40 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff511e68776648b4d7a0b11050e4083ed05860111991f89ddc1572b251cf663`  
		Last Modified: Tue, 31 Mar 2020 04:13:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:e5a4733e99ac2bbfb5a45dc18ddb4aa6419c46ba9174fc5b1642e20b2ab0a1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:3491c33af3989c1b7b624e5e17b3298f33d9f1c28035715681ef0204c30a65a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.4 MB (376397097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f547a7a4c1f2715995bb9722403e94129e6f68c60fc894861682fa5f92285706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:01:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 31 Mar 2020 04:01:00 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 04:02:33 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 31 Mar 2020 04:02:45 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:02:50 GMT
RUN set -x;     npm install -g rtlcss
# Tue, 31 Mar 2020 04:02:51 GMT
ENV ODOO_VERSION=13.0
# Tue, 31 Mar 2020 04:02:51 GMT
ARG ODOO_RELEASE=20200121
# Tue, 31 Mar 2020 04:02:51 GMT
ARG ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
# Tue, 31 Mar 2020 04:04:11 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 31 Mar 2020 04:04:13 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 31 Mar 2020 04:04:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 31 Mar 2020 04:04:15 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 31 Mar 2020 04:04:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 31 Mar 2020 04:04:15 GMT
EXPOSE 8069 8071
# Tue, 31 Mar 2020 04:04:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 31 Mar 2020 04:04:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 31 Mar 2020 04:04:16 GMT
USER odoo
# Tue, 31 Mar 2020 04:04:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 04:04:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7075ed407fc9f7da2b7eeec4bb67cecb1c74d191d5ec07f93677d16017043e2`  
		Last Modified: Tue, 31 Mar 2020 04:14:36 GMT  
		Size: 203.6 MB (203559197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcba7648a2ee187728f9fe05ef76ae6372ff633f754b3f0b967ced94b32869e`  
		Last Modified: Tue, 31 Mar 2020 04:13:42 GMT  
		Size: 2.3 MB (2332527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e7f1d05f24bb1e4bd87f8ce71daaa4bf39bcaae92ba0398a18818f41a8e406`  
		Last Modified: Tue, 31 Mar 2020 04:13:41 GMT  
		Size: 1.1 MB (1086097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef581070ef713deb946275e977f0930686ead23255b5971abd49f397c2e47ec`  
		Last Modified: Tue, 31 Mar 2020 04:14:39 GMT  
		Size: 142.3 MB (142325014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2556215a8963862f7f301294913ceaf4e8afab9638ae5c0072d72bfb566b1c`  
		Last Modified: Tue, 31 Mar 2020 04:13:40 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a3b61b574e9657b6c1c736a016fae773baf0a4b1a38cebc6abcc8bde2b77d`  
		Last Modified: Tue, 31 Mar 2020 04:13:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080ef099b45f5388b501670b4bd342db4efff4539c7277be793a784a82604db6`  
		Last Modified: Tue, 31 Mar 2020 04:13:40 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff511e68776648b4d7a0b11050e4083ed05860111991f89ddc1572b251cf663`  
		Last Modified: Tue, 31 Mar 2020 04:13:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
