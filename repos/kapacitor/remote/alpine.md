## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:d48aec6275c8b765a0b14b675ccbbd95bb0f0f0030c8ef2cbf2b213a9b397845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7d712ed195eab169db2ebdc0e4ab19e0dc00ea7202beae8c37a55669bfb92f8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63761631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd07fd9194d52977eeb93e86964207ca489379bbc7739a3c8e4fa27541bcb90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:05:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 20 Jul 2022 02:05:17 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 20 Jul 2022 03:40:05 GMT
ENV KAPACITOR_VERSION=1.6.4
# Wed, 20 Jul 2022 03:40:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 20 Jul 2022 03:40:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 20 Jul 2022 03:40:12 GMT
EXPOSE 9092
# Wed, 20 Jul 2022 03:40:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 20 Jul 2022 03:40:13 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 20 Jul 2022 03:40:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 03:40:13 GMT
CMD ["kapacitord"]
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
	-	`sha256:aeebdc01d98dee3aaf4ffd272bcd262929382ded7430969574238b3839c1f52b`  
		Last Modified: Wed, 20 Jul 2022 02:06:16 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0706409a0f83f12bf9b4de0aa9277a3fc34e3a6d2aa14632b8393b090fa45198`  
		Last Modified: Wed, 20 Jul 2022 03:40:50 GMT  
		Size: 60.7 MB (60670840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a164d8cb8bc1c1e81f72e702f914263383402b2802afa5c88db7685ffc6db507`  
		Last Modified: Wed, 20 Jul 2022 03:40:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb350df51e55e605efb98d31837258fb567bba1a587e32272e1c8f000aff9905`  
		Last Modified: Wed, 20 Jul 2022 03:40:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
