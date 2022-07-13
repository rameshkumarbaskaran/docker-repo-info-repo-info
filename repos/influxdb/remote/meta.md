## `influxdb:meta`

```console
$ docker pull influxdb@sha256:72f36335c339f3d365be5cad7f9efc0dd0298e5caa1cb05b0cb15e84d46de469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:e710a977c22ead9e10a121e8ea276ea49a976067fa58fb03d56cfb1f6709c6cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94448125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72faf02938c56010feb4d1977dc8c5cc6ea81c25f7d59cc9d3de5c63ac22bf18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Jul 2022 19:21:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 13 Jul 2022 19:21:33 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 13 Jul 2022 19:21:48 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 13 Jul 2022 19:21:48 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 13 Jul 2022 19:21:48 GMT
EXPOSE 8091
# Wed, 13 Jul 2022 19:21:48 GMT
VOLUME [/var/lib/influxdb]
# Wed, 13 Jul 2022 19:21:49 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 13 Jul 2022 19:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jul 2022 19:21:49 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d95ce0cb36c70b08627e5807cf2535a25d0914dcd172639cf3973c06f06b95`  
		Last Modified: Wed, 13 Jul 2022 19:23:07 GMT  
		Size: 2.9 KB (2896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd0b1bc8fdbd1b92f062d20ed3a989f6fcf737741a3c6155845d7d7dfeb281b`  
		Last Modified: Wed, 13 Jul 2022 19:24:02 GMT  
		Size: 23.4 MB (23412727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f64e8b68722c1276b0e1aac708dba5b9076f80609c162e2071e29d1808e6ea8`  
		Last Modified: Wed, 13 Jul 2022 19:23:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba114ec14c02440bb0ff8e28bd539d7bc66d99c77e4286002b1a78d983d5206`  
		Last Modified: Wed, 13 Jul 2022 19:23:56 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
