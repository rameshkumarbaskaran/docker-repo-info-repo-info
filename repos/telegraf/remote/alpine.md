## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:314108cc28917dd404d9f5f925a79ad058a5db1a6fcdfa7b7bfe6771235e5eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:93d6455dbb278143a257d82437c05cb956a3fd9a6bebf5b18f4b0149f5494641
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41645259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc99b10f752475d0b5baf65182c32a2caea4bac1657d72b47b84a218ab782bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 03 Nov 2021 19:44:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec &&     update-ca-certificates
# Wed, 03 Nov 2021 19:44:41 GMT
ENV TELEGRAF_VERSION=1.20.3
# Wed, 03 Nov 2021 19:44:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 03 Nov 2021 19:44:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:50 GMT
COPY file:4071aa7d94da140b944f5aaf032330509821a974e13349f4a3682e3368362128 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:50 GMT
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
	-	`sha256:4bc5969994ddff3cc06380d4484d56d3001e9b843686d9d8e2df71ab1a5bfb87`  
		Last Modified: Wed, 03 Nov 2021 19:45:21 GMT  
		Size: 3.4 MB (3371089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3f6d84ea81248992b415c62942686816e6f3afa27c6bfc47d8d4fdfcbd5b50`  
		Last Modified: Wed, 03 Nov 2021 19:46:25 GMT  
		Size: 35.5 MB (35459363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc2ae9653b2fdf734ac5e280179840f825a6d5d86db796fec9daf63e3e30de9`  
		Last Modified: Wed, 03 Nov 2021 19:46:19 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
