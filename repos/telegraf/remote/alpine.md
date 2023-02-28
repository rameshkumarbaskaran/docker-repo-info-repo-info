## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:8f8543e81d2d4621b7db15c3175658fa27463332c2edafc1a984b393e8344ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:705bf72786ca3458dfb5899282a18cb5467973a6b8659bc1d2113cafec114501
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52499770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183712a92a73afbda6e7927241663239edc3e8f458c1d8dd45f4950a2a391b21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 09:58:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 11 Feb 2023 14:07:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Tue, 28 Feb 2023 01:37:17 GMT
ENV TELEGRAF_VERSION=1.25.3
# Tue, 28 Feb 2023 01:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Tue, 28 Feb 2023 01:37:23 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 28 Feb 2023 01:37:23 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Tue, 28 Feb 2023 01:37:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Feb 2023 01:37:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78609e30990ccbdf3bf8ff0fb97d9cc3f1a128207e6de80aae40ce96e63cd92c`  
		Last Modified: Sat, 11 Feb 2023 14:08:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fe5f60e0243cd70ce085e0773498f72d2e22f37d66e8d91308d81e17f4e844`  
		Last Modified: Sat, 11 Feb 2023 14:08:50 GMT  
		Size: 3.3 MB (3298280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6711fcfeaac5716d29975818839c1516a1b969f8daf4c2e5b46ca4f79257a73`  
		Last Modified: Tue, 28 Feb 2023 01:38:11 GMT  
		Size: 46.4 MB (46393123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc62e6281930eb3e2afb1f86a84c0cc7c81d97bb2a0929724e4d77255685f80`  
		Last Modified: Tue, 28 Feb 2023 01:38:04 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
