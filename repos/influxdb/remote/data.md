## `influxdb:data`

```console
$ docker pull influxdb@sha256:3a26d8253463ebe40259603fdd95c422e2de35288dc12467cb11231edc8b122c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:c8378b632179b2eda2bdaa7698666107e03b663be7d5c33d7e743e1f5c02176f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127797611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccaaeee2ad67dec020949950574fbe6f2e9450c25ac895353a50ab2ba8d102d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:01:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:01:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 09:10:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 09:10:26 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Thu, 23 Mar 2023 09:10:36 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 23 Mar 2023 09:10:36 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Mar 2023 09:10:36 GMT
EXPOSE 8086
# Thu, 23 Mar 2023 09:10:36 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Mar 2023 09:10:36 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Mar 2023 09:10:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Mar 2023 09:10:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 09:10:36 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a71c865a2c34678c6dea55e4b0928f751ee3c0ca91cace6e4e0578c534d6cf`  
		Last Modified: Thu, 23 Mar 2023 06:08:01 GMT  
		Size: 5.2 MB (5166592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670730c27c2eacf07897a6e94fe55423ea50b884d9c28161a283bbbf064d1124`  
		Last Modified: Thu, 23 Mar 2023 06:08:02 GMT  
		Size: 10.9 MB (10876735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165bd3b11d2827be7cfa74469262318a1b241fc5503b5910c21aa5e141e16ade`  
		Last Modified: Thu, 23 Mar 2023 09:12:27 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a9c23a27241249f72ee98af4999c43f9616df94d1caa64b90708d52245fde3`  
		Last Modified: Thu, 23 Mar 2023 09:12:49 GMT  
		Size: 56.7 MB (56705110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a47d1447e1d4241900ca4256f8fb5e77dcef39d90fb54d043c80c53365e444`  
		Last Modified: Thu, 23 Mar 2023 09:12:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179fd39fd26f0303b92f5b5ec454c7a04e75a3f3908c7545b9977929eab4d641`  
		Last Modified: Thu, 23 Mar 2023 09:12:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d332754aabe21f5227680757e6ba8be3341e5892df83c2c6d0e96bbd70bedd6`  
		Last Modified: Thu, 23 Mar 2023 09:12:42 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
