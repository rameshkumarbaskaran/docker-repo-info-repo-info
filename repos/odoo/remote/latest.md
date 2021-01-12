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
