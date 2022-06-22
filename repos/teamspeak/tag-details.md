<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `teamspeak`

-	[`teamspeak:3.13`](#teamspeak313)
-	[`teamspeak:3.13.7`](#teamspeak3137)
-	[`teamspeak:latest`](#teamspeaklatest)

## `teamspeak:3.13`

```console
$ docker pull teamspeak@sha256:f03f4d2f97691c3bc81b1c34b0a760713d5bd9d0d738609d21dd1f9eec3a987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `teamspeak:3.13` - linux; amd64

```console
$ docker pull teamspeak@sha256:5d5f6afd552e808702cbeec3abcd809296a268bd2c05099335b0a5063eeb98c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13497596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3860da3e61c25af36441b440fe4ccb76d7bcd45b83d4a9d5ed2b4863f3b7d628`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:43:51 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq
# Tue, 05 Apr 2022 09:43:51 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Tue, 05 Apr 2022 09:43:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Wed, 22 Jun 2022 21:36:40 GMT
ARG TEAMSPEAK_CHECKSUM=897c4bc24588bf35e65da4cee1b6b0798687827f3e4d915dcabed785f55e573f
# Wed, 22 Jun 2022 21:36:40 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Wed, 22 Jun 2022 21:36:43 GMT
# ARGS: TEAMSPEAK_CHECKSUM=897c4bc24588bf35e65da4cee1b6b0798687827f3e4d915dcabed785f55e573f TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib
# Wed, 22 Jun 2022 21:36:43 GMT
VOLUME [/var/ts3server/]
# Wed, 22 Jun 2022 21:36:43 GMT
WORKDIR /var/ts3server/
# Wed, 22 Jun 2022 21:36:43 GMT
EXPOSE 10011 30033 9987/udp
# Wed, 22 Jun 2022 21:36:43 GMT
COPY file:d9f653f53e40ea33be02ca61f8194eb1a4147066050f721a3172007f06bb834c in /opt/ts3server 
# Wed, 22 Jun 2022 21:36:43 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 22 Jun 2022 21:36:43 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e2a3e53f7b63d3b584a2f90666a9bf53058b5909fe8d100b2fdd33af737fd3`  
		Last Modified: Tue, 05 Apr 2022 09:44:05 GMT  
		Size: 1.4 MB (1425643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94580f7d0016c73ceb27fa192cc5db03b877381b0cdf079fb1b31df3a769e34b`  
		Last Modified: Tue, 05 Apr 2022 09:44:05 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4befeb9003fee226d8ffbcccc17742f3733b8ba0ecf2d42912e289ccd9844de1`  
		Last Modified: Wed, 22 Jun 2022 21:36:54 GMT  
		Size: 9.2 MB (9249757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d747c92ef92e47ef91c0dddffe6f2f3e700a7f2ed8b65f33cbec235d2b614f2`  
		Last Modified: Wed, 22 Jun 2022 21:36:53 GMT  
		Size: 1.6 KB (1567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `teamspeak:3.13.7`

```console
$ docker pull teamspeak@sha256:f03f4d2f97691c3bc81b1c34b0a760713d5bd9d0d738609d21dd1f9eec3a987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `teamspeak:3.13.7` - linux; amd64

```console
$ docker pull teamspeak@sha256:5d5f6afd552e808702cbeec3abcd809296a268bd2c05099335b0a5063eeb98c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13497596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3860da3e61c25af36441b440fe4ccb76d7bcd45b83d4a9d5ed2b4863f3b7d628`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:43:51 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq
# Tue, 05 Apr 2022 09:43:51 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Tue, 05 Apr 2022 09:43:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Wed, 22 Jun 2022 21:36:40 GMT
ARG TEAMSPEAK_CHECKSUM=897c4bc24588bf35e65da4cee1b6b0798687827f3e4d915dcabed785f55e573f
# Wed, 22 Jun 2022 21:36:40 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Wed, 22 Jun 2022 21:36:43 GMT
# ARGS: TEAMSPEAK_CHECKSUM=897c4bc24588bf35e65da4cee1b6b0798687827f3e4d915dcabed785f55e573f TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib
# Wed, 22 Jun 2022 21:36:43 GMT
VOLUME [/var/ts3server/]
# Wed, 22 Jun 2022 21:36:43 GMT
WORKDIR /var/ts3server/
# Wed, 22 Jun 2022 21:36:43 GMT
EXPOSE 10011 30033 9987/udp
# Wed, 22 Jun 2022 21:36:43 GMT
COPY file:d9f653f53e40ea33be02ca61f8194eb1a4147066050f721a3172007f06bb834c in /opt/ts3server 
# Wed, 22 Jun 2022 21:36:43 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 22 Jun 2022 21:36:43 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e2a3e53f7b63d3b584a2f90666a9bf53058b5909fe8d100b2fdd33af737fd3`  
		Last Modified: Tue, 05 Apr 2022 09:44:05 GMT  
		Size: 1.4 MB (1425643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94580f7d0016c73ceb27fa192cc5db03b877381b0cdf079fb1b31df3a769e34b`  
		Last Modified: Tue, 05 Apr 2022 09:44:05 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4befeb9003fee226d8ffbcccc17742f3733b8ba0ecf2d42912e289ccd9844de1`  
		Last Modified: Wed, 22 Jun 2022 21:36:54 GMT  
		Size: 9.2 MB (9249757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d747c92ef92e47ef91c0dddffe6f2f3e700a7f2ed8b65f33cbec235d2b614f2`  
		Last Modified: Wed, 22 Jun 2022 21:36:53 GMT  
		Size: 1.6 KB (1567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:f03f4d2f97691c3bc81b1c34b0a760713d5bd9d0d738609d21dd1f9eec3a987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:5d5f6afd552e808702cbeec3abcd809296a268bd2c05099335b0a5063eeb98c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13497596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3860da3e61c25af36441b440fe4ccb76d7bcd45b83d4a9d5ed2b4863f3b7d628`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:43:51 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq
# Tue, 05 Apr 2022 09:43:51 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Tue, 05 Apr 2022 09:43:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Wed, 22 Jun 2022 21:36:40 GMT
ARG TEAMSPEAK_CHECKSUM=897c4bc24588bf35e65da4cee1b6b0798687827f3e4d915dcabed785f55e573f
# Wed, 22 Jun 2022 21:36:40 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Wed, 22 Jun 2022 21:36:43 GMT
# ARGS: TEAMSPEAK_CHECKSUM=897c4bc24588bf35e65da4cee1b6b0798687827f3e4d915dcabed785f55e573f TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib
# Wed, 22 Jun 2022 21:36:43 GMT
VOLUME [/var/ts3server/]
# Wed, 22 Jun 2022 21:36:43 GMT
WORKDIR /var/ts3server/
# Wed, 22 Jun 2022 21:36:43 GMT
EXPOSE 10011 30033 9987/udp
# Wed, 22 Jun 2022 21:36:43 GMT
COPY file:d9f653f53e40ea33be02ca61f8194eb1a4147066050f721a3172007f06bb834c in /opt/ts3server 
# Wed, 22 Jun 2022 21:36:43 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 22 Jun 2022 21:36:43 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e2a3e53f7b63d3b584a2f90666a9bf53058b5909fe8d100b2fdd33af737fd3`  
		Last Modified: Tue, 05 Apr 2022 09:44:05 GMT  
		Size: 1.4 MB (1425643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94580f7d0016c73ceb27fa192cc5db03b877381b0cdf079fb1b31df3a769e34b`  
		Last Modified: Tue, 05 Apr 2022 09:44:05 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4befeb9003fee226d8ffbcccc17742f3733b8ba0ecf2d42912e289ccd9844de1`  
		Last Modified: Wed, 22 Jun 2022 21:36:54 GMT  
		Size: 9.2 MB (9249757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d747c92ef92e47ef91c0dddffe6f2f3e700a7f2ed8b65f33cbec235d2b614f2`  
		Last Modified: Wed, 22 Jun 2022 21:36:53 GMT  
		Size: 1.6 KB (1567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
