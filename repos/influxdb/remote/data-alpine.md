## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:c0779c43dfcee8dc8e8e1c9d3253007b036db2e09e1d767b5770f6c6cbe878e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e2d060e0434d175503db7d15b6295133a8c3111eb5e70e9a771cc0229aa76be8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61352869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2001a94dffaf3e6bb1a5eb27e0d279e36d434b03e3f1f5c550467ddb0d5a79bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:09:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 15 Jun 2023 00:09:37 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 15 Jun 2023 00:09:49 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Thu, 15 Jun 2023 00:09:58 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 15 Jun 2023 00:09:58 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 15 Jun 2023 00:09:58 GMT
EXPOSE 8086
# Thu, 15 Jun 2023 00:09:58 GMT
VOLUME [/var/lib/influxdb]
# Thu, 15 Jun 2023 00:09:58 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 15 Jun 2023 00:09:58 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 15 Jun 2023 00:09:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 00:09:59 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2214dfdd928ecf1e62b4f8e2a9a59608a27026918bc2c56798c200b89a66607`  
		Last Modified: Thu, 15 Jun 2023 00:11:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777733a36019c90975436d08f29c75a0e8bdb7a267141dc5334b3c8b56ba18b5`  
		Last Modified: Thu, 15 Jun 2023 00:11:45 GMT  
		Size: 1.5 MB (1472400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f212f543d7c0393d55b4940b209a666debc0934e4fe7813a47e24992610fd6db`  
		Last Modified: Thu, 15 Jun 2023 00:12:09 GMT  
		Size: 56.5 MB (56503680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7a5e09687e6f697e7241fbe5448dee7d5dbf8ba47c8e9713852bf15b36edcc`  
		Last Modified: Thu, 15 Jun 2023 00:12:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9a49fa1b54c5a3e6357da24c8bdeb3659deb6957ab4ff6e808718c27a9e6f7`  
		Last Modified: Thu, 15 Jun 2023 00:12:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb16398d95b80fec557b5e6cb101bb39934712eaf0c697d9c46169c2b164d9f`  
		Last Modified: Thu, 15 Jun 2023 00:12:01 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
