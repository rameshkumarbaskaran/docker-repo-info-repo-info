## `influxdb:meta`

```console
$ docker pull influxdb@sha256:30f30f5b057cf606140473f79615652422e09c408fd6f0107db5607ff2f6c25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:d68053f345c45796638d26c586cd0fe903d6d8b0c9a8511c1e4616dc9e0fa1c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84435640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21ae890173010bd7f4b96cce5b10fb023618ccd26c4f05aa345686187838d45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:09:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 09 Aug 2021 22:20:27 GMT
ENV INFLUXDB_VERSION=1.8.7-c1.8.7
# Mon, 09 Aug 2021 22:20:55 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Mon, 09 Aug 2021 22:20:55 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Mon, 09 Aug 2021 22:20:56 GMT
EXPOSE 8091
# Mon, 09 Aug 2021 22:20:56 GMT
VOLUME [/var/lib/influxdb]
# Mon, 09 Aug 2021 22:20:56 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Mon, 09 Aug 2021 22:20:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Aug 2021 22:20:56 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3caf86f5b9d8f8e63437571297df5fa6d454140b9c1985c47d6ad526da824`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 11.3 MB (11294469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c316554a558d4aa95c0be17c01e4a0366d6026a98eeba53dca5baa6091e815`  
		Last Modified: Thu, 22 Jul 2021 01:22:23 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656f0072b8c89a0c7b5308df04e67a1dcdff0073232d3ea6b21ab680d8075fc6`  
		Last Modified: Fri, 23 Jul 2021 02:13:04 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc8382c105d722cba20fb3e5be3616c07820e48e7ccd3e967296ddfe92dcdbb`  
		Last Modified: Mon, 09 Aug 2021 22:23:36 GMT  
		Size: 23.4 MB (23415582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82384e1bb1d98a237f20ecb5b1eb1718616488e96cb7ad22e46067dac2a198a9`  
		Last Modified: Mon, 09 Aug 2021 22:23:33 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e95119485c569f5f7e5080792b3f1b186d756e4761fdde3f52dfff274fd09f`  
		Last Modified: Mon, 09 Aug 2021 22:23:33 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
