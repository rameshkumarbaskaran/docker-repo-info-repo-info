## `telegraf:latest`

```console
$ docker pull telegraf@sha256:3e2895cc855e47e3a2b674972addf259db397e40727a60c2e4a91f103d4ace1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:6d309ce4ec0c722688638a32fddc67fdb7ea6e387d22a22d5b0c96eea565a6e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143150759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245ed83f748572e64d13c688a308dc0974fe6ed0f5f7c82f9c05b4cab67a6bc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:54 GMT
ADD file:e530b0563ea53d97b2f28e62149a665900196f86611df99a88c7a8ab2097b95d in / 
# Mon, 12 Jun 2023 23:20:54 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 19:52:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 19:52:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Jun 2023 19:53:19 GMT
ENV TELEGRAF_VERSION=1.27.0
# Tue, 13 Jun 2023 19:53:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Jun 2023 19:53:24 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 13 Jun 2023 19:53:24 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:53:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:53:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:93c2d578e4211e82e47e7ada9ed05d1869a2362c6f7509f2ee8d91ccebfb7fbd`  
		Last Modified: Mon, 12 Jun 2023 23:26:08 GMT  
		Size: 55.1 MB (55055162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87e6f3487e1d7e61ee7a415e0ced4eb6f0b3484eb1e15a4339d110d3cadf899`  
		Last Modified: Tue, 13 Jun 2023 03:37:33 GMT  
		Size: 15.8 MB (15760332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a1bd817f4c2f4115a0999d4f802752e4012c281b24cb70d83cfe54ae359eae`  
		Last Modified: Tue, 13 Jun 2023 19:53:43 GMT  
		Size: 18.8 MB (18760197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e8cc37fc85816666c16f78e6251af17182a69419caf030788879fe7a9880e2`  
		Last Modified: Tue, 13 Jun 2023 19:53:39 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d7f8aeba4eca40e57044bd41a26d2581d5a39c201dcbf489d069dd3bd14c2f`  
		Last Modified: Tue, 13 Jun 2023 19:54:20 GMT  
		Size: 53.6 MB (53572918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9263108d6f4924541d80366aae40641cca1b2542ea12df478ba470193dcd1e28`  
		Last Modified: Tue, 13 Jun 2023 19:54:12 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ebb8eedc17d40eba47972a6fa26049b9443c2de34bf67f249fe799de1858e8e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132683761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191c149d327519175115201e60c03b2a43ffaa6cfc8bc55f9bfb478ec611550f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 May 2023 00:57:45 GMT
ADD file:d8748d34e524d93a6df76d2a8ea8ca32ca04897521719f9f1f2a88ec692dd69e in / 
# Tue, 23 May 2023 00:57:45 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:54:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 23:16:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 23:16:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 12 Jun 2023 20:14:08 GMT
ENV TELEGRAF_VERSION=1.27.0
# Mon, 12 Jun 2023 20:14:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 12 Jun 2023 20:14:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 12 Jun 2023 20:14:16 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 12 Jun 2023 20:14:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jun 2023 20:14:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:29949e2d07dd1e283862cb4c3d4ec3043f1d54a1ac59f7b7a998ed9038a0243c`  
		Last Modified: Tue, 23 May 2023 01:01:23 GMT  
		Size: 50.2 MB (50210000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaf40f65a7bdc041e615a5825b6ae62227f6a7ceec53af9e210fb62293e0bd2`  
		Last Modified: Tue, 23 May 2023 10:04:45 GMT  
		Size: 14.9 MB (14868582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fa44955cadb3e3d3d5fe86d27c4488b7e7aac3646248014cc6911ff7195039`  
		Last Modified: Tue, 23 May 2023 23:16:55 GMT  
		Size: 17.5 MB (17462338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e198f55fd4a95bb93ec5e99c99bf326613e1a6bad919dda290b804d7b627934`  
		Last Modified: Tue, 23 May 2023 23:16:52 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf35db1597432e97f40b5654396929e3122a11d7bb80f6f386019f84b8d3c17`  
		Last Modified: Mon, 12 Jun 2023 20:14:36 GMT  
		Size: 50.1 MB (50140690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789bf4d947e2c7713739b13712bddf384d8336e4e2380a55e6c572f8b6127a2a`  
		Last Modified: Mon, 12 Jun 2023 20:14:27 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0a5b380d04db9ca43e02c93374ecc03fdc8cb8de54928522af3a276f0d005c80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136782425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46ddc43978731f3dbb7730d557d92847e6067918a6e9eec74f72207f71e61dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:32:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:32:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Jun 2023 18:32:27 GMT
ENV TELEGRAF_VERSION=1.27.0
# Tue, 13 Jun 2023 18:32:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 13 Jun 2023 18:32:31 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 13 Jun 2023 18:32:31 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Tue, 13 Jun 2023 18:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 18:32:31 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c9c60873892c6128382a04355bf76576dd23d87e5fdad03161dba5a2db45e`  
		Last Modified: Tue, 13 Jun 2023 03:08:33 GMT  
		Size: 15.7 MB (15746563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f7beb564cd4e17ac6f0066d8923c3e1a33cf5131542c873cd289e83bc2f98d`  
		Last Modified: Tue, 13 Jun 2023 18:32:50 GMT  
		Size: 18.6 MB (18598375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73606481ffac7e00171316db43e6998cf7b12ad1484bf62c4f7da607957b601`  
		Last Modified: Tue, 13 Jun 2023 18:32:47 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b386b6ac686ceffe9ef1031e6d8cf8f8a986aa3abf49d85a719e50199947e7c5`  
		Last Modified: Tue, 13 Jun 2023 18:33:21 GMT  
		Size: 48.7 MB (48731199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aaad56bf2200970306cd3a79d4a12bcd89d2b50edcf2f1ca2e761c800c2425`  
		Last Modified: Tue, 13 Jun 2023 18:33:16 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
