## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:746438d2fde97f2eda294b2b648d20e3863b2eb56d6778e70c64d2a4e37206db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a99d9fd20d35b275f645895336095e31f8746b6778768ab6d736731cc1395a9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64886619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5031258dbfba9472f0b4e1655f9b0d3b1af50f4f4936e21809de5044c1ea0dbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 20:24:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 11 Dec 2023 20:24:48 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Wed, 13 Dec 2023 18:32:19 GMT
ENV TELEGRAF_VERSION=1.29.1
# Wed, 13 Dec 2023 18:32:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 13 Dec 2023 18:32:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Dec 2023 18:32:27 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 13 Dec 2023 18:32:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Dec 2023 18:32:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a0a804738aec5dc0fcb4fd199dcec31ce20ba35442c1faf7dabd1365e5a224`  
		Last Modified: Mon, 11 Dec 2023 20:26:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae898eca22470e7dd671dcd09308fe50994c32849751def459aff8c21d37515`  
		Last Modified: Mon, 11 Dec 2023 20:26:03 GMT  
		Size: 2.6 MB (2612141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee88a1b2c02386041727092bd75604f2e54eb1b175b08c68ccc1d5520f83f3d`  
		Last Modified: Wed, 13 Dec 2023 18:33:12 GMT  
		Size: 58.9 MB (58865391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972039f3f1b1109c963230b23ec032bf5b5ed640889a9af8a35090c74a9b95cf`  
		Last Modified: Wed, 13 Dec 2023 18:33:02 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6491ef294608e410035cf0389fd644ae0e0041a4c5ffbda652cf2fd94bce4289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59314251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef61e4e596fba049cc7fa5801d366d22a477fb3226660ca2663904ed1b193d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 20:07:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 11 Dec 2023 20:07:21 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Wed, 13 Dec 2023 19:02:53 GMT
ENV TELEGRAF_VERSION=1.29.1
# Wed, 13 Dec 2023 19:03:02 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Wed, 13 Dec 2023 19:03:03 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 13 Dec 2023 19:03:03 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Wed, 13 Dec 2023 19:03:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Dec 2023 19:03:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f827e8bf907751a3e5b3169f3913e7b67c70b21c02477454501cd2043be3c67b`  
		Last Modified: Mon, 11 Dec 2023 20:08:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e495f22bdfc73e46af702cdb849f85f47df776e5075848c4a6ad77b02ec00f34`  
		Last Modified: Mon, 11 Dec 2023 20:08:05 GMT  
		Size: 2.7 MB (2694865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ffa696c997225f0e100e3803e1742a94a691d1adf95a0cc2a30a2bd6c20df8`  
		Last Modified: Wed, 13 Dec 2023 19:03:47 GMT  
		Size: 53.3 MB (53270987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1749e6213c0bbfa4de45d222ad57104f5dd806126875336a6f7ea3545133b9b6`  
		Last Modified: Wed, 13 Dec 2023 19:03:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
