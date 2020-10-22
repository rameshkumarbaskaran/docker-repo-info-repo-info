## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:fa9c29387c8360d444e5c97c333e506614e86fc06f14c0c95e8b2e3a58a3f20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b22e31d531bfa7252dec3a1c25cf632813e5b875d98720ac50213d50feeb0f23
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68808650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8547609c51108d14614f1352838a0d8d72bd96c56fa9bd5ee72012f05c83daf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:28:23 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:29:36 GMT
ENV INFLUXDB_VERSION=1.8.3
# Thu, 22 Oct 2020 04:29:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:29:49 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 22 Oct 2020 04:29:49 GMT
EXPOSE 8086
# Thu, 22 Oct 2020 04:29:49 GMT
VOLUME [/var/lib/influxdb]
# Thu, 22 Oct 2020 04:29:50 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 22 Oct 2020 04:29:50 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 22 Oct 2020 04:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:29:51 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f09710cb1e9d1e2b329758d6e450a28347bc3d5b9279be1c2f97edf904405`  
		Last Modified: Thu, 22 Oct 2020 04:31:13 GMT  
		Size: 1.3 MB (1303321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65afcd077387f3004aa678cd1a97c4ab452ef130c1dabb9379fd8a8ea02bf0c1`  
		Last Modified: Thu, 22 Oct 2020 04:32:12 GMT  
		Size: 64.7 MB (64706602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5ed56e1e804b4e14492088d5cdc079f81cce8c2be7a2f2e2a5a9f1fadbb5d2`  
		Last Modified: Thu, 22 Oct 2020 04:32:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff7ff23b8fd0e2f766fea8d90029c074f251d78186f990af67c6c5d8f58d962`  
		Last Modified: Thu, 22 Oct 2020 04:32:02 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4a837504c80f785d2225635ef420bb90097f8c3f80b9311949691c26c7912`  
		Last Modified: Thu, 22 Oct 2020 04:32:01 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
