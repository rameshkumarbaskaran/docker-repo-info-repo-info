<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:1`](#kong1)
-	[`kong:1.5`](#kong15)
-	[`kong:1.5.1`](#kong151)
-	[`kong:1.5.1-alpine`](#kong151-alpine)
-	[`kong:1.5.1-centos`](#kong151-centos)
-	[`kong:1.5.1-ubuntu`](#kong151-ubuntu)
-	[`kong:1.5-centos`](#kong15-centos)
-	[`kong:1.5-ubuntu`](#kong15-ubuntu)
-	[`kong:2`](#kong2)
-	[`kong:2.0`](#kong20)
-	[`kong:2.0.5`](#kong205)
-	[`kong:2.0.5-alpine`](#kong205-alpine)
-	[`kong:2.0.5-centos`](#kong205-centos)
-	[`kong:2.0.5-ubuntu`](#kong205-ubuntu)
-	[`kong:2.0-centos`](#kong20-centos)
-	[`kong:2.0-ubuntu`](#kong20-ubuntu)
-	[`kong:2.1`](#kong21)
-	[`kong:2.1.0-beta.1`](#kong210-beta1)
-	[`kong:2.1.0-beta.1-alpine`](#kong210-beta1-alpine)
-	[`kong:2.1.0-beta.1-centos`](#kong210-beta1-centos)
-	[`kong:2.1.0-beta.1-ubuntu`](#kong210-beta1-ubuntu)
-	[`kong:2.1-alpine`](#kong21-alpine)
-	[`kong:2.1-centos`](#kong21-centos)
-	[`kong:2.1-ubuntu`](#kong21-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:centos`](#kongcentos)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:1`

```console
$ docker pull kong@sha256:d394801bcfdfd7ffb00416baab1d5a0152a698320a72c3ad5eccb8b78b3767eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:1` - linux; amd64

```console
$ docker pull kong@sha256:5d9044488b2587b9e06376a35cb8e48bce8789821794b932735f93ca74256882
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44122107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb43d1ffc3b7166fbb62df75fe40fd74ddf32ecc6a7f02e67040f83a0f6ab4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:00:32 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Fri, 24 Apr 2020 14:01:31 GMT
ENV KONG_VERSION=1.5.1
# Fri, 24 Apr 2020 14:01:31 GMT
ENV KONG_SHA256=ae31a80d82642ef485a59c832cc91beda7403617cb79384d47b5fbdb2b6f7224
# Fri, 24 Apr 2020 14:01:40 GMT
RUN adduser -Su 1337 kong 	&& mkdir -p "/usr/local/kong" 	&& apk add --no-cache --virtual .build-deps curl wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata libcap su-exec zip 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Fri, 24 Apr 2020 14:01:40 GMT
USER kong
# Fri, 24 Apr 2020 14:01:40 GMT
COPY file:a3a704d6fb65fcd83b4f8be540ad321c86550844ad700b6ca4833afbd65c04a2 in /docker-entrypoint.sh 
# Fri, 24 Apr 2020 14:01:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 24 Apr 2020 14:01:41 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 24 Apr 2020 14:01:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Apr 2020 14:01:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f5d653a9ebb1ffa8146c3d0adb444848a636343eb69dd1e60599fe0a2a94d`  
		Last Modified: Fri, 24 Apr 2020 14:05:29 GMT  
		Size: 41.3 MB (41325960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed14408bcf7d87cab0dda9795262fadaf39a4d65221d26f8128bc8b6ff3ae88`  
		Last Modified: Fri, 24 Apr 2020 14:05:21 GMT  
		Size: 567.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:1.5`

```console
$ docker pull kong@sha256:d394801bcfdfd7ffb00416baab1d5a0152a698320a72c3ad5eccb8b78b3767eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:1.5` - linux; amd64

```console
$ docker pull kong@sha256:5d9044488b2587b9e06376a35cb8e48bce8789821794b932735f93ca74256882
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44122107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb43d1ffc3b7166fbb62df75fe40fd74ddf32ecc6a7f02e67040f83a0f6ab4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:00:32 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Fri, 24 Apr 2020 14:01:31 GMT
ENV KONG_VERSION=1.5.1
# Fri, 24 Apr 2020 14:01:31 GMT
ENV KONG_SHA256=ae31a80d82642ef485a59c832cc91beda7403617cb79384d47b5fbdb2b6f7224
# Fri, 24 Apr 2020 14:01:40 GMT
RUN adduser -Su 1337 kong 	&& mkdir -p "/usr/local/kong" 	&& apk add --no-cache --virtual .build-deps curl wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata libcap su-exec zip 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Fri, 24 Apr 2020 14:01:40 GMT
USER kong
# Fri, 24 Apr 2020 14:01:40 GMT
COPY file:a3a704d6fb65fcd83b4f8be540ad321c86550844ad700b6ca4833afbd65c04a2 in /docker-entrypoint.sh 
# Fri, 24 Apr 2020 14:01:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 24 Apr 2020 14:01:41 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 24 Apr 2020 14:01:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Apr 2020 14:01:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f5d653a9ebb1ffa8146c3d0adb444848a636343eb69dd1e60599fe0a2a94d`  
		Last Modified: Fri, 24 Apr 2020 14:05:29 GMT  
		Size: 41.3 MB (41325960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed14408bcf7d87cab0dda9795262fadaf39a4d65221d26f8128bc8b6ff3ae88`  
		Last Modified: Fri, 24 Apr 2020 14:05:21 GMT  
		Size: 567.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:1.5.1`

```console
$ docker pull kong@sha256:d394801bcfdfd7ffb00416baab1d5a0152a698320a72c3ad5eccb8b78b3767eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:1.5.1` - linux; amd64

```console
$ docker pull kong@sha256:5d9044488b2587b9e06376a35cb8e48bce8789821794b932735f93ca74256882
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44122107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb43d1ffc3b7166fbb62df75fe40fd74ddf32ecc6a7f02e67040f83a0f6ab4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:00:32 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Fri, 24 Apr 2020 14:01:31 GMT
ENV KONG_VERSION=1.5.1
# Fri, 24 Apr 2020 14:01:31 GMT
ENV KONG_SHA256=ae31a80d82642ef485a59c832cc91beda7403617cb79384d47b5fbdb2b6f7224
# Fri, 24 Apr 2020 14:01:40 GMT
RUN adduser -Su 1337 kong 	&& mkdir -p "/usr/local/kong" 	&& apk add --no-cache --virtual .build-deps curl wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata libcap su-exec zip 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Fri, 24 Apr 2020 14:01:40 GMT
USER kong
# Fri, 24 Apr 2020 14:01:40 GMT
COPY file:a3a704d6fb65fcd83b4f8be540ad321c86550844ad700b6ca4833afbd65c04a2 in /docker-entrypoint.sh 
# Fri, 24 Apr 2020 14:01:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 24 Apr 2020 14:01:41 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 24 Apr 2020 14:01:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Apr 2020 14:01:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f5d653a9ebb1ffa8146c3d0adb444848a636343eb69dd1e60599fe0a2a94d`  
		Last Modified: Fri, 24 Apr 2020 14:05:29 GMT  
		Size: 41.3 MB (41325960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed14408bcf7d87cab0dda9795262fadaf39a4d65221d26f8128bc8b6ff3ae88`  
		Last Modified: Fri, 24 Apr 2020 14:05:21 GMT  
		Size: 567.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:1.5.1-alpine`

```console
$ docker pull kong@sha256:d394801bcfdfd7ffb00416baab1d5a0152a698320a72c3ad5eccb8b78b3767eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:1.5.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:5d9044488b2587b9e06376a35cb8e48bce8789821794b932735f93ca74256882
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44122107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb43d1ffc3b7166fbb62df75fe40fd74ddf32ecc6a7f02e67040f83a0f6ab4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:00:32 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Fri, 24 Apr 2020 14:01:31 GMT
ENV KONG_VERSION=1.5.1
# Fri, 24 Apr 2020 14:01:31 GMT
ENV KONG_SHA256=ae31a80d82642ef485a59c832cc91beda7403617cb79384d47b5fbdb2b6f7224
# Fri, 24 Apr 2020 14:01:40 GMT
RUN adduser -Su 1337 kong 	&& mkdir -p "/usr/local/kong" 	&& apk add --no-cache --virtual .build-deps curl wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata libcap su-exec zip 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Fri, 24 Apr 2020 14:01:40 GMT
USER kong
# Fri, 24 Apr 2020 14:01:40 GMT
COPY file:a3a704d6fb65fcd83b4f8be540ad321c86550844ad700b6ca4833afbd65c04a2 in /docker-entrypoint.sh 
# Fri, 24 Apr 2020 14:01:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 24 Apr 2020 14:01:41 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 24 Apr 2020 14:01:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Apr 2020 14:01:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f5d653a9ebb1ffa8146c3d0adb444848a636343eb69dd1e60599fe0a2a94d`  
		Last Modified: Fri, 24 Apr 2020 14:05:29 GMT  
		Size: 41.3 MB (41325960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed14408bcf7d87cab0dda9795262fadaf39a4d65221d26f8128bc8b6ff3ae88`  
		Last Modified: Fri, 24 Apr 2020 14:05:21 GMT  
		Size: 567.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:1.5.1-centos`

```console
$ docker pull kong@sha256:1e5daef6de28a3cf07fdfe0a388dd8afb7323b3024d265a6ecaca50ebafa44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:1.5.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:25e4f468d3406fc0b11878c6237393ad8efb322632a23bfc7acec0bed685f472
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151295984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713522c8c9ce6a6f6412f8a5edb89417a714fe844f5a3aeb919e4f466e59a38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 21:54:58 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Tue, 05 May 2020 21:54:58 GMT
ENV KONG_VERSION=1.5.1
# Tue, 05 May 2020 21:54:58 GMT
ARG SU_EXEC_VERSION=0.2
# Tue, 05 May 2020 21:54:58 GMT
ARG SU_EXEC_URL=https://github.com/ncopa/su-exec/archive/v0.2.tar.gz
# Tue, 05 May 2020 21:55:35 GMT
# ARGS: SU_EXEC_URL=https://github.com/ncopa/su-exec/archive/v0.2.tar.gz SU_EXEC_VERSION=0.2
RUN yum install -y -q gcc make unzip 	&& curl -sL "${SU_EXEC_URL}" | tar -C /tmp -zxf - 	&& make -C "/tmp/su-exec-${SU_EXEC_VERSION}" 	&& cp "/tmp/su-exec-${SU_EXEC_VERSION}/su-exec" /usr/bin 	&& rm -fr "/tmp/su-exec-${SU_EXEC_VERSION}" 	&& yum autoremove -y -q gcc make 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki
# Tue, 05 May 2020 21:55:52 GMT
# ARGS: SU_EXEC_URL=https://github.com/ncopa/su-exec/archive/v0.2.tar.gz SU_EXEC_VERSION=0.2
RUN useradd --uid 1337 kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm 	&& yum clean all 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Tue, 05 May 2020 21:55:52 GMT
USER kong
# Tue, 05 May 2020 21:55:52 GMT
COPY file:53261f3826b37731452f0b663f02629669c2338dfa058cd1a4d6be45db56e5a6 in /docker-entrypoint.sh 
# Tue, 05 May 2020 21:55:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 May 2020 21:55:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 May 2020 21:55:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 May 2020 21:55:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe1df8626656e70284e03cc075b524446a3eed089992705f3ae8ba0aa5411b7`  
		Last Modified: Tue, 05 May 2020 22:03:02 GMT  
		Size: 6.6 MB (6605212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54720925d19a1b0ac8043b74835533b91584b9affb8daf2c87856438fe9b158f`  
		Last Modified: Tue, 05 May 2020 22:03:17 GMT  
		Size: 68.8 MB (68810065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652852c5b39726a80091ad85a93689d862800f1ecfdbc0cd727cdd21fb6ec114`  
		Last Modified: Tue, 05 May 2020 22:03:01 GMT  
		Size: 566.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:1.5.1-ubuntu`

```console
$ docker pull kong@sha256:6ee0d2e4377549cc691acd3dc48eeab08f815f9309489cea9b249d6db575f1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:1.5.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9d8a119d7b9538fb4e6d89b91544522c2ce5fbd1fce63e8ffabafeba84f5c75d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81349992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafa2f671183df8b13e5282fbce2fd90be933ea447d7db94fd4ad309f81fcb05`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:18:09 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Tue, 07 Jul 2020 00:18:10 GMT
ENV KONG_VERSION=1.5.1
# Tue, 07 Jul 2020 00:18:27 GMT
RUN useradd kong     && mkdir -p "/usr/local/kong"     && apt-get update     && apt-get install -y --no-install-recommends ca-certificates curl perl unzip     && rm -rf /var/lib/apt/lists/*     && curl -fsSLo kong.deb https://bintray.com/kong/kong-deb/download_file?file_path=kong-${KONG_VERSION}.xenial.$(dpkg --print-architecture).deb     && apt-get purge -y --auto-remove ca-certificates curl     && dpkg -i kong.deb     && rm -rf kong.deb     && chown -R kong:0 /usr/local/kong     && chmod -R g=u /usr/local/kong
# Tue, 07 Jul 2020 00:18:28 GMT
COPY file:a4763218d814cc99d340cb11497461af1e7b06c7ec7d19308fb1d59952ad34a4 in /docker-entrypoint.sh 
# Tue, 07 Jul 2020 00:18:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:18:28 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jul 2020 00:18:28 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jul 2020 00:18:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ee7f3cbcbb038aee91a772b64ab2ca370267491086dd7d2155dc802651ff50`  
		Last Modified: Tue, 07 Jul 2020 00:19:35 GMT  
		Size: 37.0 MB (36973986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5975cc101460bfd63c2552c2e33057ac16726e249baa232c35be2f54e7a5614b`  
		Last Modified: Tue, 07 Jul 2020 00:19:26 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:1.5.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:064a4561e3228a28aea0a8be31e4a3f62cf515e5bd8e4153b1d6742c863f45c3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76008930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ce44d30fec1e949cc4587e2bae35fdf859284dc70145e036f4f34cbf9da139`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:14:08 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Mon, 06 Jul 2020 23:14:08 GMT
ENV KONG_VERSION=1.5.1
# Mon, 06 Jul 2020 23:14:45 GMT
RUN useradd kong     && mkdir -p "/usr/local/kong"     && apt-get update     && apt-get install -y --no-install-recommends ca-certificates curl perl unzip     && rm -rf /var/lib/apt/lists/*     && curl -fsSLo kong.deb https://bintray.com/kong/kong-deb/download_file?file_path=kong-${KONG_VERSION}.xenial.$(dpkg --print-architecture).deb     && apt-get purge -y --auto-remove ca-certificates curl     && dpkg -i kong.deb     && rm -rf kong.deb     && chown -R kong:0 /usr/local/kong     && chmod -R g=u /usr/local/kong
# Mon, 06 Jul 2020 23:14:48 GMT
COPY file:a4763218d814cc99d340cb11497461af1e7b06c7ec7d19308fb1d59952ad34a4 in /docker-entrypoint.sh 
# Mon, 06 Jul 2020 23:14:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 Jul 2020 23:14:49 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 06 Jul 2020 23:14:50 GMT
STOPSIGNAL SIGQUIT
# Mon, 06 Jul 2020 23:14:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15dbb6cfa7292c6a2d1530741593e54259d6e5ceef7157ec50e2314633b17c8`  
		Last Modified: Mon, 06 Jul 2020 23:16:05 GMT  
		Size: 36.0 MB (35971659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60b50fef88adc05a118f8c834eb83a16ba16dc5b15324964e05319df6cbc797`  
		Last Modified: Mon, 06 Jul 2020 23:15:53 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:1.5-centos`

```console
$ docker pull kong@sha256:1e5daef6de28a3cf07fdfe0a388dd8afb7323b3024d265a6ecaca50ebafa44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:1.5-centos` - linux; amd64

```console
$ docker pull kong@sha256:25e4f468d3406fc0b11878c6237393ad8efb322632a23bfc7acec0bed685f472
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151295984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713522c8c9ce6a6f6412f8a5edb89417a714fe844f5a3aeb919e4f466e59a38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 21:54:58 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Tue, 05 May 2020 21:54:58 GMT
ENV KONG_VERSION=1.5.1
# Tue, 05 May 2020 21:54:58 GMT
ARG SU_EXEC_VERSION=0.2
# Tue, 05 May 2020 21:54:58 GMT
ARG SU_EXEC_URL=https://github.com/ncopa/su-exec/archive/v0.2.tar.gz
# Tue, 05 May 2020 21:55:35 GMT
# ARGS: SU_EXEC_URL=https://github.com/ncopa/su-exec/archive/v0.2.tar.gz SU_EXEC_VERSION=0.2
RUN yum install -y -q gcc make unzip 	&& curl -sL "${SU_EXEC_URL}" | tar -C /tmp -zxf - 	&& make -C "/tmp/su-exec-${SU_EXEC_VERSION}" 	&& cp "/tmp/su-exec-${SU_EXEC_VERSION}/su-exec" /usr/bin 	&& rm -fr "/tmp/su-exec-${SU_EXEC_VERSION}" 	&& yum autoremove -y -q gcc make 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki
# Tue, 05 May 2020 21:55:52 GMT
# ARGS: SU_EXEC_URL=https://github.com/ncopa/su-exec/archive/v0.2.tar.gz SU_EXEC_VERSION=0.2
RUN useradd --uid 1337 kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm 	&& yum clean all 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Tue, 05 May 2020 21:55:52 GMT
USER kong
# Tue, 05 May 2020 21:55:52 GMT
COPY file:53261f3826b37731452f0b663f02629669c2338dfa058cd1a4d6be45db56e5a6 in /docker-entrypoint.sh 
# Tue, 05 May 2020 21:55:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 May 2020 21:55:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 May 2020 21:55:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 May 2020 21:55:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe1df8626656e70284e03cc075b524446a3eed089992705f3ae8ba0aa5411b7`  
		Last Modified: Tue, 05 May 2020 22:03:02 GMT  
		Size: 6.6 MB (6605212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54720925d19a1b0ac8043b74835533b91584b9affb8daf2c87856438fe9b158f`  
		Last Modified: Tue, 05 May 2020 22:03:17 GMT  
		Size: 68.8 MB (68810065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652852c5b39726a80091ad85a93689d862800f1ecfdbc0cd727cdd21fb6ec114`  
		Last Modified: Tue, 05 May 2020 22:03:01 GMT  
		Size: 566.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:1.5-ubuntu`

```console
$ docker pull kong@sha256:6ee0d2e4377549cc691acd3dc48eeab08f815f9309489cea9b249d6db575f1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:1.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9d8a119d7b9538fb4e6d89b91544522c2ce5fbd1fce63e8ffabafeba84f5c75d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81349992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafa2f671183df8b13e5282fbce2fd90be933ea447d7db94fd4ad309f81fcb05`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:18:09 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Tue, 07 Jul 2020 00:18:10 GMT
ENV KONG_VERSION=1.5.1
# Tue, 07 Jul 2020 00:18:27 GMT
RUN useradd kong     && mkdir -p "/usr/local/kong"     && apt-get update     && apt-get install -y --no-install-recommends ca-certificates curl perl unzip     && rm -rf /var/lib/apt/lists/*     && curl -fsSLo kong.deb https://bintray.com/kong/kong-deb/download_file?file_path=kong-${KONG_VERSION}.xenial.$(dpkg --print-architecture).deb     && apt-get purge -y --auto-remove ca-certificates curl     && dpkg -i kong.deb     && rm -rf kong.deb     && chown -R kong:0 /usr/local/kong     && chmod -R g=u /usr/local/kong
# Tue, 07 Jul 2020 00:18:28 GMT
COPY file:a4763218d814cc99d340cb11497461af1e7b06c7ec7d19308fb1d59952ad34a4 in /docker-entrypoint.sh 
# Tue, 07 Jul 2020 00:18:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:18:28 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jul 2020 00:18:28 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jul 2020 00:18:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ee7f3cbcbb038aee91a772b64ab2ca370267491086dd7d2155dc802651ff50`  
		Last Modified: Tue, 07 Jul 2020 00:19:35 GMT  
		Size: 37.0 MB (36973986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5975cc101460bfd63c2552c2e33057ac16726e249baa232c35be2f54e7a5614b`  
		Last Modified: Tue, 07 Jul 2020 00:19:26 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:1.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:064a4561e3228a28aea0a8be31e4a3f62cf515e5bd8e4153b1d6742c863f45c3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76008930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ce44d30fec1e949cc4587e2bae35fdf859284dc70145e036f4f34cbf9da139`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:14:08 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Mon, 06 Jul 2020 23:14:08 GMT
ENV KONG_VERSION=1.5.1
# Mon, 06 Jul 2020 23:14:45 GMT
RUN useradd kong     && mkdir -p "/usr/local/kong"     && apt-get update     && apt-get install -y --no-install-recommends ca-certificates curl perl unzip     && rm -rf /var/lib/apt/lists/*     && curl -fsSLo kong.deb https://bintray.com/kong/kong-deb/download_file?file_path=kong-${KONG_VERSION}.xenial.$(dpkg --print-architecture).deb     && apt-get purge -y --auto-remove ca-certificates curl     && dpkg -i kong.deb     && rm -rf kong.deb     && chown -R kong:0 /usr/local/kong     && chmod -R g=u /usr/local/kong
# Mon, 06 Jul 2020 23:14:48 GMT
COPY file:a4763218d814cc99d340cb11497461af1e7b06c7ec7d19308fb1d59952ad34a4 in /docker-entrypoint.sh 
# Mon, 06 Jul 2020 23:14:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 Jul 2020 23:14:49 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 06 Jul 2020 23:14:50 GMT
STOPSIGNAL SIGQUIT
# Mon, 06 Jul 2020 23:14:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15dbb6cfa7292c6a2d1530741593e54259d6e5ceef7157ec50e2314633b17c8`  
		Last Modified: Mon, 06 Jul 2020 23:16:05 GMT  
		Size: 36.0 MB (35971659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60b50fef88adc05a118f8c834eb83a16ba16dc5b15324964e05319df6cbc797`  
		Last Modified: Mon, 06 Jul 2020 23:15:53 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2`

```console
$ docker pull kong@sha256:32a09516a4fad6a7d42a90f7f754970555027a73e349b980a72c7120e00488b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:dc302feb438b82d99d70e7e140df748654b53341bde9725c7d663baa8fb9b5e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89025900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a800e1cef72354e6e0f6549c23e47d8622aed285f35e7ec340cd19dce577d01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Tue, 05 May 2020 00:19:57 GMT
ARG KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:19:57 GMT
ENV KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:19:57 GMT
ARG KONG_SHA256=457dd0172ae2de2e0b71ce625f78e06449faf38fd734dd6825eb7782d74cb77e
# Tue, 05 May 2020 00:19:57 GMT
ENV KONG_SHA256=457dd0172ae2de2e0b71ce625f78e06449faf38fd734dd6825eb7782d74cb77e
# Tue, 05 May 2020 00:20:09 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong
# Tue, 05 May 2020 00:20:10 GMT
COPY file:c7c95ad9b95e03a404039e7ee878ca4bb52cbcb965cd2d12c91037eb7a3b7e65 in /docker-entrypoint.sh 
# Tue, 05 May 2020 00:20:10 GMT
USER kong
# Tue, 05 May 2020 00:20:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 May 2020 00:20:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 May 2020 00:20:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 May 2020 00:20:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362c162bd1100f98c75c4f57997da5b9e28cd6ed876bf245131f63971c73f7aa`  
		Last Modified: Tue, 05 May 2020 00:22:58 GMT  
		Size: 86.2 MB (86211770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4da51840b66cea01c99f6efb58af2ac5bee97ac78b11d937f7bc2dca9ac4de`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0`

```console
$ docker pull kong@sha256:32a09516a4fad6a7d42a90f7f754970555027a73e349b980a72c7120e00488b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0` - linux; amd64

```console
$ docker pull kong@sha256:dc302feb438b82d99d70e7e140df748654b53341bde9725c7d663baa8fb9b5e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89025900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a800e1cef72354e6e0f6549c23e47d8622aed285f35e7ec340cd19dce577d01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Tue, 05 May 2020 00:19:57 GMT
ARG KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:19:57 GMT
ENV KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:19:57 GMT
ARG KONG_SHA256=457dd0172ae2de2e0b71ce625f78e06449faf38fd734dd6825eb7782d74cb77e
# Tue, 05 May 2020 00:19:57 GMT
ENV KONG_SHA256=457dd0172ae2de2e0b71ce625f78e06449faf38fd734dd6825eb7782d74cb77e
# Tue, 05 May 2020 00:20:09 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong
# Tue, 05 May 2020 00:20:10 GMT
COPY file:c7c95ad9b95e03a404039e7ee878ca4bb52cbcb965cd2d12c91037eb7a3b7e65 in /docker-entrypoint.sh 
# Tue, 05 May 2020 00:20:10 GMT
USER kong
# Tue, 05 May 2020 00:20:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 May 2020 00:20:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 May 2020 00:20:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 May 2020 00:20:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362c162bd1100f98c75c4f57997da5b9e28cd6ed876bf245131f63971c73f7aa`  
		Last Modified: Tue, 05 May 2020 00:22:58 GMT  
		Size: 86.2 MB (86211770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4da51840b66cea01c99f6efb58af2ac5bee97ac78b11d937f7bc2dca9ac4de`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5`

**does not exist** (yet?)

## `kong:2.0.5-alpine`

**does not exist** (yet?)

## `kong:2.0.5-centos`

**does not exist** (yet?)

## `kong:2.0.5-ubuntu`

**does not exist** (yet?)

## `kong:2.0-centos`

```console
$ docker pull kong@sha256:26b695f46f0401152bb06730abff6966a06a35c75d151ede1859b450a213df40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0-centos` - linux; amd64

```console
$ docker pull kong@sha256:0770a2caadebe3516c2b2e3a89f03f0b5ebe5ded765d4b9d89cc9e9107496ab2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125876109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33606e3edaee945be23e4e4e9a8afbc416da3421b00be80f861dec3045b53b2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 21:54:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 21:54:26 GMT
ARG ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
ENV ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Tue, 05 May 2020 21:54:27 GMT
ARG KONG_VERSION=2.0.4
# Tue, 05 May 2020 21:54:27 GMT
ENV KONG_VERSION=2.0.4
# Tue, 05 May 2020 21:54:27 GMT
ARG KONG_SHA256=16a934a7bc2e182f00f03bd75b67f4bdb483150b3820d33cab9b0c95539dd353
# Tue, 05 May 2020 21:54:27 GMT
ENV KONG_SHA256=16a934a7bc2e182f00f03bd75b67f4bdb483150b3820d33cab9b0c95539dd353
# Tue, 05 May 2020 21:54:46 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm &&         echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;     fi;     yum install -y -q unzip shadow-utils 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong
# Tue, 05 May 2020 21:54:47 GMT
COPY file:c7c95ad9b95e03a404039e7ee878ca4bb52cbcb965cd2d12c91037eb7a3b7e65 in /docker-entrypoint.sh 
# Tue, 05 May 2020 21:54:47 GMT
USER kong
# Tue, 05 May 2020 21:54:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 May 2020 21:54:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 May 2020 21:54:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 May 2020 21:54:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce7701dd3817fcacdc04d8abfd7cd6ea61fe7f4d909903260a2ebe43fce007f`  
		Last Modified: Tue, 05 May 2020 22:02:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c09eae848c2b3842c2e1b6863034e9fb2ca603d8438ae1ffa8d1f1dbd3d1593`  
		Last Modified: Tue, 05 May 2020 22:02:55 GMT  
		Size: 50.0 MB (49995157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a8e1c9ddcadf4475ac984587a95973290b72baed79445bbec7bddea3e7d3ad`  
		Last Modified: Tue, 05 May 2020 22:02:16 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0-ubuntu`

```console
$ docker pull kong@sha256:e289d1d59f30d50b9705fb25f5d3e09c5e9f789c7d56cdaf5000adfc36d66287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:280df6e40ecdad6e7bc43ee4257ffe43902f3f0b30a4a5a0f60bc15bc64e19b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94313042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52318c270a779c2d2e695333c6f79efa3cb3fef73aa8f092891a6cccf9f830d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:16:32 GMT
ARG ASSET=ce
# Tue, 07 Jul 2020 00:16:32 GMT
ENV ASSET=ce
# Tue, 07 Jul 2020 00:16:32 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Tue, 07 Jul 2020 00:17:33 GMT
ARG KONG_VERSION=2.0.4
# Tue, 07 Jul 2020 00:17:33 GMT
ENV KONG_VERSION=2.0.4
# Tue, 07 Jul 2020 00:17:53 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb &&         apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong
# Tue, 07 Jul 2020 00:17:54 GMT
COPY file:7cd3b30326ffeaddc1253699208f97fb54711d4ae930aeeeff1e19ebf51cb561 in /docker-entrypoint.sh 
# Tue, 07 Jul 2020 00:17:54 GMT
USER kong
# Tue, 07 Jul 2020 00:17:55 GMT
RUN kong version
# Tue, 07 Jul 2020 00:17:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:17:55 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jul 2020 00:17:55 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jul 2020 00:17:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143c32b458621fe6c4f8e03075d63acff14f384d32857620905001d581d3c71c`  
		Last Modified: Tue, 07 Jul 2020 00:18:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b973c91d253a303114da9230977c9f151dc3c925daec767151fcf3dfa12961`  
		Last Modified: Tue, 07 Jul 2020 00:19:20 GMT  
		Size: 49.9 MB (49936491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19141e6b35ee673101c4a8456210c18a82a96548c1d8ecea615eaabc46185d0a`  
		Last Modified: Tue, 07 Jul 2020 00:19:09 GMT  
		Size: 632.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2daef6cc11258da19c632b8132c7113fa861eb62bdfbba576e72b3686513ef6`  
		Last Modified: Tue, 07 Jul 2020 00:19:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f45baefb4365cf59fbfb8784a87835c07c003e6cd4d43061a622f595a87f9896
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87956868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaad0ea2000f7e8419a14d4050bd515e37846a9be657ce80e8743675ef6ed4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:11:52 GMT
ARG ASSET=ce
# Mon, 06 Jul 2020 23:11:52 GMT
ENV ASSET=ce
# Mon, 06 Jul 2020 23:11:53 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Mon, 06 Jul 2020 23:13:11 GMT
ARG KONG_VERSION=2.0.4
# Mon, 06 Jul 2020 23:13:11 GMT
ENV KONG_VERSION=2.0.4
# Mon, 06 Jul 2020 23:13:49 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb &&         apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong
# Mon, 06 Jul 2020 23:13:52 GMT
COPY file:7cd3b30326ffeaddc1253699208f97fb54711d4ae930aeeeff1e19ebf51cb561 in /docker-entrypoint.sh 
# Mon, 06 Jul 2020 23:13:52 GMT
USER kong
# Mon, 06 Jul 2020 23:13:54 GMT
RUN kong version
# Mon, 06 Jul 2020 23:13:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 Jul 2020 23:13:55 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 06 Jul 2020 23:13:56 GMT
STOPSIGNAL SIGQUIT
# Mon, 06 Jul 2020 23:13:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e9d9ca3d496619cb7d9dd321c5e1b12f499e234a4bfff523ed3169665df8b`  
		Last Modified: Mon, 06 Jul 2020 23:15:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167cc4fdbdcd6b1e42eefef9a0e843677603d721543bdd71fbb5fccfe0c784b`  
		Last Modified: Mon, 06 Jul 2020 23:15:45 GMT  
		Size: 47.9 MB (47919051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145f31f4d6fa8e388dcda72f41d13b4140883938ea81778a74cdc775a44e8c4e`  
		Last Modified: Mon, 06 Jul 2020 23:15:30 GMT  
		Size: 632.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627990a3dfb0b5ae178e48a22a9b7c41e7c01d057779a3d83dfc2f96e91d4b5c`  
		Last Modified: Mon, 06 Jul 2020 23:15:29 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1`

```console
$ docker pull kong@sha256:9da7678dcfa53e72c111e0808e25c8d2add5de1d9fed435b99ebd508b46ec8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1` - linux; amd64

```console
$ docker pull kong@sha256:8ab38a1619b83fcde75726a683c365fb6eccaef9058e8bd9f37bb113c050adc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59535920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28952b67ba3794666dc118fb13b5d1fd043f1175a15b65e889dc4fe8e1206fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Mon, 22 Jun 2020 19:27:05 GMT
ARG KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:27:06 GMT
ENV KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:27:06 GMT
ARG KONG_SHA256=2f6d703b54c9da3787bdab1e38ec8c1ec70e4cb30751c7df021d97957704736d
# Mon, 22 Jun 2020 19:27:06 GMT
ENV KONG_SHA256=2f6d703b54c9da3787bdab1e38ec8c1ec70e4cb30751c7df021d97957704736d
# Mon, 22 Jun 2020 19:27:16 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Mon, 22 Jun 2020 19:27:16 GMT
COPY file:fa8375740fa706893b805c585210990194c529e023568323f95bd7d67be95132 in /docker-entrypoint.sh 
# Mon, 22 Jun 2020 19:27:17 GMT
USER kong
# Mon, 22 Jun 2020 19:27:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2020 19:27:17 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 22 Jun 2020 19:27:17 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2020 19:27:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e69e7b1c0aea7473e2ebdf44bfc933b632f3449d14ce0b2ed4395999a4d92`  
		Last Modified: Mon, 22 Jun 2020 19:29:32 GMT  
		Size: 56.7 MB (56721776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c1f62c47aea958010c7e08361b601d389ccb3a7ce0e42f1ab917b6426eedb4`  
		Last Modified: Mon, 22 Jun 2020 19:29:21 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.0-beta.1`

```console
$ docker pull kong@sha256:9da7678dcfa53e72c111e0808e25c8d2add5de1d9fed435b99ebd508b46ec8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1.0-beta.1` - linux; amd64

```console
$ docker pull kong@sha256:8ab38a1619b83fcde75726a683c365fb6eccaef9058e8bd9f37bb113c050adc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59535920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28952b67ba3794666dc118fb13b5d1fd043f1175a15b65e889dc4fe8e1206fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Mon, 22 Jun 2020 19:27:05 GMT
ARG KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:27:06 GMT
ENV KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:27:06 GMT
ARG KONG_SHA256=2f6d703b54c9da3787bdab1e38ec8c1ec70e4cb30751c7df021d97957704736d
# Mon, 22 Jun 2020 19:27:06 GMT
ENV KONG_SHA256=2f6d703b54c9da3787bdab1e38ec8c1ec70e4cb30751c7df021d97957704736d
# Mon, 22 Jun 2020 19:27:16 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Mon, 22 Jun 2020 19:27:16 GMT
COPY file:fa8375740fa706893b805c585210990194c529e023568323f95bd7d67be95132 in /docker-entrypoint.sh 
# Mon, 22 Jun 2020 19:27:17 GMT
USER kong
# Mon, 22 Jun 2020 19:27:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2020 19:27:17 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 22 Jun 2020 19:27:17 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2020 19:27:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e69e7b1c0aea7473e2ebdf44bfc933b632f3449d14ce0b2ed4395999a4d92`  
		Last Modified: Mon, 22 Jun 2020 19:29:32 GMT  
		Size: 56.7 MB (56721776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c1f62c47aea958010c7e08361b601d389ccb3a7ce0e42f1ab917b6426eedb4`  
		Last Modified: Mon, 22 Jun 2020 19:29:21 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.0-beta.1-alpine`

```console
$ docker pull kong@sha256:9da7678dcfa53e72c111e0808e25c8d2add5de1d9fed435b99ebd508b46ec8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1.0-beta.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:8ab38a1619b83fcde75726a683c365fb6eccaef9058e8bd9f37bb113c050adc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59535920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28952b67ba3794666dc118fb13b5d1fd043f1175a15b65e889dc4fe8e1206fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Mon, 22 Jun 2020 19:27:05 GMT
ARG KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:27:06 GMT
ENV KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:27:06 GMT
ARG KONG_SHA256=2f6d703b54c9da3787bdab1e38ec8c1ec70e4cb30751c7df021d97957704736d
# Mon, 22 Jun 2020 19:27:06 GMT
ENV KONG_SHA256=2f6d703b54c9da3787bdab1e38ec8c1ec70e4cb30751c7df021d97957704736d
# Mon, 22 Jun 2020 19:27:16 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Mon, 22 Jun 2020 19:27:16 GMT
COPY file:fa8375740fa706893b805c585210990194c529e023568323f95bd7d67be95132 in /docker-entrypoint.sh 
# Mon, 22 Jun 2020 19:27:17 GMT
USER kong
# Mon, 22 Jun 2020 19:27:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2020 19:27:17 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 22 Jun 2020 19:27:17 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2020 19:27:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e69e7b1c0aea7473e2ebdf44bfc933b632f3449d14ce0b2ed4395999a4d92`  
		Last Modified: Mon, 22 Jun 2020 19:29:32 GMT  
		Size: 56.7 MB (56721776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c1f62c47aea958010c7e08361b601d389ccb3a7ce0e42f1ab917b6426eedb4`  
		Last Modified: Mon, 22 Jun 2020 19:29:21 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.0-beta.1-centos`

```console
$ docker pull kong@sha256:513e10ab873591c7748e52e67f916cc530bbd451cf54e3a583c4754088b83de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1.0-beta.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:48a8b309f4c9d55102e5927ae9c9720e2443b45dc1190a78472ba8f277628433
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133982638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebbd2b3a9c9454aac62b967315898a55a30b20fe3c6ed2693ed7bbb11c61b74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 21:54:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 21:54:26 GMT
ARG ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
ENV ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Mon, 22 Jun 2020 19:28:16 GMT
ARG KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:28:16 GMT
ENV KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:28:17 GMT
ARG KONG_SHA256=cc6440089fce6f450c8fea5749753bf67fb92d4e3712de9aa50c1fd75997a770
# Mon, 22 Jun 2020 19:28:17 GMT
ENV KONG_SHA256=cc6440089fce6f450c8fea5749753bf67fb92d4e3712de9aa50c1fd75997a770
# Mon, 22 Jun 2020 19:28:41 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib zlib-devel 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Mon, 22 Jun 2020 19:28:42 GMT
COPY file:fa8375740fa706893b805c585210990194c529e023568323f95bd7d67be95132 in /docker-entrypoint.sh 
# Mon, 22 Jun 2020 19:28:42 GMT
USER kong
# Mon, 22 Jun 2020 19:28:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2020 19:28:42 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 22 Jun 2020 19:28:42 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2020 19:28:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce7701dd3817fcacdc04d8abfd7cd6ea61fe7f4d909903260a2ebe43fce007f`  
		Last Modified: Tue, 05 May 2020 22:02:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ae30896a07cad0a8dc8c498289c1a383fc9a1a7c85a2768bf3365f641709c6`  
		Last Modified: Mon, 22 Jun 2020 19:30:05 GMT  
		Size: 58.1 MB (58101671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8807af506f42b0df56df0d9011059d12539e6444b3ddbed6f2cf7b9558bbdf5`  
		Last Modified: Mon, 22 Jun 2020 19:29:54 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.0-beta.1-ubuntu`

```console
$ docker pull kong@sha256:1debe57e06a25e631d306307570c837e8a71a61dd5e444039b43a17e1e5b7b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.0-beta.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:706e03a0000f1092a515e10878a0b7378425e15ab19e535a16ec6c11211feb12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115984148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e4ae8713c898d85acdcd62f3cd6cfc06e5902d22e4ff3726cd7ea726c8cf0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:16:32 GMT
ARG ASSET=ce
# Tue, 07 Jul 2020 00:16:32 GMT
ENV ASSET=ce
# Tue, 07 Jul 2020 00:16:32 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Tue, 07 Jul 2020 00:16:32 GMT
ARG KONG_VERSION=2.1.0beta.1
# Tue, 07 Jul 2020 00:16:32 GMT
ENV KONG_VERSION=2.1.0beta.1
# Tue, 07 Jul 2020 00:17:16 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git     && { apt-get install -y --no-install-recommends zlibc || true; }     && { apt-get install -y --no-install-recommends zlib1g-dev || true; }     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Tue, 07 Jul 2020 00:17:16 GMT
COPY file:8cfc195cab364205f6c571f352a222ce4e5f1211c3309cce2e55fc785367559d in /docker-entrypoint.sh 
# Tue, 07 Jul 2020 00:17:16 GMT
USER kong
# Tue, 07 Jul 2020 00:17:17 GMT
RUN kong version
# Tue, 07 Jul 2020 00:17:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:17:18 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jul 2020 00:17:18 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jul 2020 00:17:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143c32b458621fe6c4f8e03075d63acff14f384d32857620905001d581d3c71c`  
		Last Modified: Tue, 07 Jul 2020 00:18:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2195fd3e9e4be6b1cd7d7ae16bf74957f22127aa2126a7ee95f636f36a701d`  
		Last Modified: Tue, 07 Jul 2020 00:19:02 GMT  
		Size: 71.6 MB (71607582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28a8234efe902d91d4eb48ded173b8068a2e57d88fe89959827793ddf3cd4bb`  
		Last Modified: Tue, 07 Jul 2020 00:18:48 GMT  
		Size: 647.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d74e5bd7de115fd006481a1411bf97131c1bc4111208a54f2f7816b85b6d4`  
		Last Modified: Tue, 07 Jul 2020 00:18:48 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.0-beta.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d55cd823d7e8acad8b7474604cdc06be0839ccca3c4bd1248879deff3881e357
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107050701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b213d86338a74c4d64fd760078eeba41ce67bb851f7f72a27250cf56fe7832bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:11:52 GMT
ARG ASSET=ce
# Mon, 06 Jul 2020 23:11:52 GMT
ENV ASSET=ce
# Mon, 06 Jul 2020 23:11:53 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Mon, 06 Jul 2020 23:11:54 GMT
ARG KONG_VERSION=2.1.0beta.1
# Mon, 06 Jul 2020 23:11:54 GMT
ENV KONG_VERSION=2.1.0beta.1
# Mon, 06 Jul 2020 23:12:47 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git     && { apt-get install -y --no-install-recommends zlibc || true; }     && { apt-get install -y --no-install-recommends zlib1g-dev || true; }     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Mon, 06 Jul 2020 23:12:50 GMT
COPY file:8cfc195cab364205f6c571f352a222ce4e5f1211c3309cce2e55fc785367559d in /docker-entrypoint.sh 
# Mon, 06 Jul 2020 23:12:51 GMT
USER kong
# Mon, 06 Jul 2020 23:12:53 GMT
RUN kong version
# Mon, 06 Jul 2020 23:12:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 Jul 2020 23:12:54 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 06 Jul 2020 23:12:54 GMT
STOPSIGNAL SIGQUIT
# Mon, 06 Jul 2020 23:12:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e9d9ca3d496619cb7d9dd321c5e1b12f499e234a4bfff523ed3169665df8b`  
		Last Modified: Mon, 06 Jul 2020 23:15:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e711916e1be27756a6cb02ebd3288f2789aaf6d952daa8592efd00c8268d640`  
		Last Modified: Mon, 06 Jul 2020 23:15:23 GMT  
		Size: 67.0 MB (67012871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7985b5e0b41e967fe49553c6262882988867ac8e7d086a81df1634ae7a108355`  
		Last Modified: Mon, 06 Jul 2020 23:15:03 GMT  
		Size: 647.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d62a2a35450bbecb38273fc4e53505709b0a408790497ddc5fc671911046c9`  
		Last Modified: Mon, 06 Jul 2020 23:15:03 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-alpine`

```console
$ docker pull kong@sha256:9da7678dcfa53e72c111e0808e25c8d2add5de1d9fed435b99ebd508b46ec8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:8ab38a1619b83fcde75726a683c365fb6eccaef9058e8bd9f37bb113c050adc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59535920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28952b67ba3794666dc118fb13b5d1fd043f1175a15b65e889dc4fe8e1206fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Mon, 22 Jun 2020 19:27:05 GMT
ARG KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:27:06 GMT
ENV KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:27:06 GMT
ARG KONG_SHA256=2f6d703b54c9da3787bdab1e38ec8c1ec70e4cb30751c7df021d97957704736d
# Mon, 22 Jun 2020 19:27:06 GMT
ENV KONG_SHA256=2f6d703b54c9da3787bdab1e38ec8c1ec70e4cb30751c7df021d97957704736d
# Mon, 22 Jun 2020 19:27:16 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Mon, 22 Jun 2020 19:27:16 GMT
COPY file:fa8375740fa706893b805c585210990194c529e023568323f95bd7d67be95132 in /docker-entrypoint.sh 
# Mon, 22 Jun 2020 19:27:17 GMT
USER kong
# Mon, 22 Jun 2020 19:27:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2020 19:27:17 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 22 Jun 2020 19:27:17 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2020 19:27:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e69e7b1c0aea7473e2ebdf44bfc933b632f3449d14ce0b2ed4395999a4d92`  
		Last Modified: Mon, 22 Jun 2020 19:29:32 GMT  
		Size: 56.7 MB (56721776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c1f62c47aea958010c7e08361b601d389ccb3a7ce0e42f1ab917b6426eedb4`  
		Last Modified: Mon, 22 Jun 2020 19:29:21 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-centos`

```console
$ docker pull kong@sha256:513e10ab873591c7748e52e67f916cc530bbd451cf54e3a583c4754088b83de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:48a8b309f4c9d55102e5927ae9c9720e2443b45dc1190a78472ba8f277628433
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133982638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebbd2b3a9c9454aac62b967315898a55a30b20fe3c6ed2693ed7bbb11c61b74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 21:54:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 21:54:26 GMT
ARG ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
ENV ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Mon, 22 Jun 2020 19:28:16 GMT
ARG KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:28:16 GMT
ENV KONG_VERSION=2.1.0beta.1
# Mon, 22 Jun 2020 19:28:17 GMT
ARG KONG_SHA256=cc6440089fce6f450c8fea5749753bf67fb92d4e3712de9aa50c1fd75997a770
# Mon, 22 Jun 2020 19:28:17 GMT
ENV KONG_SHA256=cc6440089fce6f450c8fea5749753bf67fb92d4e3712de9aa50c1fd75997a770
# Mon, 22 Jun 2020 19:28:41 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib zlib-devel 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Mon, 22 Jun 2020 19:28:42 GMT
COPY file:fa8375740fa706893b805c585210990194c529e023568323f95bd7d67be95132 in /docker-entrypoint.sh 
# Mon, 22 Jun 2020 19:28:42 GMT
USER kong
# Mon, 22 Jun 2020 19:28:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2020 19:28:42 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 22 Jun 2020 19:28:42 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2020 19:28:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce7701dd3817fcacdc04d8abfd7cd6ea61fe7f4d909903260a2ebe43fce007f`  
		Last Modified: Tue, 05 May 2020 22:02:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ae30896a07cad0a8dc8c498289c1a383fc9a1a7c85a2768bf3365f641709c6`  
		Last Modified: Mon, 22 Jun 2020 19:30:05 GMT  
		Size: 58.1 MB (58101671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8807af506f42b0df56df0d9011059d12539e6444b3ddbed6f2cf7b9558bbdf5`  
		Last Modified: Mon, 22 Jun 2020 19:29:54 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-ubuntu`

```console
$ docker pull kong@sha256:1debe57e06a25e631d306307570c837e8a71a61dd5e444039b43a17e1e5b7b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:706e03a0000f1092a515e10878a0b7378425e15ab19e535a16ec6c11211feb12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115984148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e4ae8713c898d85acdcd62f3cd6cfc06e5902d22e4ff3726cd7ea726c8cf0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:16:32 GMT
ARG ASSET=ce
# Tue, 07 Jul 2020 00:16:32 GMT
ENV ASSET=ce
# Tue, 07 Jul 2020 00:16:32 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Tue, 07 Jul 2020 00:16:32 GMT
ARG KONG_VERSION=2.1.0beta.1
# Tue, 07 Jul 2020 00:16:32 GMT
ENV KONG_VERSION=2.1.0beta.1
# Tue, 07 Jul 2020 00:17:16 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git     && { apt-get install -y --no-install-recommends zlibc || true; }     && { apt-get install -y --no-install-recommends zlib1g-dev || true; }     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Tue, 07 Jul 2020 00:17:16 GMT
COPY file:8cfc195cab364205f6c571f352a222ce4e5f1211c3309cce2e55fc785367559d in /docker-entrypoint.sh 
# Tue, 07 Jul 2020 00:17:16 GMT
USER kong
# Tue, 07 Jul 2020 00:17:17 GMT
RUN kong version
# Tue, 07 Jul 2020 00:17:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:17:18 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jul 2020 00:17:18 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jul 2020 00:17:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143c32b458621fe6c4f8e03075d63acff14f384d32857620905001d581d3c71c`  
		Last Modified: Tue, 07 Jul 2020 00:18:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2195fd3e9e4be6b1cd7d7ae16bf74957f22127aa2126a7ee95f636f36a701d`  
		Last Modified: Tue, 07 Jul 2020 00:19:02 GMT  
		Size: 71.6 MB (71607582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28a8234efe902d91d4eb48ded173b8068a2e57d88fe89959827793ddf3cd4bb`  
		Last Modified: Tue, 07 Jul 2020 00:18:48 GMT  
		Size: 647.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d74e5bd7de115fd006481a1411bf97131c1bc4111208a54f2f7816b85b6d4`  
		Last Modified: Tue, 07 Jul 2020 00:18:48 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d55cd823d7e8acad8b7474604cdc06be0839ccca3c4bd1248879deff3881e357
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107050701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b213d86338a74c4d64fd760078eeba41ce67bb851f7f72a27250cf56fe7832bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:11:52 GMT
ARG ASSET=ce
# Mon, 06 Jul 2020 23:11:52 GMT
ENV ASSET=ce
# Mon, 06 Jul 2020 23:11:53 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Mon, 06 Jul 2020 23:11:54 GMT
ARG KONG_VERSION=2.1.0beta.1
# Mon, 06 Jul 2020 23:11:54 GMT
ENV KONG_VERSION=2.1.0beta.1
# Mon, 06 Jul 2020 23:12:47 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-prerelease/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git     && { apt-get install -y --no-install-recommends zlibc || true; }     && { apt-get install -y --no-install-recommends zlib1g-dev || true; }     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Mon, 06 Jul 2020 23:12:50 GMT
COPY file:8cfc195cab364205f6c571f352a222ce4e5f1211c3309cce2e55fc785367559d in /docker-entrypoint.sh 
# Mon, 06 Jul 2020 23:12:51 GMT
USER kong
# Mon, 06 Jul 2020 23:12:53 GMT
RUN kong version
# Mon, 06 Jul 2020 23:12:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 Jul 2020 23:12:54 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 06 Jul 2020 23:12:54 GMT
STOPSIGNAL SIGQUIT
# Mon, 06 Jul 2020 23:12:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e9d9ca3d496619cb7d9dd321c5e1b12f499e234a4bfff523ed3169665df8b`  
		Last Modified: Mon, 06 Jul 2020 23:15:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e711916e1be27756a6cb02ebd3288f2789aaf6d952daa8592efd00c8268d640`  
		Last Modified: Mon, 06 Jul 2020 23:15:23 GMT  
		Size: 67.0 MB (67012871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7985b5e0b41e967fe49553c6262882988867ac8e7d086a81df1634ae7a108355`  
		Last Modified: Mon, 06 Jul 2020 23:15:03 GMT  
		Size: 647.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d62a2a35450bbecb38273fc4e53505709b0a408790497ddc5fc671911046c9`  
		Last Modified: Mon, 06 Jul 2020 23:15:03 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:32a09516a4fad6a7d42a90f7f754970555027a73e349b980a72c7120e00488b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:dc302feb438b82d99d70e7e140df748654b53341bde9725c7d663baa8fb9b5e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89025900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a800e1cef72354e6e0f6549c23e47d8622aed285f35e7ec340cd19dce577d01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Tue, 05 May 2020 00:19:57 GMT
ARG KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:19:57 GMT
ENV KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:19:57 GMT
ARG KONG_SHA256=457dd0172ae2de2e0b71ce625f78e06449faf38fd734dd6825eb7782d74cb77e
# Tue, 05 May 2020 00:19:57 GMT
ENV KONG_SHA256=457dd0172ae2de2e0b71ce625f78e06449faf38fd734dd6825eb7782d74cb77e
# Tue, 05 May 2020 00:20:09 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong
# Tue, 05 May 2020 00:20:10 GMT
COPY file:c7c95ad9b95e03a404039e7ee878ca4bb52cbcb965cd2d12c91037eb7a3b7e65 in /docker-entrypoint.sh 
# Tue, 05 May 2020 00:20:10 GMT
USER kong
# Tue, 05 May 2020 00:20:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 May 2020 00:20:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 May 2020 00:20:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 May 2020 00:20:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362c162bd1100f98c75c4f57997da5b9e28cd6ed876bf245131f63971c73f7aa`  
		Last Modified: Tue, 05 May 2020 00:22:58 GMT  
		Size: 86.2 MB (86211770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4da51840b66cea01c99f6efb58af2ac5bee97ac78b11d937f7bc2dca9ac4de`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:centos`

```console
$ docker pull kong@sha256:26b695f46f0401152bb06730abff6966a06a35c75d151ede1859b450a213df40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:0770a2caadebe3516c2b2e3a89f03f0b5ebe5ded765d4b9d89cc9e9107496ab2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125876109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33606e3edaee945be23e4e4e9a8afbc416da3421b00be80f861dec3045b53b2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 21:54:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 21:54:26 GMT
ARG ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
ENV ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Tue, 05 May 2020 21:54:27 GMT
ARG KONG_VERSION=2.0.4
# Tue, 05 May 2020 21:54:27 GMT
ENV KONG_VERSION=2.0.4
# Tue, 05 May 2020 21:54:27 GMT
ARG KONG_SHA256=16a934a7bc2e182f00f03bd75b67f4bdb483150b3820d33cab9b0c95539dd353
# Tue, 05 May 2020 21:54:27 GMT
ENV KONG_SHA256=16a934a7bc2e182f00f03bd75b67f4bdb483150b3820d33cab9b0c95539dd353
# Tue, 05 May 2020 21:54:46 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm &&         echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;     fi;     yum install -y -q unzip shadow-utils 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong
# Tue, 05 May 2020 21:54:47 GMT
COPY file:c7c95ad9b95e03a404039e7ee878ca4bb52cbcb965cd2d12c91037eb7a3b7e65 in /docker-entrypoint.sh 
# Tue, 05 May 2020 21:54:47 GMT
USER kong
# Tue, 05 May 2020 21:54:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 May 2020 21:54:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 May 2020 21:54:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 May 2020 21:54:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce7701dd3817fcacdc04d8abfd7cd6ea61fe7f4d909903260a2ebe43fce007f`  
		Last Modified: Tue, 05 May 2020 22:02:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c09eae848c2b3842c2e1b6863034e9fb2ca603d8438ae1ffa8d1f1dbd3d1593`  
		Last Modified: Tue, 05 May 2020 22:02:55 GMT  
		Size: 50.0 MB (49995157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a8e1c9ddcadf4475ac984587a95973290b72baed79445bbec7bddea3e7d3ad`  
		Last Modified: Tue, 05 May 2020 22:02:16 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:32a09516a4fad6a7d42a90f7f754970555027a73e349b980a72c7120e00488b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:dc302feb438b82d99d70e7e140df748654b53341bde9725c7d663baa8fb9b5e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89025900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a800e1cef72354e6e0f6549c23e47d8622aed285f35e7ec340cd19dce577d01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Tue, 05 May 2020 00:19:57 GMT
ARG KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:19:57 GMT
ENV KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:19:57 GMT
ARG KONG_SHA256=457dd0172ae2de2e0b71ce625f78e06449faf38fd734dd6825eb7782d74cb77e
# Tue, 05 May 2020 00:19:57 GMT
ENV KONG_SHA256=457dd0172ae2de2e0b71ce625f78e06449faf38fd734dd6825eb7782d74cb77e
# Tue, 05 May 2020 00:20:09 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong
# Tue, 05 May 2020 00:20:10 GMT
COPY file:c7c95ad9b95e03a404039e7ee878ca4bb52cbcb965cd2d12c91037eb7a3b7e65 in /docker-entrypoint.sh 
# Tue, 05 May 2020 00:20:10 GMT
USER kong
# Tue, 05 May 2020 00:20:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 May 2020 00:20:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 May 2020 00:20:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 May 2020 00:20:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362c162bd1100f98c75c4f57997da5b9e28cd6ed876bf245131f63971c73f7aa`  
		Last Modified: Tue, 05 May 2020 00:22:58 GMT  
		Size: 86.2 MB (86211770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4da51840b66cea01c99f6efb58af2ac5bee97ac78b11d937f7bc2dca9ac4de`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:e289d1d59f30d50b9705fb25f5d3e09c5e9f789c7d56cdaf5000adfc36d66287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:280df6e40ecdad6e7bc43ee4257ffe43902f3f0b30a4a5a0f60bc15bc64e19b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94313042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52318c270a779c2d2e695333c6f79efa3cb3fef73aa8f092891a6cccf9f830d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:16:32 GMT
ARG ASSET=ce
# Tue, 07 Jul 2020 00:16:32 GMT
ENV ASSET=ce
# Tue, 07 Jul 2020 00:16:32 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Tue, 07 Jul 2020 00:17:33 GMT
ARG KONG_VERSION=2.0.4
# Tue, 07 Jul 2020 00:17:33 GMT
ENV KONG_VERSION=2.0.4
# Tue, 07 Jul 2020 00:17:53 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb &&         apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong
# Tue, 07 Jul 2020 00:17:54 GMT
COPY file:7cd3b30326ffeaddc1253699208f97fb54711d4ae930aeeeff1e19ebf51cb561 in /docker-entrypoint.sh 
# Tue, 07 Jul 2020 00:17:54 GMT
USER kong
# Tue, 07 Jul 2020 00:17:55 GMT
RUN kong version
# Tue, 07 Jul 2020 00:17:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jul 2020 00:17:55 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jul 2020 00:17:55 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jul 2020 00:17:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143c32b458621fe6c4f8e03075d63acff14f384d32857620905001d581d3c71c`  
		Last Modified: Tue, 07 Jul 2020 00:18:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b973c91d253a303114da9230977c9f151dc3c925daec767151fcf3dfa12961`  
		Last Modified: Tue, 07 Jul 2020 00:19:20 GMT  
		Size: 49.9 MB (49936491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19141e6b35ee673101c4a8456210c18a82a96548c1d8ecea615eaabc46185d0a`  
		Last Modified: Tue, 07 Jul 2020 00:19:09 GMT  
		Size: 632.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2daef6cc11258da19c632b8132c7113fa861eb62bdfbba576e72b3686513ef6`  
		Last Modified: Tue, 07 Jul 2020 00:19:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f45baefb4365cf59fbfb8784a87835c07c003e6cd4d43061a622f595a87f9896
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87956868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaad0ea2000f7e8419a14d4050bd515e37846a9be657ce80e8743675ef6ed4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:11:52 GMT
ARG ASSET=ce
# Mon, 06 Jul 2020 23:11:52 GMT
ENV ASSET=ce
# Mon, 06 Jul 2020 23:11:53 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Mon, 06 Jul 2020 23:13:11 GMT
ARG KONG_VERSION=2.0.4
# Mon, 06 Jul 2020 23:13:11 GMT
ENV KONG_VERSION=2.0.4
# Mon, 06 Jul 2020 23:13:49 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb &&         apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong
# Mon, 06 Jul 2020 23:13:52 GMT
COPY file:7cd3b30326ffeaddc1253699208f97fb54711d4ae930aeeeff1e19ebf51cb561 in /docker-entrypoint.sh 
# Mon, 06 Jul 2020 23:13:52 GMT
USER kong
# Mon, 06 Jul 2020 23:13:54 GMT
RUN kong version
# Mon, 06 Jul 2020 23:13:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 Jul 2020 23:13:55 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 06 Jul 2020 23:13:56 GMT
STOPSIGNAL SIGQUIT
# Mon, 06 Jul 2020 23:13:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e9d9ca3d496619cb7d9dd321c5e1b12f499e234a4bfff523ed3169665df8b`  
		Last Modified: Mon, 06 Jul 2020 23:15:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167cc4fdbdcd6b1e42eefef9a0e843677603d721543bdd71fbb5fccfe0c784b`  
		Last Modified: Mon, 06 Jul 2020 23:15:45 GMT  
		Size: 47.9 MB (47919051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145f31f4d6fa8e388dcda72f41d13b4140883938ea81778a74cdc775a44e8c4e`  
		Last Modified: Mon, 06 Jul 2020 23:15:30 GMT  
		Size: 632.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627990a3dfb0b5ae178e48a22a9b7c41e7c01d057779a3d83dfc2f96e91d4b5c`  
		Last Modified: Mon, 06 Jul 2020 23:15:29 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
