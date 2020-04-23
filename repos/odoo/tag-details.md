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
$ docker pull odoo@sha256:7dd00695526a36c7dcdaca465b1ab17f10a60713db1a3965680a023f6b5b4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11` - linux; amd64

```console
$ docker pull odoo@sha256:9ae74debfc257f96870f4652916e6274bcbd7c72c9ead8b37b0e905e09a8059b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386116136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90453baffa0584c0949dbe3cccf86abf102a285d954b7e4d2ca474fcb9092e36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:51:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Apr 2020 13:51:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Apr 2020 13:51:50 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:51:51 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 23 Apr 2020 13:53:45 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Apr 2020 13:53:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:55:38 GMT
ENV ODOO_VERSION=11.0
# Thu, 23 Apr 2020 13:55:38 GMT
ARG ODOO_RELEASE=20200417
# Thu, 23 Apr 2020 13:55:38 GMT
ARG ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
# Thu, 23 Apr 2020 13:56:52 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb        && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Apr 2020 13:56:54 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Thu, 23 Apr 2020 13:56:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Apr 2020 13:56:56 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Apr 2020 13:56:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Apr 2020 13:56:56 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Apr 2020 13:56:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Apr 2020 13:56:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Apr 2020 13:56:57 GMT
USER odoo
# Thu, 23 Apr 2020 13:56:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 13:56:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4609067e6fdc32b9dafccf410fd3193786315de9dfdbe34a5d7f6364086d43bf`  
		Last Modified: Thu, 23 Apr 2020 13:58:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16617e0e9e558519367f0f8154e29d15167329d900f36be6389c0d2e38b5e4b3`  
		Last Modified: Thu, 23 Apr 2020 13:58:58 GMT  
		Size: 219.6 MB (219649819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772895ca7cf6c2b949ac87125f7be7848c72df8906496522d9768802df11e35a`  
		Last Modified: Thu, 23 Apr 2020 13:58:10 GMT  
		Size: 2.3 MB (2334693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861a7c702c46fa314d893142bbce183ea3b0fb281d56239f43ed7fd87e3c19c1`  
		Last Modified: Thu, 23 Apr 2020 13:59:48 GMT  
		Size: 141.6 MB (141615497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b057ce605a43f4f986732e32393925bd15054a32fa1aaef025e92cc9a9ab6af`  
		Last Modified: Thu, 23 Apr 2020 13:59:04 GMT  
		Size: 674.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92865297eddd6c745a69681748285b0a01dc326fd09c7a3b3ecc61ef48828f31`  
		Last Modified: Thu, 23 Apr 2020 13:59:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2478900fe61d0a2eb0afeac83f6d2ca27897121de2bccdfd38fe598cdf661a57`  
		Last Modified: Thu, 23 Apr 2020 13:59:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559d2ad414b55d133db74df63a14eea7d399cfbb30d0f4c14299ddc2d8604af2`  
		Last Modified: Thu, 23 Apr 2020 13:59:03 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11.0`

```console
$ docker pull odoo@sha256:7dd00695526a36c7dcdaca465b1ab17f10a60713db1a3965680a023f6b5b4891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11.0` - linux; amd64

```console
$ docker pull odoo@sha256:9ae74debfc257f96870f4652916e6274bcbd7c72c9ead8b37b0e905e09a8059b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386116136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90453baffa0584c0949dbe3cccf86abf102a285d954b7e4d2ca474fcb9092e36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:51:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Apr 2020 13:51:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Apr 2020 13:51:50 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:51:51 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 23 Apr 2020 13:53:45 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Apr 2020 13:53:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:55:38 GMT
ENV ODOO_VERSION=11.0
# Thu, 23 Apr 2020 13:55:38 GMT
ARG ODOO_RELEASE=20200417
# Thu, 23 Apr 2020 13:55:38 GMT
ARG ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
# Thu, 23 Apr 2020 13:56:52 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb        && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Apr 2020 13:56:54 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Thu, 23 Apr 2020 13:56:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Apr 2020 13:56:56 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Apr 2020 13:56:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Apr 2020 13:56:56 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Apr 2020 13:56:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Apr 2020 13:56:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Apr 2020 13:56:57 GMT
USER odoo
# Thu, 23 Apr 2020 13:56:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 13:56:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4609067e6fdc32b9dafccf410fd3193786315de9dfdbe34a5d7f6364086d43bf`  
		Last Modified: Thu, 23 Apr 2020 13:58:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16617e0e9e558519367f0f8154e29d15167329d900f36be6389c0d2e38b5e4b3`  
		Last Modified: Thu, 23 Apr 2020 13:58:58 GMT  
		Size: 219.6 MB (219649819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772895ca7cf6c2b949ac87125f7be7848c72df8906496522d9768802df11e35a`  
		Last Modified: Thu, 23 Apr 2020 13:58:10 GMT  
		Size: 2.3 MB (2334693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861a7c702c46fa314d893142bbce183ea3b0fb281d56239f43ed7fd87e3c19c1`  
		Last Modified: Thu, 23 Apr 2020 13:59:48 GMT  
		Size: 141.6 MB (141615497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b057ce605a43f4f986732e32393925bd15054a32fa1aaef025e92cc9a9ab6af`  
		Last Modified: Thu, 23 Apr 2020 13:59:04 GMT  
		Size: 674.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92865297eddd6c745a69681748285b0a01dc326fd09c7a3b3ecc61ef48828f31`  
		Last Modified: Thu, 23 Apr 2020 13:59:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2478900fe61d0a2eb0afeac83f6d2ca27897121de2bccdfd38fe598cdf661a57`  
		Last Modified: Thu, 23 Apr 2020 13:59:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559d2ad414b55d133db74df63a14eea7d399cfbb30d0f4c14299ddc2d8604af2`  
		Last Modified: Thu, 23 Apr 2020 13:59:03 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12`

```console
$ docker pull odoo@sha256:15ddbe4a821eecd2ed21e74de295c6e9a99293ddc5676c953410032d2886bc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:e27a51d196e89176e2b92bd67c49a4a565e08d0469326a8f40ad0397d6d0430a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 MB (395839563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e65c5696d72afc34e5f7853c8c0da2447c17da4d534bf18671e64b3e23becf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:51:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Apr 2020 13:51:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Apr 2020 13:51:50 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:51:51 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 23 Apr 2020 13:53:45 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Apr 2020 13:53:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:54:08 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:54:08 GMT
ENV ODOO_VERSION=12.0
# Thu, 23 Apr 2020 13:54:08 GMT
ARG ODOO_RELEASE=20200417
# Thu, 23 Apr 2020 13:54:09 GMT
ARG ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
# Thu, 23 Apr 2020 13:55:17 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Apr 2020 13:55:19 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 23 Apr 2020 13:55:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Apr 2020 13:55:20 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Apr 2020 13:55:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Apr 2020 13:55:21 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Apr 2020 13:55:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Apr 2020 13:55:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Apr 2020 13:55:22 GMT
USER odoo
# Thu, 23 Apr 2020 13:55:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 13:55:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4609067e6fdc32b9dafccf410fd3193786315de9dfdbe34a5d7f6364086d43bf`  
		Last Modified: Thu, 23 Apr 2020 13:58:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16617e0e9e558519367f0f8154e29d15167329d900f36be6389c0d2e38b5e4b3`  
		Last Modified: Thu, 23 Apr 2020 13:58:58 GMT  
		Size: 219.6 MB (219649819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772895ca7cf6c2b949ac87125f7be7848c72df8906496522d9768802df11e35a`  
		Last Modified: Thu, 23 Apr 2020 13:58:10 GMT  
		Size: 2.3 MB (2334693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6eea3eddbfa386c35a18f829ec0374be8fbc686c2966c66dd37ee8a3ed5c16`  
		Last Modified: Thu, 23 Apr 2020 13:58:16 GMT  
		Size: 22.2 MB (22230525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de44b047f86e49d84c39dc108d03931ea96dc0d97315a4fc427b59998e89ad70`  
		Last Modified: Thu, 23 Apr 2020 13:58:45 GMT  
		Size: 129.1 MB (129108399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341e7e5365e2f58f3e1508765ee96fa546f25e894b8efa63822cfa9980e5086`  
		Last Modified: Thu, 23 Apr 2020 13:58:08 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d559dbc4a736859c60313c99ccf47ed3591da79b5e8fd76700de4ed4c109470`  
		Last Modified: Thu, 23 Apr 2020 13:58:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f910d0904b863a18a1edddd2ded5d392ab729866eb950dfb320dbe6c6e1a7b`  
		Last Modified: Thu, 23 Apr 2020 13:58:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a665100b01b1da42cbbe24c515e91877fc57fb13e2aff6e3e61ae5be5da037e1`  
		Last Modified: Thu, 23 Apr 2020 13:58:08 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:15ddbe4a821eecd2ed21e74de295c6e9a99293ddc5676c953410032d2886bc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:e27a51d196e89176e2b92bd67c49a4a565e08d0469326a8f40ad0397d6d0430a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 MB (395839563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e65c5696d72afc34e5f7853c8c0da2447c17da4d534bf18671e64b3e23becf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:51:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Apr 2020 13:51:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Apr 2020 13:51:50 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:51:51 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 23 Apr 2020 13:53:45 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Apr 2020 13:53:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:54:08 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:54:08 GMT
ENV ODOO_VERSION=12.0
# Thu, 23 Apr 2020 13:54:08 GMT
ARG ODOO_RELEASE=20200417
# Thu, 23 Apr 2020 13:54:09 GMT
ARG ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
# Thu, 23 Apr 2020 13:55:17 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Apr 2020 13:55:19 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 23 Apr 2020 13:55:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Apr 2020 13:55:20 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Apr 2020 13:55:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Apr 2020 13:55:21 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Apr 2020 13:55:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Apr 2020 13:55:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Apr 2020 13:55:22 GMT
USER odoo
# Thu, 23 Apr 2020 13:55:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 13:55:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4609067e6fdc32b9dafccf410fd3193786315de9dfdbe34a5d7f6364086d43bf`  
		Last Modified: Thu, 23 Apr 2020 13:58:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16617e0e9e558519367f0f8154e29d15167329d900f36be6389c0d2e38b5e4b3`  
		Last Modified: Thu, 23 Apr 2020 13:58:58 GMT  
		Size: 219.6 MB (219649819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772895ca7cf6c2b949ac87125f7be7848c72df8906496522d9768802df11e35a`  
		Last Modified: Thu, 23 Apr 2020 13:58:10 GMT  
		Size: 2.3 MB (2334693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6eea3eddbfa386c35a18f829ec0374be8fbc686c2966c66dd37ee8a3ed5c16`  
		Last Modified: Thu, 23 Apr 2020 13:58:16 GMT  
		Size: 22.2 MB (22230525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de44b047f86e49d84c39dc108d03931ea96dc0d97315a4fc427b59998e89ad70`  
		Last Modified: Thu, 23 Apr 2020 13:58:45 GMT  
		Size: 129.1 MB (129108399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341e7e5365e2f58f3e1508765ee96fa546f25e894b8efa63822cfa9980e5086`  
		Last Modified: Thu, 23 Apr 2020 13:58:08 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d559dbc4a736859c60313c99ccf47ed3591da79b5e8fd76700de4ed4c109470`  
		Last Modified: Thu, 23 Apr 2020 13:58:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f910d0904b863a18a1edddd2ded5d392ab729866eb950dfb320dbe6c6e1a7b`  
		Last Modified: Thu, 23 Apr 2020 13:58:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a665100b01b1da42cbbe24c515e91877fc57fb13e2aff6e3e61ae5be5da037e1`  
		Last Modified: Thu, 23 Apr 2020 13:58:08 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:68095fc56215b44edb7ef8cb91a8583a71db51bb0ebdde43bf67cbc348fef047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:29d185fbbbcb7628f0f2e3ab8fd4e9bbc7f452fede4f92e7072579465ab9ed8d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.7 MB (377675792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006812cec75a454c761169a47318a17f3d5b74308886c93d5bfa8a310c3b18a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Apr 2020 13:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Apr 2020 13:48:18 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:49:53 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Apr 2020 13:50:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:50:11 GMT
RUN npm install -g rtlcss
# Thu, 23 Apr 2020 13:50:11 GMT
ENV ODOO_VERSION=13.0
# Thu, 23 Apr 2020 13:50:11 GMT
ARG ODOO_RELEASE=20200417
# Thu, 23 Apr 2020 13:50:12 GMT
ARG ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
# Thu, 23 Apr 2020 13:51:37 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Apr 2020 13:51:39 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 23 Apr 2020 13:51:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Apr 2020 13:51:41 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Apr 2020 13:51:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Apr 2020 13:51:41 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Apr 2020 13:51:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Apr 2020 13:51:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Apr 2020 13:51:43 GMT
USER odoo
# Thu, 23 Apr 2020 13:51:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 13:51:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64147cf99a9df5963c8f5e254867b3ab8a671690f06148b663da8ff4af2aad55`  
		Last Modified: Thu, 23 Apr 2020 13:58:02 GMT  
		Size: 203.6 MB (203558470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ab21f01ae692d1c7543d1ac2f1cd6d262460d415e40ef11b4c0b40b29c937a`  
		Last Modified: Thu, 23 Apr 2020 13:57:19 GMT  
		Size: 2.3 MB (2332481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6719380b9a1115b239e0a58488eb77a6ede46d937c764dac60e3107ff895e2`  
		Last Modified: Thu, 23 Apr 2020 13:57:18 GMT  
		Size: 1.1 MB (1089705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6b961fcb32adf8ebfd3e8fafee7bb2b90d215c5e3f663af157a9d75ceacc61`  
		Last Modified: Thu, 23 Apr 2020 13:58:04 GMT  
		Size: 143.6 MB (143594478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7019a73556325cf3a59e132801b94f5953c1dc5c0e29d6b66ed517ad0c55d716`  
		Last Modified: Thu, 23 Apr 2020 13:57:17 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7541867d3bdd1fed27a0f214f406e24e37f4a373e86bacb3d9263dc587f1bb94`  
		Last Modified: Thu, 23 Apr 2020 13:57:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8111647263db765b5964d5e7ac0f844f7a7a1f69483f5a719fd76832bf0fa1`  
		Last Modified: Thu, 23 Apr 2020 13:57:16 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb22a57199ce8cb0be63cd9a138959fb00f8ae1cb1235ec6fe25ac91e95ccb6`  
		Last Modified: Thu, 23 Apr 2020 13:57:17 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:68095fc56215b44edb7ef8cb91a8583a71db51bb0ebdde43bf67cbc348fef047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:29d185fbbbcb7628f0f2e3ab8fd4e9bbc7f452fede4f92e7072579465ab9ed8d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.7 MB (377675792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006812cec75a454c761169a47318a17f3d5b74308886c93d5bfa8a310c3b18a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Apr 2020 13:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Apr 2020 13:48:18 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:49:53 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Apr 2020 13:50:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:50:11 GMT
RUN npm install -g rtlcss
# Thu, 23 Apr 2020 13:50:11 GMT
ENV ODOO_VERSION=13.0
# Thu, 23 Apr 2020 13:50:11 GMT
ARG ODOO_RELEASE=20200417
# Thu, 23 Apr 2020 13:50:12 GMT
ARG ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
# Thu, 23 Apr 2020 13:51:37 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Apr 2020 13:51:39 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 23 Apr 2020 13:51:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Apr 2020 13:51:41 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Apr 2020 13:51:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Apr 2020 13:51:41 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Apr 2020 13:51:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Apr 2020 13:51:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Apr 2020 13:51:43 GMT
USER odoo
# Thu, 23 Apr 2020 13:51:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 13:51:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64147cf99a9df5963c8f5e254867b3ab8a671690f06148b663da8ff4af2aad55`  
		Last Modified: Thu, 23 Apr 2020 13:58:02 GMT  
		Size: 203.6 MB (203558470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ab21f01ae692d1c7543d1ac2f1cd6d262460d415e40ef11b4c0b40b29c937a`  
		Last Modified: Thu, 23 Apr 2020 13:57:19 GMT  
		Size: 2.3 MB (2332481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6719380b9a1115b239e0a58488eb77a6ede46d937c764dac60e3107ff895e2`  
		Last Modified: Thu, 23 Apr 2020 13:57:18 GMT  
		Size: 1.1 MB (1089705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6b961fcb32adf8ebfd3e8fafee7bb2b90d215c5e3f663af157a9d75ceacc61`  
		Last Modified: Thu, 23 Apr 2020 13:58:04 GMT  
		Size: 143.6 MB (143594478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7019a73556325cf3a59e132801b94f5953c1dc5c0e29d6b66ed517ad0c55d716`  
		Last Modified: Thu, 23 Apr 2020 13:57:17 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7541867d3bdd1fed27a0f214f406e24e37f4a373e86bacb3d9263dc587f1bb94`  
		Last Modified: Thu, 23 Apr 2020 13:57:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8111647263db765b5964d5e7ac0f844f7a7a1f69483f5a719fd76832bf0fa1`  
		Last Modified: Thu, 23 Apr 2020 13:57:16 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb22a57199ce8cb0be63cd9a138959fb00f8ae1cb1235ec6fe25ac91e95ccb6`  
		Last Modified: Thu, 23 Apr 2020 13:57:17 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:68095fc56215b44edb7ef8cb91a8583a71db51bb0ebdde43bf67cbc348fef047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:29d185fbbbcb7628f0f2e3ab8fd4e9bbc7f452fede4f92e7072579465ab9ed8d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.7 MB (377675792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006812cec75a454c761169a47318a17f3d5b74308886c93d5bfa8a310c3b18a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Apr 2020 13:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Apr 2020 13:48:18 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:49:53 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Apr 2020 13:50:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:50:11 GMT
RUN npm install -g rtlcss
# Thu, 23 Apr 2020 13:50:11 GMT
ENV ODOO_VERSION=13.0
# Thu, 23 Apr 2020 13:50:11 GMT
ARG ODOO_RELEASE=20200417
# Thu, 23 Apr 2020 13:50:12 GMT
ARG ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
# Thu, 23 Apr 2020 13:51:37 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Apr 2020 13:51:39 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 23 Apr 2020 13:51:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Apr 2020 13:51:41 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Apr 2020 13:51:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Apr 2020 13:51:41 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Apr 2020 13:51:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Apr 2020 13:51:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Apr 2020 13:51:43 GMT
USER odoo
# Thu, 23 Apr 2020 13:51:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 13:51:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64147cf99a9df5963c8f5e254867b3ab8a671690f06148b663da8ff4af2aad55`  
		Last Modified: Thu, 23 Apr 2020 13:58:02 GMT  
		Size: 203.6 MB (203558470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ab21f01ae692d1c7543d1ac2f1cd6d262460d415e40ef11b4c0b40b29c937a`  
		Last Modified: Thu, 23 Apr 2020 13:57:19 GMT  
		Size: 2.3 MB (2332481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6719380b9a1115b239e0a58488eb77a6ede46d937c764dac60e3107ff895e2`  
		Last Modified: Thu, 23 Apr 2020 13:57:18 GMT  
		Size: 1.1 MB (1089705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6b961fcb32adf8ebfd3e8fafee7bb2b90d215c5e3f663af157a9d75ceacc61`  
		Last Modified: Thu, 23 Apr 2020 13:58:04 GMT  
		Size: 143.6 MB (143594478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7019a73556325cf3a59e132801b94f5953c1dc5c0e29d6b66ed517ad0c55d716`  
		Last Modified: Thu, 23 Apr 2020 13:57:17 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7541867d3bdd1fed27a0f214f406e24e37f4a373e86bacb3d9263dc587f1bb94`  
		Last Modified: Thu, 23 Apr 2020 13:57:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8111647263db765b5964d5e7ac0f844f7a7a1f69483f5a719fd76832bf0fa1`  
		Last Modified: Thu, 23 Apr 2020 13:57:16 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb22a57199ce8cb0be63cd9a138959fb00f8ae1cb1235ec6fe25ac91e95ccb6`  
		Last Modified: Thu, 23 Apr 2020 13:57:17 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
