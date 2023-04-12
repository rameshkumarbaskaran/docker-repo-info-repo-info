## `influxdb:data`

```console
$ docker pull influxdb@sha256:651fb015520279fc2eb70429e5e39a0cb27a00e373270af4abce43e1324d8bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:d8c700b1e793262594120826f9773525711d5da51c8a507f903a8e52e5eccd57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127804861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991f6378bce35ee5f4e6068f9d196d026a42957cba592edbe3d8faf0aa0406bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 14:03:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 12 Apr 2023 14:03:59 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 12 Apr 2023 14:04:05 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 12 Apr 2023 14:04:05 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 12 Apr 2023 14:04:05 GMT
EXPOSE 8086
# Wed, 12 Apr 2023 14:04:05 GMT
VOLUME [/var/lib/influxdb]
# Wed, 12 Apr 2023 14:04:06 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 12 Apr 2023 14:04:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 12 Apr 2023 14:04:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Apr 2023 14:04:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32b00312931323a7e65b8fcb723e6c767ed0e5b7b5ebca9059ebd8bab99bbf8`  
		Last Modified: Wed, 12 Apr 2023 14:05:37 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cf5d0ed10ace6baeea02705ffa1ffda74ce779efe566c6fe809b8394cc35e2`  
		Last Modified: Wed, 12 Apr 2023 14:05:59 GMT  
		Size: 56.7 MB (56705107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d3b9ddf0193b06f898d957b9b6e124283fcf97ba7145e80b4600cfd6d665bd`  
		Last Modified: Wed, 12 Apr 2023 14:05:52 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437cc0e198df5b2772d7092253d0eef4b36ee456285c417834d11e3c0c1c6582`  
		Last Modified: Wed, 12 Apr 2023 14:05:52 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be58dc3ea55fc0f5be05a6b9f6db5b99ced026fe55b99e291afe6bdefd620e29`  
		Last Modified: Wed, 12 Apr 2023 14:05:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
