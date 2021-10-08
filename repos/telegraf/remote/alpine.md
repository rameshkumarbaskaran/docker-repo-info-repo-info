## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:a5fac131412fe7078fb4b7d6d8c4edc5016c984c69cbf1ee787ff59ed5d896c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:884120aaa5b052fcb8727d4def67519b2bb9f697ae20efec50097721abb4a5dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40758696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135f23862b5d9b6b00e3540179e34be36eb001c54cb5344ed55554a7d73802f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Sep 2021 22:24:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 08 Oct 2021 17:31:44 GMT
ENV TELEGRAF_VERSION=1.20.2
# Fri, 08 Oct 2021 17:31:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 08 Oct 2021 17:31:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 08 Oct 2021 17:31:56 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Fri, 08 Oct 2021 17:31:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Oct 2021 17:31:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758daa9673013581700790c0ac7a9855a70445ef1c41bfc2d0ab94288ab13a6b`  
		Last Modified: Mon, 20 Sep 2021 22:25:51 GMT  
		Size: 3.3 MB (3348558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eafdaa25d6c53cc5132e20cbe015727e3bb384607caf6c76ca71f527bfba272`  
		Last Modified: Fri, 08 Oct 2021 17:32:44 GMT  
		Size: 34.6 MB (34595357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d9340b120badda5a4cd2792ac218ece7061af283ead0fbbd6ca756da19a8c2`  
		Last Modified: Fri, 08 Oct 2021 17:32:38 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
