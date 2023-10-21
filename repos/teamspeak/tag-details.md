<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `teamspeak`

-	[`teamspeak:3.13`](#teamspeak313)
-	[`teamspeak:3.13.7`](#teamspeak3137)
-	[`teamspeak:latest`](#teamspeaklatest)

## `teamspeak:3.13`

```console
$ docker pull teamspeak@sha256:cfdeb278e1838b9db4b47f493af0b45cad30586d5f97af2a87eb90f86a0d6467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `teamspeak:3.13` - linux; amd64

```console
$ docker pull teamspeak@sha256:a2ccf9bf830bd59436a01be0c692fba5360a63f90c8c8ea1593b622bf61029f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13970727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122d1f6460fdd340e171d00e0f77b9f46a765552f851b2bcc5646ff8834476fe`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 03:40:56 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq
# Sat, 21 Oct 2023 03:40:57 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Sat, 21 Oct 2023 03:40:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Sat, 21 Oct 2023 03:40:57 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Sat, 21 Oct 2023 03:40:57 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Sat, 21 Oct 2023 03:41:01 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib
# Sat, 21 Oct 2023 03:41:01 GMT
VOLUME [/var/ts3server/]
# Sat, 21 Oct 2023 03:41:02 GMT
WORKDIR /var/ts3server/
# Sat, 21 Oct 2023 03:41:02 GMT
EXPOSE 10011 30033 9987/udp
# Sat, 21 Oct 2023 03:41:02 GMT
COPY file:d9f653f53e40ea33be02ca61f8194eb1a4147066050f721a3172007f06bb834c in /opt/ts3server 
# Sat, 21 Oct 2023 03:41:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 21 Oct 2023 03:41:02 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081955062f61d69bbb7f1b23ae29cae1e3c8fa4831ae1edebd9790bdf7c0feda`  
		Last Modified: Sat, 21 Oct 2023 03:41:12 GMT  
		Size: 1.3 MB (1316512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4036272adc44ecbd23a715748426c917d39fa3f477bce285e99de7d3bd305478`  
		Last Modified: Sat, 21 Oct 2023 03:41:12 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d486e1585bac2daca06be305fcfa134c27044b10adc9ca4490a64e9db139ff`  
		Last Modified: Sat, 21 Oct 2023 03:41:13 GMT  
		Size: 9.2 MB (9249356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee97e4c50c163eb9792f8b99bbf90782e9ff1d781ce46706d4347c792395c65`  
		Last Modified: Sat, 21 Oct 2023 03:41:11 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `teamspeak:3.13.7`

```console
$ docker pull teamspeak@sha256:cfdeb278e1838b9db4b47f493af0b45cad30586d5f97af2a87eb90f86a0d6467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `teamspeak:3.13.7` - linux; amd64

```console
$ docker pull teamspeak@sha256:a2ccf9bf830bd59436a01be0c692fba5360a63f90c8c8ea1593b622bf61029f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13970727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122d1f6460fdd340e171d00e0f77b9f46a765552f851b2bcc5646ff8834476fe`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 03:40:56 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq
# Sat, 21 Oct 2023 03:40:57 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Sat, 21 Oct 2023 03:40:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Sat, 21 Oct 2023 03:40:57 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Sat, 21 Oct 2023 03:40:57 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Sat, 21 Oct 2023 03:41:01 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib
# Sat, 21 Oct 2023 03:41:01 GMT
VOLUME [/var/ts3server/]
# Sat, 21 Oct 2023 03:41:02 GMT
WORKDIR /var/ts3server/
# Sat, 21 Oct 2023 03:41:02 GMT
EXPOSE 10011 30033 9987/udp
# Sat, 21 Oct 2023 03:41:02 GMT
COPY file:d9f653f53e40ea33be02ca61f8194eb1a4147066050f721a3172007f06bb834c in /opt/ts3server 
# Sat, 21 Oct 2023 03:41:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 21 Oct 2023 03:41:02 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081955062f61d69bbb7f1b23ae29cae1e3c8fa4831ae1edebd9790bdf7c0feda`  
		Last Modified: Sat, 21 Oct 2023 03:41:12 GMT  
		Size: 1.3 MB (1316512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4036272adc44ecbd23a715748426c917d39fa3f477bce285e99de7d3bd305478`  
		Last Modified: Sat, 21 Oct 2023 03:41:12 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d486e1585bac2daca06be305fcfa134c27044b10adc9ca4490a64e9db139ff`  
		Last Modified: Sat, 21 Oct 2023 03:41:13 GMT  
		Size: 9.2 MB (9249356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee97e4c50c163eb9792f8b99bbf90782e9ff1d781ce46706d4347c792395c65`  
		Last Modified: Sat, 21 Oct 2023 03:41:11 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:cfdeb278e1838b9db4b47f493af0b45cad30586d5f97af2a87eb90f86a0d6467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:a2ccf9bf830bd59436a01be0c692fba5360a63f90c8c8ea1593b622bf61029f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13970727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122d1f6460fdd340e171d00e0f77b9f46a765552f851b2bcc5646ff8834476fe`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 03:40:56 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq
# Sat, 21 Oct 2023 03:40:57 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Sat, 21 Oct 2023 03:40:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Sat, 21 Oct 2023 03:40:57 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Sat, 21 Oct 2023 03:40:57 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Sat, 21 Oct 2023 03:41:01 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib
# Sat, 21 Oct 2023 03:41:01 GMT
VOLUME [/var/ts3server/]
# Sat, 21 Oct 2023 03:41:02 GMT
WORKDIR /var/ts3server/
# Sat, 21 Oct 2023 03:41:02 GMT
EXPOSE 10011 30033 9987/udp
# Sat, 21 Oct 2023 03:41:02 GMT
COPY file:d9f653f53e40ea33be02ca61f8194eb1a4147066050f721a3172007f06bb834c in /opt/ts3server 
# Sat, 21 Oct 2023 03:41:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 21 Oct 2023 03:41:02 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081955062f61d69bbb7f1b23ae29cae1e3c8fa4831ae1edebd9790bdf7c0feda`  
		Last Modified: Sat, 21 Oct 2023 03:41:12 GMT  
		Size: 1.3 MB (1316512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4036272adc44ecbd23a715748426c917d39fa3f477bce285e99de7d3bd305478`  
		Last Modified: Sat, 21 Oct 2023 03:41:12 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d486e1585bac2daca06be305fcfa134c27044b10adc9ca4490a64e9db139ff`  
		Last Modified: Sat, 21 Oct 2023 03:41:13 GMT  
		Size: 9.2 MB (9249356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee97e4c50c163eb9792f8b99bbf90782e9ff1d781ce46706d4347c792395c65`  
		Last Modified: Sat, 21 Oct 2023 03:41:11 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
