## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:d2655f2b805934a42733bd10f6d67c87f5175a563a4c5b5e7ef065cb896efae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7b6f1ada333030c175e3ce54dcf4dba2453154e289352c09f744fd13a8f7c289
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60740006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01dd2c62b9c308a0d8ec9e8bd1800b4eac0f18b95905da025fb35a3033bbf0b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 02:50:13 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 02:51:23 GMT
ENV INFLUXDB_VERSION=1.8.9-c1.8.9
# Wed, 01 Sep 2021 02:51:30 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 02:51:30 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 01 Sep 2021 02:51:31 GMT
EXPOSE 8086
# Wed, 01 Sep 2021 02:51:31 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Sep 2021 02:51:31 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 01 Sep 2021 02:51:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Sep 2021 02:51:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 02:51:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0008876e8a91e0b35d1083692e19678d4f5b242f7b3cc6e9767809cd9ff4f491`  
		Last Modified: Wed, 01 Sep 2021 02:54:23 GMT  
		Size: 1.4 MB (1430763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9b61b36682f61ca469cdb0f5380bb618d52abe59d3e2d7da9972e5faf8200c`  
		Last Modified: Wed, 01 Sep 2021 02:55:51 GMT  
		Size: 56.5 MB (56505586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63c9aa64d0bcf7674f1364b019c0178d1e5152999f0ee698f761ad1de835e54`  
		Last Modified: Wed, 01 Sep 2021 02:55:42 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8306a4ff27c480f93352f427ec85705bbd45877ef4d56acf24d3fe8e405e96c`  
		Last Modified: Wed, 01 Sep 2021 02:55:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205ead3baac5aa10c87c1747f3c66a27274e1eb7f7615e5b83f1fee0ea563102`  
		Last Modified: Wed, 01 Sep 2021 02:55:42 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
