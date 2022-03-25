## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:07d242f6b8222a6f0e531ef665ec0403d10abc2b251a04087a49e5d5b20f9a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:ba629122f0f1096c6ac9cd97e085351febb17d16fbb9eae2168aea3f7a75f165
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63759302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ece327d562ac124fe4cfcf4c6ad1de857e89f46f45a54e2506c2cd4a25a249`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 24 Mar 2022 22:24:39 GMT
ENV KAPACITOR_VERSION=1.6.4
# Thu, 24 Mar 2022 22:24:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 24 Mar 2022 22:24:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 24 Mar 2022 22:24:48 GMT
EXPOSE 9092
# Thu, 24 Mar 2022 22:24:48 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 24 Mar 2022 22:24:48 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 24 Mar 2022 22:24:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 22:24:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b74230ee1ffa356cb93a66b538c6de055b31a91af446db57facd26adf8b52d`  
		Last Modified: Thu, 24 Mar 2022 22:25:34 GMT  
		Size: 60.7 MB (60670854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0471533845bde002bebdbed8fa921a4a78d0e52b4bbfcc055fc903fa1ed4660`  
		Last Modified: Thu, 24 Mar 2022 22:25:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ea9c4c1fc429a5f60ef4c53efb82955df2ef029f31c5bc9af7abbb6fe95e7e`  
		Last Modified: Thu, 24 Mar 2022 22:25:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
