## `odoo:latest`

```console
$ docker pull odoo@sha256:c86f1e31a2184f1205ac947784d54d8fe1bce5bcefa574a62cb555b71a19c46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:ddebf5d6687839331b56d9c64cf2831429c65cd41b373df452d6824f0ebacccb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.0 MB (511001151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c0a83777bd828e3a8f8360a9ab2e8c9693a9283ef5c7b0dc299f01d9c2d3e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Tue, 09 Feb 2021 17:29:18 GMT
ARG ODOO_RELEASE=20210204
# Tue, 09 Feb 2021 17:29:18 GMT
ARG ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
# Tue, 09 Feb 2021 17:30:33 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 09 Feb 2021 17:30:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 09 Feb 2021 17:30:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 09 Feb 2021 17:30:36 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 09 Feb 2021 17:30:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Feb 2021 17:30:37 GMT
EXPOSE 8069 8071 8072
# Tue, 09 Feb 2021 17:30:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Feb 2021 17:30:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 09 Feb 2021 17:30:37 GMT
USER odoo
# Tue, 09 Feb 2021 17:30:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 17:30:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a898f2782afa8cd348b59eb601a7fa0faa1e3d5daa392229041f7d234ad2f0a7`  
		Last Modified: Tue, 09 Feb 2021 17:39:28 GMT  
		Size: 267.5 MB (267496192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a0f63469096ef47e3badda0d84ef75e0a0ef3d8b455632d8354e897710e611`  
		Last Modified: Tue, 09 Feb 2021 17:37:46 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6838bd2119731862abf2af94c7bf146ed0072afa39430ada8ce7be4faa137a6f`  
		Last Modified: Tue, 09 Feb 2021 17:37:47 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4dbeb6ebb72bf5688199c8afb052f2401416936eb822375b7ecd720dd891b3`  
		Last Modified: Tue, 09 Feb 2021 17:37:47 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bad7ef1e443313127014c6a07a7d040e08518d264e0c010191991b67774cc8`  
		Last Modified: Tue, 09 Feb 2021 17:37:46 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
