## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:f2e57221f055c9353d3a2bfe47a26a7f5281bb32e2542959cf2965943d4618b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d74cbf1631a9d51c0aa773033d918cbca127457c817031d4148a939fc7336a03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60799662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68315ae79d6a73c9d69a54cafa0090f6e7fc7a022d57f0928dc813086e9001b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:05:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 20 Jul 2022 03:30:02 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 20 Jul 2022 03:30:15 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 20 Jul 2022 03:30:21 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 20 Jul 2022 03:30:21 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 20 Jul 2022 03:30:21 GMT
EXPOSE 8086
# Wed, 20 Jul 2022 03:30:21 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 Jul 2022 03:30:22 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 20 Jul 2022 03:30:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 20 Jul 2022 03:30:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 03:30:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e050afca26d1663052795a9809162a09fcb00af702e4f05a668eb44854faca9`  
		Last Modified: Wed, 20 Jul 2022 02:06:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411cfec0347a0975f1e043fa78d518fcad886c4a72474be83fb4d0ddc146a6ae`  
		Last Modified: Wed, 20 Jul 2022 03:32:38 GMT  
		Size: 1.5 MB (1475528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9da608a738b7e9b6f66e67682b7842c9b86a35ebbdb9c1c4df19fa4681db50f`  
		Last Modified: Wed, 20 Jul 2022 03:33:03 GMT  
		Size: 56.5 MB (56503672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371d2951083df444ba9efa39f9fe96be80a8a0f90bfcdf270c92eb9314f5a383`  
		Last Modified: Wed, 20 Jul 2022 03:32:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103c0d8712a1ffe169da968b12e0fd4601ec1a10f4b954efe5b6f187e48769e`  
		Last Modified: Wed, 20 Jul 2022 03:32:56 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7bfda9cb77d7347ab876ff50da2cece8d56fed58b17939c501375cb156eb21`  
		Last Modified: Wed, 20 Jul 2022 03:32:56 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
