## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:4b41ca5e02650aa6f69ece0393720f9eef1234b393280666a4d39f7b886f9025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:874bbafd3e33806adb27cb248a43882c44c611d256056bb3f24d984c73367734
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27526515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294907712664990c7434bd74d477d9f359ec8db78761b5e0b9261f2b6bee3c6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

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
# Wed, 01 Sep 2021 02:51:44 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 02:51:45 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 01 Sep 2021 02:51:45 GMT
EXPOSE 8091
# Wed, 01 Sep 2021 02:51:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Sep 2021 02:51:46 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 01 Sep 2021 02:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 02:51:47 GMT
CMD ["influxd-meta"]
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
	-	`sha256:e77a703875e9fd86c585c07c64ab93678e989235dd8e5c43573250dc593db5db`  
		Last Modified: Wed, 01 Sep 2021 02:56:08 GMT  
		Size: 23.3 MB (23293297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39817ad28ee23c81ceb2bda4b439c4280e380eb4fb1899301a80b25a5ae39319`  
		Last Modified: Wed, 01 Sep 2021 02:56:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9a94a0bd7c0d3d13dbec4538843c98da7b8e3bc45178d12fbd47e2768347ee`  
		Last Modified: Wed, 01 Sep 2021 02:56:05 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
