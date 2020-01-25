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
$ docker pull odoo@sha256:a09d4a58279e6d08a7139f3a8930d77689229498da80573944454b682c065ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11` - linux; amd64

```console
$ docker pull odoo@sha256:83902ae8ab7a51e17594adef667bc1601309c2c2841cd37409d6bfe7f56a2715
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.8 MB (385848866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b64de883328ecc6cb58223065ac5972298cd0ab4b9080e783c8c39dd42004e`
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
# Sat, 25 Jan 2020 01:26:09 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 25 Jan 2020 01:26:18 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 25 Jan 2020 01:27:25 GMT
ENV ODOO_VERSION=11.0
# Sat, 25 Jan 2020 01:27:25 GMT
ARG ODOO_RELEASE=20200121
# Sat, 25 Jan 2020 01:27:26 GMT
ARG ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
# Sat, 25 Jan 2020 01:28:10 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 25 Jan 2020 01:28:11 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Sat, 25 Jan 2020 01:28:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 25 Jan 2020 01:28:12 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 25 Jan 2020 01:28:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 25 Jan 2020 01:28:12 GMT
EXPOSE 8069 8071
# Sat, 25 Jan 2020 01:28:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 25 Jan 2020 01:28:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 25 Jan 2020 01:28:13 GMT
USER odoo
# Sat, 25 Jan 2020 01:28:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:28:13 GMT
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
	-	`sha256:56a2ef2902cdd18995eafb68b205795af8fe45614fe9da08a1d16960257f2b0b`  
		Last Modified: Sat, 25 Jan 2020 01:29:31 GMT  
		Size: 219.6 MB (219649821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f37827b0e68782059757d74867a60b2b22556cb0cadc892599e4140b01b05b`  
		Last Modified: Sat, 25 Jan 2020 01:29:01 GMT  
		Size: 2.2 MB (2246055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f89d87aefaf00a05933d454f744de4fd41ec2e1c986925c179c9e98d08937`  
		Last Modified: Sat, 25 Jan 2020 01:30:10 GMT  
		Size: 141.4 MB (141425746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e8bc6a61b952d6657272a04d4445bdbc2918b965c8d70e8c12ce00b1015fdd`  
		Last Modified: Sat, 25 Jan 2020 01:29:45 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d98db6de910fc142a204bd25c53b59a64c68b54b6f23b55771c6daa5f0eab4`  
		Last Modified: Sat, 25 Jan 2020 01:29:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1763889c8825ad1ba469c7a36a4f0a0579fe7c3080a8957d5c579422970bc840`  
		Last Modified: Sat, 25 Jan 2020 01:29:45 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d22d22ebc7674db4d95eb5c3259f585a10838f57d22d9195b1e44ec8b61578`  
		Last Modified: Sat, 25 Jan 2020 01:29:45 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11.0`

```console
$ docker pull odoo@sha256:a09d4a58279e6d08a7139f3a8930d77689229498da80573944454b682c065ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11.0` - linux; amd64

```console
$ docker pull odoo@sha256:83902ae8ab7a51e17594adef667bc1601309c2c2841cd37409d6bfe7f56a2715
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.8 MB (385848866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b64de883328ecc6cb58223065ac5972298cd0ab4b9080e783c8c39dd42004e`
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
# Sat, 25 Jan 2020 01:26:09 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 25 Jan 2020 01:26:18 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 25 Jan 2020 01:27:25 GMT
ENV ODOO_VERSION=11.0
# Sat, 25 Jan 2020 01:27:25 GMT
ARG ODOO_RELEASE=20200121
# Sat, 25 Jan 2020 01:27:26 GMT
ARG ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
# Sat, 25 Jan 2020 01:28:10 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 25 Jan 2020 01:28:11 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Sat, 25 Jan 2020 01:28:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 25 Jan 2020 01:28:12 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 25 Jan 2020 01:28:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 25 Jan 2020 01:28:12 GMT
EXPOSE 8069 8071
# Sat, 25 Jan 2020 01:28:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 25 Jan 2020 01:28:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 25 Jan 2020 01:28:13 GMT
USER odoo
# Sat, 25 Jan 2020 01:28:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:28:13 GMT
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
	-	`sha256:56a2ef2902cdd18995eafb68b205795af8fe45614fe9da08a1d16960257f2b0b`  
		Last Modified: Sat, 25 Jan 2020 01:29:31 GMT  
		Size: 219.6 MB (219649821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f37827b0e68782059757d74867a60b2b22556cb0cadc892599e4140b01b05b`  
		Last Modified: Sat, 25 Jan 2020 01:29:01 GMT  
		Size: 2.2 MB (2246055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f89d87aefaf00a05933d454f744de4fd41ec2e1c986925c179c9e98d08937`  
		Last Modified: Sat, 25 Jan 2020 01:30:10 GMT  
		Size: 141.4 MB (141425746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e8bc6a61b952d6657272a04d4445bdbc2918b965c8d70e8c12ce00b1015fdd`  
		Last Modified: Sat, 25 Jan 2020 01:29:45 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d98db6de910fc142a204bd25c53b59a64c68b54b6f23b55771c6daa5f0eab4`  
		Last Modified: Sat, 25 Jan 2020 01:29:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1763889c8825ad1ba469c7a36a4f0a0579fe7c3080a8957d5c579422970bc840`  
		Last Modified: Sat, 25 Jan 2020 01:29:45 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d22d22ebc7674db4d95eb5c3259f585a10838f57d22d9195b1e44ec8b61578`  
		Last Modified: Sat, 25 Jan 2020 01:29:45 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12`

```console
$ docker pull odoo@sha256:9b7097353f78402d05120b2c3f333ca4a4e5925c4494ed13033c7099bea8931e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:f396d5d1d9ad2bf53b9b164bc98fda8d88923a302e573509040085306ae3e261
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.8 MB (399771653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b015838c1ab370d6c4b9a8bdb7f6dce00261028dab1dad965ae1bc158dd9dfcf`
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
# Sat, 25 Jan 2020 01:26:09 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 25 Jan 2020 01:26:18 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 25 Jan 2020 01:26:31 GMT
RUN set -x;    echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && export GNUPGHOME="$(mktemp -d)"     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 25 Jan 2020 01:26:32 GMT
ENV ODOO_VERSION=12.0
# Sat, 25 Jan 2020 01:26:32 GMT
ARG ODOO_RELEASE=20200121
# Sat, 25 Jan 2020 01:26:32 GMT
ARG ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
# Sat, 25 Jan 2020 01:27:18 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 25 Jan 2020 01:27:19 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 25 Jan 2020 01:27:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 25 Jan 2020 01:27:19 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 25 Jan 2020 01:27:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 25 Jan 2020 01:27:20 GMT
EXPOSE 8069 8071
# Sat, 25 Jan 2020 01:27:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 25 Jan 2020 01:27:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 25 Jan 2020 01:27:20 GMT
USER odoo
# Sat, 25 Jan 2020 01:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:27:21 GMT
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
	-	`sha256:56a2ef2902cdd18995eafb68b205795af8fe45614fe9da08a1d16960257f2b0b`  
		Last Modified: Sat, 25 Jan 2020 01:29:31 GMT  
		Size: 219.6 MB (219649821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f37827b0e68782059757d74867a60b2b22556cb0cadc892599e4140b01b05b`  
		Last Modified: Sat, 25 Jan 2020 01:29:01 GMT  
		Size: 2.2 MB (2246055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d2f6315e14866ecd67dc92b840e2f487d19c7cb499f6435aef9482fb9b857e`  
		Last Modified: Sat, 25 Jan 2020 01:29:07 GMT  
		Size: 26.6 MB (26557299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b455258dbd6194acebc4e579b490b188dbf7947a3cddc268cb7bdf0718c1c2d`  
		Last Modified: Sat, 25 Jan 2020 01:29:30 GMT  
		Size: 128.8 MB (128791236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d7b453b3d518f3a94c55578e57c086e0cdc4c1cbd556033feb51ca10f0b5ab`  
		Last Modified: Sat, 25 Jan 2020 01:28:59 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3419aaa6458703f10898783f8b0b5c080822c63897f427c0d450bbe67e39cc`  
		Last Modified: Sat, 25 Jan 2020 01:29:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1361ed1974e087c7a1be260d7726b60975e98662183bf21ade48b809d8005543`  
		Last Modified: Sat, 25 Jan 2020 01:29:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626fbe225183a2c14d2224c6d1cc8ff33301735a9e82223b74e4ba13c0f06e40`  
		Last Modified: Sat, 25 Jan 2020 01:28:59 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:9b7097353f78402d05120b2c3f333ca4a4e5925c4494ed13033c7099bea8931e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:f396d5d1d9ad2bf53b9b164bc98fda8d88923a302e573509040085306ae3e261
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.8 MB (399771653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b015838c1ab370d6c4b9a8bdb7f6dce00261028dab1dad965ae1bc158dd9dfcf`
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
# Sat, 25 Jan 2020 01:26:09 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 25 Jan 2020 01:26:18 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 25 Jan 2020 01:26:31 GMT
RUN set -x;    echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && export GNUPGHOME="$(mktemp -d)"     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 25 Jan 2020 01:26:32 GMT
ENV ODOO_VERSION=12.0
# Sat, 25 Jan 2020 01:26:32 GMT
ARG ODOO_RELEASE=20200121
# Sat, 25 Jan 2020 01:26:32 GMT
ARG ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
# Sat, 25 Jan 2020 01:27:18 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 25 Jan 2020 01:27:19 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 25 Jan 2020 01:27:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 25 Jan 2020 01:27:19 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 25 Jan 2020 01:27:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 25 Jan 2020 01:27:20 GMT
EXPOSE 8069 8071
# Sat, 25 Jan 2020 01:27:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 25 Jan 2020 01:27:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 25 Jan 2020 01:27:20 GMT
USER odoo
# Sat, 25 Jan 2020 01:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:27:21 GMT
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
	-	`sha256:56a2ef2902cdd18995eafb68b205795af8fe45614fe9da08a1d16960257f2b0b`  
		Last Modified: Sat, 25 Jan 2020 01:29:31 GMT  
		Size: 219.6 MB (219649821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f37827b0e68782059757d74867a60b2b22556cb0cadc892599e4140b01b05b`  
		Last Modified: Sat, 25 Jan 2020 01:29:01 GMT  
		Size: 2.2 MB (2246055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d2f6315e14866ecd67dc92b840e2f487d19c7cb499f6435aef9482fb9b857e`  
		Last Modified: Sat, 25 Jan 2020 01:29:07 GMT  
		Size: 26.6 MB (26557299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b455258dbd6194acebc4e579b490b188dbf7947a3cddc268cb7bdf0718c1c2d`  
		Last Modified: Sat, 25 Jan 2020 01:29:30 GMT  
		Size: 128.8 MB (128791236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d7b453b3d518f3a94c55578e57c086e0cdc4c1cbd556033feb51ca10f0b5ab`  
		Last Modified: Sat, 25 Jan 2020 01:28:59 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3419aaa6458703f10898783f8b0b5c080822c63897f427c0d450bbe67e39cc`  
		Last Modified: Sat, 25 Jan 2020 01:29:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1361ed1974e087c7a1be260d7726b60975e98662183bf21ade48b809d8005543`  
		Last Modified: Sat, 25 Jan 2020 01:29:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626fbe225183a2c14d2224c6d1cc8ff33301735a9e82223b74e4ba13c0f06e40`  
		Last Modified: Sat, 25 Jan 2020 01:28:59 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:78a718fa783ae5b1702c86f614b6ef90782cda811f5360da15e048d7b02f497c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:721a8e0f0bf2ad3dfa0230848f81ddf10471b706d5258af69e3f9f8076321a40
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.3 MB (376262987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09778cb51e628e618b70e6cf9c5cfccf1f8aa29ac1107aa69ac1a045bc2f181`
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
# Sat, 25 Jan 2020 01:23:01 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 25 Jan 2020 01:23:07 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 25 Jan 2020 01:23:11 GMT
RUN set -x;     npm install -g rtlcss
# Sat, 25 Jan 2020 01:23:11 GMT
ENV ODOO_VERSION=13.0
# Sat, 25 Jan 2020 01:23:11 GMT
ARG ODOO_RELEASE=20200121
# Sat, 25 Jan 2020 01:23:11 GMT
ARG ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
# Sat, 25 Jan 2020 01:24:06 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 25 Jan 2020 01:24:07 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 25 Jan 2020 01:24:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 25 Jan 2020 01:24:08 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 25 Jan 2020 01:24:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 25 Jan 2020 01:24:08 GMT
EXPOSE 8069 8071
# Sat, 25 Jan 2020 01:24:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 25 Jan 2020 01:24:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 25 Jan 2020 01:24:09 GMT
USER odoo
# Sat, 25 Jan 2020 01:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:24:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1cd10c96a474f83c5fd7419147e972e18ea4108e3f17cca2c6dc708ddc5118`  
		Last Modified: Sat, 25 Jan 2020 01:28:54 GMT  
		Size: 203.5 MB (203545697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd0d53c1b9294e47686761ee22815ee089edad6b540f2a2b363e29278ee698f`  
		Last Modified: Sat, 25 Jan 2020 01:28:23 GMT  
		Size: 2.2 MB (2228700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a071a0125bdde3027331b1f1d2e0722a6322d9f6465250a063c8e37d0ccb4`  
		Last Modified: Sat, 25 Jan 2020 01:28:23 GMT  
		Size: 1.1 MB (1068678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4d664e87b6b28deb259311c8a17a63c76d7616653cc51d9c14ea6a023c2428`  
		Last Modified: Sat, 25 Jan 2020 01:28:54 GMT  
		Size: 142.3 MB (142325237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76373892e057bb3764d68494e47f2a771376a75ac2c0df9842733274527c96`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419c49cbf81dd3403efddecdc7fe620e3b9b59f532102910fc442c86e921c74`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2db78927a1ad8ca6abeda2e64fbba64bc6117d40b014e4193873b1d5c3ef08`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4c52286c8d051d9a6785b7aa0b3e4b12461229acdfec49ba4bafb95e432455`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:78a718fa783ae5b1702c86f614b6ef90782cda811f5360da15e048d7b02f497c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:721a8e0f0bf2ad3dfa0230848f81ddf10471b706d5258af69e3f9f8076321a40
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.3 MB (376262987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09778cb51e628e618b70e6cf9c5cfccf1f8aa29ac1107aa69ac1a045bc2f181`
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
# Sat, 25 Jan 2020 01:23:01 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 25 Jan 2020 01:23:07 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 25 Jan 2020 01:23:11 GMT
RUN set -x;     npm install -g rtlcss
# Sat, 25 Jan 2020 01:23:11 GMT
ENV ODOO_VERSION=13.0
# Sat, 25 Jan 2020 01:23:11 GMT
ARG ODOO_RELEASE=20200121
# Sat, 25 Jan 2020 01:23:11 GMT
ARG ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
# Sat, 25 Jan 2020 01:24:06 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 25 Jan 2020 01:24:07 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 25 Jan 2020 01:24:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 25 Jan 2020 01:24:08 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 25 Jan 2020 01:24:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 25 Jan 2020 01:24:08 GMT
EXPOSE 8069 8071
# Sat, 25 Jan 2020 01:24:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 25 Jan 2020 01:24:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 25 Jan 2020 01:24:09 GMT
USER odoo
# Sat, 25 Jan 2020 01:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:24:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1cd10c96a474f83c5fd7419147e972e18ea4108e3f17cca2c6dc708ddc5118`  
		Last Modified: Sat, 25 Jan 2020 01:28:54 GMT  
		Size: 203.5 MB (203545697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd0d53c1b9294e47686761ee22815ee089edad6b540f2a2b363e29278ee698f`  
		Last Modified: Sat, 25 Jan 2020 01:28:23 GMT  
		Size: 2.2 MB (2228700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a071a0125bdde3027331b1f1d2e0722a6322d9f6465250a063c8e37d0ccb4`  
		Last Modified: Sat, 25 Jan 2020 01:28:23 GMT  
		Size: 1.1 MB (1068678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4d664e87b6b28deb259311c8a17a63c76d7616653cc51d9c14ea6a023c2428`  
		Last Modified: Sat, 25 Jan 2020 01:28:54 GMT  
		Size: 142.3 MB (142325237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76373892e057bb3764d68494e47f2a771376a75ac2c0df9842733274527c96`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419c49cbf81dd3403efddecdc7fe620e3b9b59f532102910fc442c86e921c74`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2db78927a1ad8ca6abeda2e64fbba64bc6117d40b014e4193873b1d5c3ef08`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4c52286c8d051d9a6785b7aa0b3e4b12461229acdfec49ba4bafb95e432455`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:78a718fa783ae5b1702c86f614b6ef90782cda811f5360da15e048d7b02f497c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:721a8e0f0bf2ad3dfa0230848f81ddf10471b706d5258af69e3f9f8076321a40
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.3 MB (376262987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09778cb51e628e618b70e6cf9c5cfccf1f8aa29ac1107aa69ac1a045bc2f181`
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
# Sat, 25 Jan 2020 01:23:01 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 25 Jan 2020 01:23:07 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Sat, 25 Jan 2020 01:23:11 GMT
RUN set -x;     npm install -g rtlcss
# Sat, 25 Jan 2020 01:23:11 GMT
ENV ODOO_VERSION=13.0
# Sat, 25 Jan 2020 01:23:11 GMT
ARG ODOO_RELEASE=20200121
# Sat, 25 Jan 2020 01:23:11 GMT
ARG ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
# Sat, 25 Jan 2020 01:24:06 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 25 Jan 2020 01:24:07 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Sat, 25 Jan 2020 01:24:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 25 Jan 2020 01:24:08 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 25 Jan 2020 01:24:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 25 Jan 2020 01:24:08 GMT
EXPOSE 8069 8071
# Sat, 25 Jan 2020 01:24:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 25 Jan 2020 01:24:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 25 Jan 2020 01:24:09 GMT
USER odoo
# Sat, 25 Jan 2020 01:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:24:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1cd10c96a474f83c5fd7419147e972e18ea4108e3f17cca2c6dc708ddc5118`  
		Last Modified: Sat, 25 Jan 2020 01:28:54 GMT  
		Size: 203.5 MB (203545697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd0d53c1b9294e47686761ee22815ee089edad6b540f2a2b363e29278ee698f`  
		Last Modified: Sat, 25 Jan 2020 01:28:23 GMT  
		Size: 2.2 MB (2228700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2a071a0125bdde3027331b1f1d2e0722a6322d9f6465250a063c8e37d0ccb4`  
		Last Modified: Sat, 25 Jan 2020 01:28:23 GMT  
		Size: 1.1 MB (1068678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4d664e87b6b28deb259311c8a17a63c76d7616653cc51d9c14ea6a023c2428`  
		Last Modified: Sat, 25 Jan 2020 01:28:54 GMT  
		Size: 142.3 MB (142325237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76373892e057bb3764d68494e47f2a771376a75ac2c0df9842733274527c96`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419c49cbf81dd3403efddecdc7fe620e3b9b59f532102910fc442c86e921c74`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2db78927a1ad8ca6abeda2e64fbba64bc6117d40b014e4193873b1d5c3ef08`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4c52286c8d051d9a6785b7aa0b3e4b12461229acdfec49ba4bafb95e432455`  
		Last Modified: Sat, 25 Jan 2020 01:28:22 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
