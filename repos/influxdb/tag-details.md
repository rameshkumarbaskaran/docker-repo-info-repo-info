<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.8`](#influxdb18)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8-data`](#influxdb18-data)
-	[`influxdb:1.8-data-alpine`](#influxdb18-data-alpine)
-	[`influxdb:1.8-meta`](#influxdb18-meta)
-	[`influxdb:1.8-meta-alpine`](#influxdb18-meta-alpine)
-	[`influxdb:1.8.10`](#influxdb1810)
-	[`influxdb:1.8.10-alpine`](#influxdb1810-alpine)
-	[`influxdb:1.8.10-data`](#influxdb1810-data)
-	[`influxdb:1.8.10-data-alpine`](#influxdb1810-data-alpine)
-	[`influxdb:1.8.10-meta`](#influxdb1810-meta)
-	[`influxdb:1.8.10-meta-alpine`](#influxdb1810-meta-alpine)
-	[`influxdb:1.9-data`](#influxdb19-data)
-	[`influxdb:1.9-data-alpine`](#influxdb19-data-alpine)
-	[`influxdb:1.9-meta`](#influxdb19-meta)
-	[`influxdb:1.9-meta-alpine`](#influxdb19-meta-alpine)
-	[`influxdb:1.9.6-data`](#influxdb196-data)
-	[`influxdb:1.9.6-data-alpine`](#influxdb196-data-alpine)
-	[`influxdb:1.9.6-meta`](#influxdb196-meta)
-	[`influxdb:1.9.6-meta-alpine`](#influxdb196-meta-alpine)
-	[`influxdb:2.0`](#influxdb20)
-	[`influxdb:2.0-alpine`](#influxdb20-alpine)
-	[`influxdb:2.0.9`](#influxdb209)
-	[`influxdb:2.0.9-alpine`](#influxdb209-alpine)
-	[`influxdb:2.1`](#influxdb21)
-	[`influxdb:2.1-alpine`](#influxdb21-alpine)
-	[`influxdb:2.1.1`](#influxdb211)
-	[`influxdb:2.1.1-alpine`](#influxdb211-alpine)
-	[`influxdb:2.2`](#influxdb22)
-	[`influxdb:2.2-alpine`](#influxdb22-alpine)
-	[`influxdb:2.2.0`](#influxdb220)
-	[`influxdb:2.2.0-alpine`](#influxdb220-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:4d8267af494f3f6f0d42cc0d096e190a411e9762566fe525a1a37adc38a9c152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:4dc8aa1263b63b14b4e2fa4e692e7127ce0a9e43924405b4bdbbc311bb4118ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115967376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9eb7b5252d2a347b3993df10fe3a458bf0a0398d002eb3bf63e0273fbfddc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:07 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 30 Mar 2022 23:05:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:13 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca272d9f078b66187b887ca31b8ca4afa85dfdd1750b13ef1b5bf599499c5d9`  
		Last Modified: Wed, 30 Mar 2022 23:08:18 GMT  
		Size: 54.9 MB (54890147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2740ef6abdea6a96813cfb0092535131c034ff3d6cbb1092ebe16a3b155f2672`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a5ae9b77009c830ef5631cb3b5794ff6322d5c6b7fca8a470efcd5fad250f9`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc28277163b44cf773f9c177ede9f406f7798b6ff10fcceb4cbdd00613c213a`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:37f1cff2c43364a8fada0207d62ee0bba55973d422bdabe58f1f80e97bbab5e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107651914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d591fb195b9b951453546a6b8076f665f118696df090f4d192f3747fd75c56fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 02:23:57 GMT
ADD file:3dc1697adfcf63a288e9ec7a2c40438b8ba2ccfff0382a1ed5457f30d7a37f76 in / 
# Tue, 29 Mar 2022 02:23:57 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 20:17:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 20:17:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 31 Mar 2022 23:48:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 31 Mar 2022 23:48:46 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 31 Mar 2022 23:48:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 31 Mar 2022 23:48:59 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 31 Mar 2022 23:48:59 GMT
EXPOSE 8086
# Thu, 31 Mar 2022 23:48:59 GMT
VOLUME [/var/lib/influxdb]
# Thu, 31 Mar 2022 23:49:00 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 31 Mar 2022 23:49:00 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 31 Mar 2022 23:49:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 31 Mar 2022 23:49:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:aecfa9e0b0179abf68bebbcfc35453928546e01ad1c8b6eaadf759360762dada`  
		Last Modified: Tue, 29 Mar 2022 02:40:33 GMT  
		Size: 42.2 MB (42151158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc36fcf6b269b843685f3e40183609c9ee393c766145d636666727cc97069e`  
		Last Modified: Wed, 30 Mar 2022 21:38:43 GMT  
		Size: 10.0 MB (9956889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e13cc08b3e8cd7b26260c7597b624d4a45ebc2afb89bb5da193fc824ab69e55`  
		Last Modified: Wed, 30 Mar 2022 21:38:39 GMT  
		Size: 3.9 MB (3921802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df41c11d71480e163f8ecfb236ed0d70624d226f05bcc6b9871eb8b05e3fcec`  
		Last Modified: Thu, 31 Mar 2022 23:49:31 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058bee89d6bf605dcff8878b929903e17567627ffff27d1b6eac278ab298129a`  
		Last Modified: Thu, 31 Mar 2022 23:50:42 GMT  
		Size: 51.6 MB (51617493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6819f22e70f5af138b036289895bcdb1f357a0853e612cfd28aa71cdef6389`  
		Last Modified: Thu, 31 Mar 2022 23:50:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e69d7cdaec10d313916f9bf91d85efb8f48f1dc87b9bcad03d04dd25a70a73`  
		Last Modified: Thu, 31 Mar 2022 23:50:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdbb22118f433d2dc3b0b242a5c543d3cade8cbe73bb14b0e2c31c46199ea48`  
		Last Modified: Thu, 31 Mar 2022 23:50:13 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:578963c45259268acb301239a3a3679806fad07c65dd91d8e2d164e9287977aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108544173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbc97103507192438f04f90864fd11c5e3ce05489afa1499826c40c1610b7c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:21 GMT
ADD file:cfa91852b5b893603b656848cb1329c06041fea5cfef841978456c7266e6ac11 in / 
# Tue, 29 Mar 2022 00:45:22 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:18:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:21:25 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 30 Mar 2022 23:21:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:21:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:21:32 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:21:33 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:21:35 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:21:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:21:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0b62b1ed6f218f82ac797884bd7a8c5dcdcdd8d003f3946678c53900cc537d7b`  
		Last Modified: Tue, 29 Mar 2022 00:53:52 GMT  
		Size: 43.2 MB (43212837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e309f576f536ef1eb431f346fb1a09b23c355e6ec7657db9b1b5d59d58c839`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 10.2 MB (10217976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91984a52400cf1b768b1f46910222bcf8cb584650c23a648535dab2f65b3ef9`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 3.9 MB (3874485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5e9af97a9e4a8158f582fd42b5462fe38123e2b8259780646271ccb9b37805`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40959cbe31a72fcd483ea95f1fe359da1f38d3bf7dddfed89189c6db7fd725dc`  
		Last Modified: Wed, 30 Mar 2022 23:23:42 GMT  
		Size: 51.2 MB (51234333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9046408609c0e444fb18f8431d85bb7e297e3a30a1641ac91c1d82f74e105`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62b2947a2cb7cb742e6a5ff31431072f7ce1f1710ca12e4e51615c604cf797c`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6d029ae6b6f2c7d9ebbe7df6c12f7870c915a71096fb42671d734cc03fe061`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:9b54e97bda0ad56d352d7b0f30f0838a7804786af3dcf9902f2facb20cdc8c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:da9e53019e9e915278d9b6a199a64cc8486e13528411101f75385bb7f2e709a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58955359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33508e3d62d57b814452b7f7b3c08050f7fbd3890283f8078e4a6979ca58299`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:03:30 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 05 Apr 2022 10:03:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 10:03:38 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 05 Apr 2022 10:03:38 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 10:03:38 GMT
VOLUME [/var/lib/influxdb]
# Tue, 05 Apr 2022 10:03:38 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 05 Apr 2022 10:03:38 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 05 Apr 2022 10:03:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:03:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c92e0e1b5e3133d942ce0fc2b295ac44f364c5d1d17b60fd452b00d16327c6`  
		Last Modified: Tue, 05 Apr 2022 10:07:22 GMT  
		Size: 54.7 MB (54659608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694e17e1c591b62f9b5418e23aba661b8e50ca089d198a5324be12c4fb3cc771`  
		Last Modified: Tue, 05 Apr 2022 10:07:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d046f1f7638fc6b5b400ed626934ab027a265996965cf13474e1dc8d21bde4b4`  
		Last Modified: Tue, 05 Apr 2022 10:07:14 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862c4c27d4c5aea4da583ac392bed4175d995bbacbd71ecc116d6b77d44a1aa3`  
		Last Modified: Tue, 05 Apr 2022 10:07:15 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:be2d5a7bd5ff0644383defcce1f7769ae89363d5867ac5b2615ae2731dcb6c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:0790872efd83e02d8fdd2faf7a2ff410f9ff50a007b58c517d14c783d48130d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117786452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276cebfb7edd0645264657425ddb00bb2bcb80b7dce64169b9281067ebc0707c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:25 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edcfcb7a5161abd03b61b6153c6f903029bcfb2d9efa4a6556918c51a064af1`  
		Last Modified: Wed, 30 Mar 2022 23:08:36 GMT  
		Size: 56.7 MB (56709163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97289aef350957936b3a19d68c846a790247f957e99f5d9f0e9c628bc74e2d0f`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1caefc2f0645fadbdce8da95cfbe3bdf21d1712e3d4b95577a26a55d97debc`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fc4496b0657c51da18c2c520e35381f811fe8d8a7eb3c3f4b15209a3b00900`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:5b6f51f9283101e2260d04e4ec6e97e6ac6b42906de0330d245556207485ff9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ffe5860e830f75f1ecc06f6d9ef5131783a4009bf8c178a202b221b7090991d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60799475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51bbfae48c946a370eace3f872988f7daf93c3ee3586f383c6165ed132c4760`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:03:43 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Thu, 07 Apr 2022 22:22:53 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:22:54 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 07 Apr 2022 22:22:54 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:22:54 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:22:54 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:22:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 07 Apr 2022 22:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:22:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d253e65fc0c40504c5ab7ed8891c7535ce694e62e9b315612518257a49a27e`  
		Last Modified: Thu, 07 Apr 2022 22:24:53 GMT  
		Size: 56.5 MB (56503671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c14b9a988386b736ef6a259676adf189b9aee692453b5a41173a23bd2aed93e`  
		Last Modified: Thu, 07 Apr 2022 22:24:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1e32c4578db25e99bb2f5fbd9bae12550160681dd612559a2fdb24774b6636`  
		Last Modified: Thu, 07 Apr 2022 22:24:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3641a605f831a5d23969cb82df4b923d91d0377459df0169f7c92d5a15449a9`  
		Last Modified: Thu, 07 Apr 2022 22:24:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:4727e7c393e16502a487921e0fcae07eaaf9e00ecf3b22b37562e86d6867188b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c50786838735ef2c78c51e7238a4404520063b935751ce517157749b2904aa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84493011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0e1d0ea12729ab4474843f41d7a88f5a1870ec065e3fe58185c6b0098c0ce1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:32 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:32 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:32 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:32 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:33 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:33 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c487c418525e877d8128d62ac4dc164cba44ce112d1bc88171390368ce61ad53`  
		Last Modified: Wed, 30 Mar 2022 23:08:52 GMT  
		Size: 23.4 MB (23416930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720a75a54e3c5d1a6d4ca4261fc76d135e3e9c04b6804de3b56615706c8fdf17`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feee196124cbe471a1e4ff40944ed9de1949b39f539001874ba0f125d28314d5`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:008db7d140fce00d44cb0f11b4e04a8d5c151222c18e20f1a6e3c40432c1b6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:06b3c6c7fdaaae61c386be3b2db8debdb79dc029c86b28fb2ddd57b7a813cca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27587601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c59c3a9d5137ca189bf5be3e9b530b46a594f7e9911d79fb7ce49a68802cbdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:03:43 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Thu, 07 Apr 2022 22:23:04 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:23:04 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 07 Apr 2022 22:23:04 GMT
EXPOSE 8091
# Thu, 07 Apr 2022 22:23:04 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:23:05 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:05 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef0611ecd34d60d54d119ad0d5b217bf9bb505143a9a76d79a71588306f6962`  
		Last Modified: Thu, 07 Apr 2022 22:25:10 GMT  
		Size: 23.3 MB (23292997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03800bc1786c31a63f2ce29355aa6c75587b563883515d7db2faec592fe0bcc5`  
		Last Modified: Thu, 07 Apr 2022 22:25:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56614b1a615f4516c69895cb7e68ac004819d3dd52ffe4766c55c5686847eff`  
		Last Modified: Thu, 07 Apr 2022 22:25:07 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:4d8267af494f3f6f0d42cc0d096e190a411e9762566fe525a1a37adc38a9c152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.10` - linux; amd64

```console
$ docker pull influxdb@sha256:4dc8aa1263b63b14b4e2fa4e692e7127ce0a9e43924405b4bdbbc311bb4118ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115967376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9eb7b5252d2a347b3993df10fe3a458bf0a0398d002eb3bf63e0273fbfddc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:07 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 30 Mar 2022 23:05:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:13 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca272d9f078b66187b887ca31b8ca4afa85dfdd1750b13ef1b5bf599499c5d9`  
		Last Modified: Wed, 30 Mar 2022 23:08:18 GMT  
		Size: 54.9 MB (54890147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2740ef6abdea6a96813cfb0092535131c034ff3d6cbb1092ebe16a3b155f2672`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a5ae9b77009c830ef5631cb3b5794ff6322d5c6b7fca8a470efcd5fad250f9`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc28277163b44cf773f9c177ede9f406f7798b6ff10fcceb4cbdd00613c213a`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:37f1cff2c43364a8fada0207d62ee0bba55973d422bdabe58f1f80e97bbab5e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107651914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d591fb195b9b951453546a6b8076f665f118696df090f4d192f3747fd75c56fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 02:23:57 GMT
ADD file:3dc1697adfcf63a288e9ec7a2c40438b8ba2ccfff0382a1ed5457f30d7a37f76 in / 
# Tue, 29 Mar 2022 02:23:57 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 20:17:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 20:17:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 31 Mar 2022 23:48:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 31 Mar 2022 23:48:46 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 31 Mar 2022 23:48:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 31 Mar 2022 23:48:59 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 31 Mar 2022 23:48:59 GMT
EXPOSE 8086
# Thu, 31 Mar 2022 23:48:59 GMT
VOLUME [/var/lib/influxdb]
# Thu, 31 Mar 2022 23:49:00 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 31 Mar 2022 23:49:00 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 31 Mar 2022 23:49:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 31 Mar 2022 23:49:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:aecfa9e0b0179abf68bebbcfc35453928546e01ad1c8b6eaadf759360762dada`  
		Last Modified: Tue, 29 Mar 2022 02:40:33 GMT  
		Size: 42.2 MB (42151158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc36fcf6b269b843685f3e40183609c9ee393c766145d636666727cc97069e`  
		Last Modified: Wed, 30 Mar 2022 21:38:43 GMT  
		Size: 10.0 MB (9956889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e13cc08b3e8cd7b26260c7597b624d4a45ebc2afb89bb5da193fc824ab69e55`  
		Last Modified: Wed, 30 Mar 2022 21:38:39 GMT  
		Size: 3.9 MB (3921802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df41c11d71480e163f8ecfb236ed0d70624d226f05bcc6b9871eb8b05e3fcec`  
		Last Modified: Thu, 31 Mar 2022 23:49:31 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058bee89d6bf605dcff8878b929903e17567627ffff27d1b6eac278ab298129a`  
		Last Modified: Thu, 31 Mar 2022 23:50:42 GMT  
		Size: 51.6 MB (51617493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6819f22e70f5af138b036289895bcdb1f357a0853e612cfd28aa71cdef6389`  
		Last Modified: Thu, 31 Mar 2022 23:50:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e69d7cdaec10d313916f9bf91d85efb8f48f1dc87b9bcad03d04dd25a70a73`  
		Last Modified: Thu, 31 Mar 2022 23:50:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdbb22118f433d2dc3b0b242a5c543d3cade8cbe73bb14b0e2c31c46199ea48`  
		Last Modified: Thu, 31 Mar 2022 23:50:13 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:578963c45259268acb301239a3a3679806fad07c65dd91d8e2d164e9287977aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108544173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbc97103507192438f04f90864fd11c5e3ce05489afa1499826c40c1610b7c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:21 GMT
ADD file:cfa91852b5b893603b656848cb1329c06041fea5cfef841978456c7266e6ac11 in / 
# Tue, 29 Mar 2022 00:45:22 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:18:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:21:25 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 30 Mar 2022 23:21:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:21:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:21:32 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:21:33 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:21:35 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:21:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:21:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0b62b1ed6f218f82ac797884bd7a8c5dcdcdd8d003f3946678c53900cc537d7b`  
		Last Modified: Tue, 29 Mar 2022 00:53:52 GMT  
		Size: 43.2 MB (43212837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e309f576f536ef1eb431f346fb1a09b23c355e6ec7657db9b1b5d59d58c839`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 10.2 MB (10217976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91984a52400cf1b768b1f46910222bcf8cb584650c23a648535dab2f65b3ef9`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 3.9 MB (3874485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5e9af97a9e4a8158f582fd42b5462fe38123e2b8259780646271ccb9b37805`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40959cbe31a72fcd483ea95f1fe359da1f38d3bf7dddfed89189c6db7fd725dc`  
		Last Modified: Wed, 30 Mar 2022 23:23:42 GMT  
		Size: 51.2 MB (51234333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9046408609c0e444fb18f8431d85bb7e297e3a30a1641ac91c1d82f74e105`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62b2947a2cb7cb742e6a5ff31431072f7ce1f1710ca12e4e51615c604cf797c`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6d029ae6b6f2c7d9ebbe7df6c12f7870c915a71096fb42671d734cc03fe061`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:9b54e97bda0ad56d352d7b0f30f0838a7804786af3dcf9902f2facb20cdc8c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:da9e53019e9e915278d9b6a199a64cc8486e13528411101f75385bb7f2e709a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58955359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33508e3d62d57b814452b7f7b3c08050f7fbd3890283f8078e4a6979ca58299`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:03:30 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 05 Apr 2022 10:03:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 10:03:38 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 05 Apr 2022 10:03:38 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 10:03:38 GMT
VOLUME [/var/lib/influxdb]
# Tue, 05 Apr 2022 10:03:38 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 05 Apr 2022 10:03:38 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 05 Apr 2022 10:03:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:03:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c92e0e1b5e3133d942ce0fc2b295ac44f364c5d1d17b60fd452b00d16327c6`  
		Last Modified: Tue, 05 Apr 2022 10:07:22 GMT  
		Size: 54.7 MB (54659608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694e17e1c591b62f9b5418e23aba661b8e50ca089d198a5324be12c4fb3cc771`  
		Last Modified: Tue, 05 Apr 2022 10:07:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d046f1f7638fc6b5b400ed626934ab027a265996965cf13474e1dc8d21bde4b4`  
		Last Modified: Tue, 05 Apr 2022 10:07:14 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862c4c27d4c5aea4da583ac392bed4175d995bbacbd71ecc116d6b77d44a1aa3`  
		Last Modified: Tue, 05 Apr 2022 10:07:15 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-data`

```console
$ docker pull influxdb@sha256:be2d5a7bd5ff0644383defcce1f7769ae89363d5867ac5b2615ae2731dcb6c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:0790872efd83e02d8fdd2faf7a2ff410f9ff50a007b58c517d14c783d48130d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117786452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276cebfb7edd0645264657425ddb00bb2bcb80b7dce64169b9281067ebc0707c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:25 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edcfcb7a5161abd03b61b6153c6f903029bcfb2d9efa4a6556918c51a064af1`  
		Last Modified: Wed, 30 Mar 2022 23:08:36 GMT  
		Size: 56.7 MB (56709163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97289aef350957936b3a19d68c846a790247f957e99f5d9f0e9c628bc74e2d0f`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1caefc2f0645fadbdce8da95cfbe3bdf21d1712e3d4b95577a26a55d97debc`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fc4496b0657c51da18c2c520e35381f811fe8d8a7eb3c3f4b15209a3b00900`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-data-alpine`

```console
$ docker pull influxdb@sha256:5b6f51f9283101e2260d04e4ec6e97e6ac6b42906de0330d245556207485ff9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ffe5860e830f75f1ecc06f6d9ef5131783a4009bf8c178a202b221b7090991d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60799475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51bbfae48c946a370eace3f872988f7daf93c3ee3586f383c6165ed132c4760`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:03:43 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Thu, 07 Apr 2022 22:22:53 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:22:54 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 07 Apr 2022 22:22:54 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:22:54 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:22:54 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:22:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 07 Apr 2022 22:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:22:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d253e65fc0c40504c5ab7ed8891c7535ce694e62e9b315612518257a49a27e`  
		Last Modified: Thu, 07 Apr 2022 22:24:53 GMT  
		Size: 56.5 MB (56503671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c14b9a988386b736ef6a259676adf189b9aee692453b5a41173a23bd2aed93e`  
		Last Modified: Thu, 07 Apr 2022 22:24:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1e32c4578db25e99bb2f5fbd9bae12550160681dd612559a2fdb24774b6636`  
		Last Modified: Thu, 07 Apr 2022 22:24:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3641a605f831a5d23969cb82df4b923d91d0377459df0169f7c92d5a15449a9`  
		Last Modified: Thu, 07 Apr 2022 22:24:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-meta`

```console
$ docker pull influxdb@sha256:4727e7c393e16502a487921e0fcae07eaaf9e00ecf3b22b37562e86d6867188b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c50786838735ef2c78c51e7238a4404520063b935751ce517157749b2904aa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84493011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0e1d0ea12729ab4474843f41d7a88f5a1870ec065e3fe58185c6b0098c0ce1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:32 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:32 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:32 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:32 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:33 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:33 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c487c418525e877d8128d62ac4dc164cba44ce112d1bc88171390368ce61ad53`  
		Last Modified: Wed, 30 Mar 2022 23:08:52 GMT  
		Size: 23.4 MB (23416930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720a75a54e3c5d1a6d4ca4261fc76d135e3e9c04b6804de3b56615706c8fdf17`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feee196124cbe471a1e4ff40944ed9de1949b39f539001874ba0f125d28314d5`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-meta-alpine`

```console
$ docker pull influxdb@sha256:008db7d140fce00d44cb0f11b4e04a8d5c151222c18e20f1a6e3c40432c1b6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:06b3c6c7fdaaae61c386be3b2db8debdb79dc029c86b28fb2ddd57b7a813cca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27587601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c59c3a9d5137ca189bf5be3e9b530b46a594f7e9911d79fb7ce49a68802cbdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:03:43 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Thu, 07 Apr 2022 22:23:04 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:23:04 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 07 Apr 2022 22:23:04 GMT
EXPOSE 8091
# Thu, 07 Apr 2022 22:23:04 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:23:05 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:05 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef0611ecd34d60d54d119ad0d5b217bf9bb505143a9a76d79a71588306f6962`  
		Last Modified: Thu, 07 Apr 2022 22:25:10 GMT  
		Size: 23.3 MB (23292997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03800bc1786c31a63f2ce29355aa6c75587b563883515d7db2faec592fe0bcc5`  
		Last Modified: Thu, 07 Apr 2022 22:25:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56614b1a615f4516c69895cb7e68ac004819d3dd52ffe4766c55c5686847eff`  
		Last Modified: Thu, 07 Apr 2022 22:25:07 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:56b57de30ed18a3c48edf6b410685fe67808c5c1d892581146a69bd0dc145169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:6db64a003dd0be8e2fa3da8a8e79dcac9bc9c9f58213a6573085eca106b815c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88681465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0baf120185e11fa5d2e9cdcc89c96e5e56c90fb0724a96d3520b24b970e091`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:37 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Wed, 30 Mar 2022 23:05:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:41 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:42 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:42 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:42 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8f4a3d69c0c22b0e3d9e7e16969bf31ec608f5e24ef4978686b771811323e8`  
		Last Modified: Wed, 30 Mar 2022 23:09:10 GMT  
		Size: 27.6 MB (27604178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782474e6ac637e1f5dda88d1471243b88c53b7a3e7da56d72c38c0b9033c0a8`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204739d56240853dfc71df7d11f0c188c2274e7fac0c4751483c66ef50b3733c`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692811b49ad9c8a8b3bfc755a24b5417049e41abb78cb11ae5dd7793fbec7488`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:d8934ee0edc69812dae63ed9b474eb91d650ca8c460605bbc305dbc18c3cb014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fcdb1822869fea2ae4d731fd9ef53bc6b7cc591649a0c19870c5dc331e725798
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31863241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba23542f7a038ace18c55398d146c9e474a0c1d4580ddc36feded2f14f6de3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:06 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Thu, 07 Apr 2022 22:23:13 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:23:14 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 07 Apr 2022 22:23:14 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:23:14 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:23:14 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:14 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 07 Apr 2022 22:23:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87330db054b158b6242dfa37ac1734394b53b4002531d619c69195fce53b880`  
		Last Modified: Thu, 07 Apr 2022 22:25:28 GMT  
		Size: 27.6 MB (27567431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0962416aa49614e3fd3d50a91a0f47e80edc2c068c8eefbbf4c022fe80a421e6`  
		Last Modified: Thu, 07 Apr 2022 22:25:24 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05404d71bfd40d3e7c7a785d85c9a0509d3ee10afb4988c70509113fd2cc8d`  
		Last Modified: Thu, 07 Apr 2022 22:25:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484b99a22ff9292d8539523a502634a0bbcebbba545ee57d04fc649d8a30620b`  
		Last Modified: Thu, 07 Apr 2022 22:25:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:eac0abfaed7a464f600047316adad3ee4c125165df3673fcbd0becb8530aab04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:535fc0aea9cf89ee24662a1b14b4734ca83a3b7d7fd5dfce34cee5e246a1289b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71515678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e8d639defc213c82c7aed0f2a72075d27885be90321bc4279575c49d2a9cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:37 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Wed, 30 Mar 2022 23:05:49 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:49 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:50 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a5ef3432923cab0a78b3334a4e681c9607f4d2034b9e92bae5a6867a6f0e2e`  
		Last Modified: Wed, 30 Mar 2022 23:09:23 GMT  
		Size: 10.4 MB (10439599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5771b52e55eed00db367d41862776a7f7ddb2ad8720e7243fd3112547bcd3ad`  
		Last Modified: Wed, 30 Mar 2022 23:09:21 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa824f3a6a3f28dbcc27ae20c996bd6f260bcce0b366d3a511e43e37560e884`  
		Last Modified: Wed, 30 Mar 2022 23:09:21 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:742a51db8dfe569adb49a69071c44ddf0f373199e5b78d0a50e3839e63b8a5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:559b89f7cb3304fe14660e80ca1af6001cde71e0c3f5b7ce787f326e5b4cbd1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14704251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a8cb4fbadc797b3409e60f86e0bebe475b9d724cd15f658d8211d794fe4b83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:06 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Thu, 07 Apr 2022 22:23:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:23:26 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 07 Apr 2022 22:23:27 GMT
EXPOSE 8091
# Thu, 07 Apr 2022 22:23:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:23:27 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:27 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f70b29b3caa461ee689124f3e52d1f96938ee16f711df91186f9de029f5b8d`  
		Last Modified: Thu, 07 Apr 2022 22:25:41 GMT  
		Size: 10.4 MB (10409651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db52da89842c67d69448b5f7a6c22170c52e7d6924782d73f71670cd9507143`  
		Last Modified: Thu, 07 Apr 2022 22:25:39 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc8508a3dc50232978c669e0a0e78a4d23b4a2b0310542757c506d69b7938d2`  
		Last Modified: Thu, 07 Apr 2022 22:25:39 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.6-data`

```console
$ docker pull influxdb@sha256:56b57de30ed18a3c48edf6b410685fe67808c5c1d892581146a69bd0dc145169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:6db64a003dd0be8e2fa3da8a8e79dcac9bc9c9f58213a6573085eca106b815c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88681465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0baf120185e11fa5d2e9cdcc89c96e5e56c90fb0724a96d3520b24b970e091`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:37 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Wed, 30 Mar 2022 23:05:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:41 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:42 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:42 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:42 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8f4a3d69c0c22b0e3d9e7e16969bf31ec608f5e24ef4978686b771811323e8`  
		Last Modified: Wed, 30 Mar 2022 23:09:10 GMT  
		Size: 27.6 MB (27604178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782474e6ac637e1f5dda88d1471243b88c53b7a3e7da56d72c38c0b9033c0a8`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204739d56240853dfc71df7d11f0c188c2274e7fac0c4751483c66ef50b3733c`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692811b49ad9c8a8b3bfc755a24b5417049e41abb78cb11ae5dd7793fbec7488`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.6-data-alpine`

```console
$ docker pull influxdb@sha256:d8934ee0edc69812dae63ed9b474eb91d650ca8c460605bbc305dbc18c3cb014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.6-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fcdb1822869fea2ae4d731fd9ef53bc6b7cc591649a0c19870c5dc331e725798
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31863241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba23542f7a038ace18c55398d146c9e474a0c1d4580ddc36feded2f14f6de3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:06 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Thu, 07 Apr 2022 22:23:13 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:23:14 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 07 Apr 2022 22:23:14 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:23:14 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:23:14 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:14 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 07 Apr 2022 22:23:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87330db054b158b6242dfa37ac1734394b53b4002531d619c69195fce53b880`  
		Last Modified: Thu, 07 Apr 2022 22:25:28 GMT  
		Size: 27.6 MB (27567431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0962416aa49614e3fd3d50a91a0f47e80edc2c068c8eefbbf4c022fe80a421e6`  
		Last Modified: Thu, 07 Apr 2022 22:25:24 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05404d71bfd40d3e7c7a785d85c9a0509d3ee10afb4988c70509113fd2cc8d`  
		Last Modified: Thu, 07 Apr 2022 22:25:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484b99a22ff9292d8539523a502634a0bbcebbba545ee57d04fc649d8a30620b`  
		Last Modified: Thu, 07 Apr 2022 22:25:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.6-meta`

```console
$ docker pull influxdb@sha256:eac0abfaed7a464f600047316adad3ee4c125165df3673fcbd0becb8530aab04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:535fc0aea9cf89ee24662a1b14b4734ca83a3b7d7fd5dfce34cee5e246a1289b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71515678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e8d639defc213c82c7aed0f2a72075d27885be90321bc4279575c49d2a9cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:37 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Wed, 30 Mar 2022 23:05:49 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:49 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:50 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a5ef3432923cab0a78b3334a4e681c9607f4d2034b9e92bae5a6867a6f0e2e`  
		Last Modified: Wed, 30 Mar 2022 23:09:23 GMT  
		Size: 10.4 MB (10439599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5771b52e55eed00db367d41862776a7f7ddb2ad8720e7243fd3112547bcd3ad`  
		Last Modified: Wed, 30 Mar 2022 23:09:21 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa824f3a6a3f28dbcc27ae20c996bd6f260bcce0b366d3a511e43e37560e884`  
		Last Modified: Wed, 30 Mar 2022 23:09:21 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.6-meta-alpine`

```console
$ docker pull influxdb@sha256:742a51db8dfe569adb49a69071c44ddf0f373199e5b78d0a50e3839e63b8a5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.6-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:559b89f7cb3304fe14660e80ca1af6001cde71e0c3f5b7ce787f326e5b4cbd1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14704251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a8cb4fbadc797b3409e60f86e0bebe475b9d724cd15f658d8211d794fe4b83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:06 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Thu, 07 Apr 2022 22:23:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:23:26 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 07 Apr 2022 22:23:27 GMT
EXPOSE 8091
# Thu, 07 Apr 2022 22:23:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:23:27 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:27 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f70b29b3caa461ee689124f3e52d1f96938ee16f711df91186f9de029f5b8d`  
		Last Modified: Thu, 07 Apr 2022 22:25:41 GMT  
		Size: 10.4 MB (10409651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db52da89842c67d69448b5f7a6c22170c52e7d6924782d73f71670cd9507143`  
		Last Modified: Thu, 07 Apr 2022 22:25:39 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc8508a3dc50232978c669e0a0e78a4d23b4a2b0310542757c506d69b7938d2`  
		Last Modified: Thu, 07 Apr 2022 22:25:39 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0`

```console
$ docker pull influxdb@sha256:3199b22c3d83d478287411931aec7582a6965fc9d73e171e6b273bc0ac394a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0` - linux; amd64

```console
$ docker pull influxdb@sha256:a5c915c7a450dd496002b7d37e6dd1a05dedbe62fbc861bdc0e6c26d75053e92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172350398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cb9a90c58041fa6402d6be3beaf1be8486a435afa98c1a31e447ed7c4c1c57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:05:58 GMT
ENV INFLUXDB_VERSION=2.0.9
# Wed, 30 Mar 2022 23:06:06 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 30 Mar 2022 23:06:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:06:07 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:06:07 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:06:07 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Wed, 30 Mar 2022 23:06:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:06:08 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:06:08 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:06:08 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba69ef51e285543b380c5080feb794e437d77b322bf5406d02a4c18275fbd65d`  
		Last Modified: Wed, 30 Mar 2022 23:09:41 GMT  
		Size: 103.1 MB (103090642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbfa930edbd4fc7d357c7a01e6bfb508f894cc4470d44fa4a2ec16c9106dc6`  
		Last Modified: Wed, 30 Mar 2022 23:09:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1607d0a086cd9cd79754f90b38c8b1b2178f8b1e55eda9792a6579668c62ec44`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e797924e061d7121c18647921bb3060c5cda9ddbfc761fc1ce35ca9e635c7f1`  
		Last Modified: Wed, 30 Mar 2022 23:09:32 GMT  
		Size: 4.9 KB (4945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:73273667c46d64d6f0f20e1b406ec9f8bf6fd26339596502cb521a4159a427e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174143023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c81bb401efe03a2c2c07755d5ce66854d5abbae522398facc17cf93eaf7e1fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:21:48 GMT
ENV INFLUXDB_VERSION=2.0.9
# Wed, 30 Mar 2022 23:21:56 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 30 Mar 2022 23:21:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:21:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:22:00 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:22:01 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Wed, 30 Mar 2022 23:22:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:22:02 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:22:03 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:22:04 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:22:05 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:22:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:22:07 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8eee3bbcc2a05e10b509b77092c4fab995de116ba9ee1c668d259a60c89c4`  
		Last Modified: Wed, 30 Mar 2022 23:24:04 GMT  
		Size: 106.5 MB (106526968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993776c3f37c52edc4f5c89071e074e1a78766f272870f599922677f8c2abe`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc91e1f3f901d572ac0b49d1ce356d88cf33d04792aa68bfd5474b4bca602e2f`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51fbe92bcf55b7ddb8c97ba90bd7b75ba1fecb276b3a637cf8156bba81c6b29`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0-alpine`

```console
$ docker pull influxdb@sha256:28b27ba51abbddb2113c728b9fb5e23261733a9bceb995402012e69aa34273d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e0e9f4602a6cc0632ea1dbc8910759c86b61ece94f6d5894382d6f1b9bcc30e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116713298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac89ea59315d99dec3c08bb1723cf2fbf03c2e11b2705cbc281417dbafc9c37e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:04:28 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:29 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 10:04:29 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 10:04:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 10:04:32 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 05 Apr 2022 10:04:44 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 05 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Apr 2022 10:04:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Apr 2022 10:04:45 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Apr 2022 10:04:45 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Tue, 05 Apr 2022 10:04:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:04:45 GMT
CMD ["influxd"]
# Tue, 05 Apr 2022 10:04:45 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 10:04:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Apr 2022 10:04:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Apr 2022 10:04:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Apr 2022 10:04:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824989658cee0fcd8b3e27d03a0b79d4ae37c3b765afaff6f49d076d0d9dc42`  
		Last Modified: Tue, 05 Apr 2022 10:08:40 GMT  
		Size: 9.8 MB (9836774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fbe7d281a77910553db440ca9d0c4b709850e35385fc474a9b9b11e55db697`  
		Last Modified: Tue, 05 Apr 2022 10:08:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288cce5ed27daa2927f6bc96c87e2581197832a7210cf5813f6d6cfea28afb7e`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 960.6 KB (960617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bae8b0ec17a5d9dbf1eb7e1e3953baef4edaf26b616fcbc218d817636d79d8`  
		Last Modified: Tue, 05 Apr 2022 10:08:45 GMT  
		Size: 103.1 MB (103090641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8f2b193010cbe745a05d4a2907ef5592bcfc3fcf2f8dc3effc77b3db59171`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485640ccb69c912529e7b70604b5ab52e45aaf7fc93bbca67c021628d1f9d141`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6553ced84695f9c93dba30575941508f22f23786270f7612e99ebd6045d0ff5c`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 4.9 KB (4942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3047f61d3f0deb8b68f3bb32f77ad1da4dc3f935344d6b4978e2b32978569b5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119819824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6df860f31be0a1452ff106725cb2865b8792e1cbca0eac815cee16c231129b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:11:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:11:29 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 04:11:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 04:11:31 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 04:11:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 04:11:35 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 05 Apr 2022 04:11:48 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 05 Apr 2022 04:11:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Apr 2022 04:11:49 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Apr 2022 04:11:51 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Apr 2022 04:11:52 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Tue, 05 Apr 2022 04:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:11:53 GMT
CMD ["influxd"]
# Tue, 05 Apr 2022 04:11:54 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 04:11:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Apr 2022 04:11:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Apr 2022 04:11:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Apr 2022 04:11:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a37e642510b42e25dbe3082e57f33cdcdb65bad4e9468cd5c76fdb5015c7a`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc96d3454b87ca3f120022077fc7d0ff9477f1b5d1c99519902ae6eed0d7b90`  
		Last Modified: Tue, 05 Apr 2022 04:13:16 GMT  
		Size: 9.7 MB (9672606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6c62b5230b53a6e53da9a15c422cfb18b955afc941e7b68331dd84392405c`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a900a68fae805f39a9a8461f2ef4778a30b18c30f3bc6b2b85e0e02a107e4`  
		Last Modified: Tue, 05 Apr 2022 04:13:13 GMT  
		Size: 896.1 KB (896074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b07cab3429e5cb05ce350093f453086d575ea3fa8b8409fca4cabf4772f1b7`  
		Last Modified: Tue, 05 Apr 2022 04:13:23 GMT  
		Size: 106.5 MB (106526974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb98004947e4307dd97bd5347a40979529a3856593981fdf5be5939eddf45abe`  
		Last Modified: Tue, 05 Apr 2022 04:13:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a58f13a13141d9b8be4fdfd19c9bc68286c28872b5e103b27a68bf9af7b4ce`  
		Last Modified: Tue, 05 Apr 2022 04:13:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f057be72e1bceb8361f6e113dba8d132297ec659a68596020245db9a7db3d89`  
		Last Modified: Tue, 05 Apr 2022 04:13:13 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.9`

```console
$ docker pull influxdb@sha256:3199b22c3d83d478287411931aec7582a6965fc9d73e171e6b273bc0ac394a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.9` - linux; amd64

```console
$ docker pull influxdb@sha256:a5c915c7a450dd496002b7d37e6dd1a05dedbe62fbc861bdc0e6c26d75053e92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172350398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cb9a90c58041fa6402d6be3beaf1be8486a435afa98c1a31e447ed7c4c1c57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:05:58 GMT
ENV INFLUXDB_VERSION=2.0.9
# Wed, 30 Mar 2022 23:06:06 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 30 Mar 2022 23:06:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:06:07 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:06:07 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:06:07 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Wed, 30 Mar 2022 23:06:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:06:08 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:06:08 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:06:08 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba69ef51e285543b380c5080feb794e437d77b322bf5406d02a4c18275fbd65d`  
		Last Modified: Wed, 30 Mar 2022 23:09:41 GMT  
		Size: 103.1 MB (103090642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbfa930edbd4fc7d357c7a01e6bfb508f894cc4470d44fa4a2ec16c9106dc6`  
		Last Modified: Wed, 30 Mar 2022 23:09:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1607d0a086cd9cd79754f90b38c8b1b2178f8b1e55eda9792a6579668c62ec44`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e797924e061d7121c18647921bb3060c5cda9ddbfc761fc1ce35ca9e635c7f1`  
		Last Modified: Wed, 30 Mar 2022 23:09:32 GMT  
		Size: 4.9 KB (4945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.9` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:73273667c46d64d6f0f20e1b406ec9f8bf6fd26339596502cb521a4159a427e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174143023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c81bb401efe03a2c2c07755d5ce66854d5abbae522398facc17cf93eaf7e1fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:21:48 GMT
ENV INFLUXDB_VERSION=2.0.9
# Wed, 30 Mar 2022 23:21:56 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 30 Mar 2022 23:21:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:21:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:22:00 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:22:01 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Wed, 30 Mar 2022 23:22:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:22:02 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:22:03 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:22:04 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:22:05 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:22:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:22:07 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8eee3bbcc2a05e10b509b77092c4fab995de116ba9ee1c668d259a60c89c4`  
		Last Modified: Wed, 30 Mar 2022 23:24:04 GMT  
		Size: 106.5 MB (106526968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993776c3f37c52edc4f5c89071e074e1a78766f272870f599922677f8c2abe`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc91e1f3f901d572ac0b49d1ce356d88cf33d04792aa68bfd5474b4bca602e2f`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51fbe92bcf55b7ddb8c97ba90bd7b75ba1fecb276b3a637cf8156bba81c6b29`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.9-alpine`

```console
$ docker pull influxdb@sha256:28b27ba51abbddb2113c728b9fb5e23261733a9bceb995402012e69aa34273d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.9-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e0e9f4602a6cc0632ea1dbc8910759c86b61ece94f6d5894382d6f1b9bcc30e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116713298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac89ea59315d99dec3c08bb1723cf2fbf03c2e11b2705cbc281417dbafc9c37e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:04:28 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:29 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 10:04:29 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 10:04:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 10:04:32 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 05 Apr 2022 10:04:44 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 05 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Apr 2022 10:04:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Apr 2022 10:04:45 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Apr 2022 10:04:45 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Tue, 05 Apr 2022 10:04:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:04:45 GMT
CMD ["influxd"]
# Tue, 05 Apr 2022 10:04:45 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 10:04:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Apr 2022 10:04:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Apr 2022 10:04:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Apr 2022 10:04:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824989658cee0fcd8b3e27d03a0b79d4ae37c3b765afaff6f49d076d0d9dc42`  
		Last Modified: Tue, 05 Apr 2022 10:08:40 GMT  
		Size: 9.8 MB (9836774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fbe7d281a77910553db440ca9d0c4b709850e35385fc474a9b9b11e55db697`  
		Last Modified: Tue, 05 Apr 2022 10:08:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288cce5ed27daa2927f6bc96c87e2581197832a7210cf5813f6d6cfea28afb7e`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 960.6 KB (960617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bae8b0ec17a5d9dbf1eb7e1e3953baef4edaf26b616fcbc218d817636d79d8`  
		Last Modified: Tue, 05 Apr 2022 10:08:45 GMT  
		Size: 103.1 MB (103090641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8f2b193010cbe745a05d4a2907ef5592bcfc3fcf2f8dc3effc77b3db59171`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485640ccb69c912529e7b70604b5ab52e45aaf7fc93bbca67c021628d1f9d141`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6553ced84695f9c93dba30575941508f22f23786270f7612e99ebd6045d0ff5c`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 4.9 KB (4942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.9-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3047f61d3f0deb8b68f3bb32f77ad1da4dc3f935344d6b4978e2b32978569b5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119819824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6df860f31be0a1452ff106725cb2865b8792e1cbca0eac815cee16c231129b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:11:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:11:29 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 04:11:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 04:11:31 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 04:11:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 04:11:35 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 05 Apr 2022 04:11:48 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 05 Apr 2022 04:11:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Apr 2022 04:11:49 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Apr 2022 04:11:51 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Apr 2022 04:11:52 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Tue, 05 Apr 2022 04:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:11:53 GMT
CMD ["influxd"]
# Tue, 05 Apr 2022 04:11:54 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 04:11:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Apr 2022 04:11:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Apr 2022 04:11:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Apr 2022 04:11:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a37e642510b42e25dbe3082e57f33cdcdb65bad4e9468cd5c76fdb5015c7a`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc96d3454b87ca3f120022077fc7d0ff9477f1b5d1c99519902ae6eed0d7b90`  
		Last Modified: Tue, 05 Apr 2022 04:13:16 GMT  
		Size: 9.7 MB (9672606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6c62b5230b53a6e53da9a15c422cfb18b955afc941e7b68331dd84392405c`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a900a68fae805f39a9a8461f2ef4778a30b18c30f3bc6b2b85e0e02a107e4`  
		Last Modified: Tue, 05 Apr 2022 04:13:13 GMT  
		Size: 896.1 KB (896074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b07cab3429e5cb05ce350093f453086d575ea3fa8b8409fca4cabf4772f1b7`  
		Last Modified: Tue, 05 Apr 2022 04:13:23 GMT  
		Size: 106.5 MB (106526974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb98004947e4307dd97bd5347a40979529a3856593981fdf5be5939eddf45abe`  
		Last Modified: Tue, 05 Apr 2022 04:13:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a58f13a13141d9b8be4fdfd19c9bc68286c28872b5e103b27a68bf9af7b4ce`  
		Last Modified: Tue, 05 Apr 2022 04:13:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f057be72e1bceb8361f6e113dba8d132297ec659a68596020245db9a7db3d89`  
		Last Modified: Tue, 05 Apr 2022 04:13:13 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.1`

```console
$ docker pull influxdb@sha256:2f6855f9556b71dbcae60e1065f4710559f14e1cd94c7c3ee9768b64c4e1e4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.1` - linux; amd64

```console
$ docker pull influxdb@sha256:6c3cc5ef911b8c16979f710651675456caf5688ee61775e9d7dd8aefa188dacf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182909101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c756b1d9ee5bf83999f7cbadd8b511e748b4e0d38095bc8421d56e7e24216c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:06:12 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:06:22 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:06:22 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:06:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:06:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:06:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:06:26 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:06:27 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:06:27 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:06:27 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793e652a43b509f8be74eb5064294d379224d59cf97316124fb499858445ef1`  
		Last Modified: Wed, 30 Mar 2022 23:10:07 GMT  
		Size: 108.3 MB (108324795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b482d9f0118895e8c347c58cbd312d1dfcca4330cf1ff83adc712580775e64f`  
		Last Modified: Wed, 30 Mar 2022 23:09:59 GMT  
		Size: 5.3 MB (5324479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2947646d0e18c37cc4fcc392b2cd653b762a7940fed46ee905128f6dbca79cea`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3282f6fa09cdf60983e54f1483883179f885470a104eeb790e88ab1be5d18d0`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ed2126a186f0abce1171df1dc7e227f047395d57632f220dfc30630bbcfd2f`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.1` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b3905f1e9ffb41a7f9fd0ce44eed59301256f1186fd7549ea2f622141215815d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183414472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d3dc0511263ca69dbd9901272be8f4e080ce9403cda81ae40ce68d78efbef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:22:18 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:22:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:22:25 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:22:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:22:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:22:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:22:32 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:22:33 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:22:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:22:34 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:22:35 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:22:36 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:22:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:22:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:22:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6874725511156ff9e815819dffafee7879b8bab6820901484dab85ba06bf9b76`  
		Last Modified: Wed, 30 Mar 2022 23:24:26 GMT  
		Size: 110.9 MB (110891613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4fe266bd0bca43087df62a3f30c9fb7668277a6f5f8ca3b039aff3f0a02816`  
		Last Modified: Wed, 30 Mar 2022 23:24:18 GMT  
		Size: 4.9 MB (4906728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c13758147cee9ae50ab7e4622cd7b280b4931b06e268aee29bbc31d97b978fc`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea839f94b295d7eafff699c715006e4e6695743e971d7c314ccb624ea0c670e`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282331cef6cbe0a9aa18ba4dfc9d6e08a6888c6110f8b2f856e4e15e0c61fe1b`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.1-alpine`

```console
$ docker pull influxdb@sha256:e291151cb07898a6bda5e4089054062f680e8da3f5640739055b53eef1c32616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.1-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b079b754eac2179d0fb6cbd917b17dabaa61ec4b84d9043a0145aa7c843abf73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127272053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b625457991728963436e2e73df9b29da7f25ac3ee39381d20a3250aedbf21bad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:04:28 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:29 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 10:04:29 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 10:04:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 10:05:20 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 05 Apr 2022 10:05:31 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 05 Apr 2022 10:05:32 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 05 Apr 2022 10:05:34 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 05 Apr 2022 10:05:35 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Apr 2022 10:05:35 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Apr 2022 10:05:35 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Apr 2022 10:05:35 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 05 Apr 2022 10:05:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:05:35 GMT
CMD ["influxd"]
# Tue, 05 Apr 2022 10:05:35 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 10:05:36 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Apr 2022 10:05:36 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Apr 2022 10:05:36 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Apr 2022 10:05:36 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824989658cee0fcd8b3e27d03a0b79d4ae37c3b765afaff6f49d076d0d9dc42`  
		Last Modified: Tue, 05 Apr 2022 10:08:40 GMT  
		Size: 9.8 MB (9836774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fbe7d281a77910553db440ca9d0c4b709850e35385fc474a9b9b11e55db697`  
		Last Modified: Tue, 05 Apr 2022 10:08:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288cce5ed27daa2927f6bc96c87e2581197832a7210cf5813f6d6cfea28afb7e`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 960.6 KB (960617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa20fe4d2144c6d8b09c669080f4145864de9ae356d813f67bddf10ed780428`  
		Last Modified: Tue, 05 Apr 2022 10:09:05 GMT  
		Size: 108.3 MB (108324842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e25e004a13a0ffacc4e90bbdd9e5c7e28df4b9bad56bbc9ec937d480616870c`  
		Last Modified: Tue, 05 Apr 2022 10:08:58 GMT  
		Size: 5.3 MB (5324482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ec7b1f550404a6e00cc084eefd5a5848dc8048e6d5574e3c7f394a32ca496`  
		Last Modified: Tue, 05 Apr 2022 10:08:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b331187d9cf6871ee12477b3eb2b2e80ae08e4ddad74fe84755de07e7ffa25ca`  
		Last Modified: Tue, 05 Apr 2022 10:08:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f47f19904df14de1b0ee2d747e393e312a1486920fa4c780f4d00c752b740`  
		Last Modified: Tue, 05 Apr 2022 10:08:57 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4bdd7bd9a0fac859951bb481dcb08bcc509d5e6a837466175fe623918ede1419
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129091252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9771a96083d7ccceef184f3c0809a099c72f18747f4cba3e332285019ef65bd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:11:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:11:29 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 04:11:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 04:11:31 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 04:11:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 04:12:08 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 05 Apr 2022 04:12:17 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 05 Apr 2022 04:12:17 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 05 Apr 2022 04:12:21 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 05 Apr 2022 04:12:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Apr 2022 04:12:23 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Apr 2022 04:12:25 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Apr 2022 04:12:26 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 05 Apr 2022 04:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:12:27 GMT
CMD ["influxd"]
# Tue, 05 Apr 2022 04:12:28 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 04:12:29 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Apr 2022 04:12:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Apr 2022 04:12:31 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Apr 2022 04:12:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a37e642510b42e25dbe3082e57f33cdcdb65bad4e9468cd5c76fdb5015c7a`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc96d3454b87ca3f120022077fc7d0ff9477f1b5d1c99519902ae6eed0d7b90`  
		Last Modified: Tue, 05 Apr 2022 04:13:16 GMT  
		Size: 9.7 MB (9672606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6c62b5230b53a6e53da9a15c422cfb18b955afc941e7b68331dd84392405c`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a900a68fae805f39a9a8461f2ef4778a30b18c30f3bc6b2b85e0e02a107e4`  
		Last Modified: Tue, 05 Apr 2022 04:13:13 GMT  
		Size: 896.1 KB (896074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1257d89608d6eb5bdb2b1dfd384f22aa999ecf1f5beb80cbdca7a7ea84462f`  
		Last Modified: Tue, 05 Apr 2022 04:13:45 GMT  
		Size: 110.9 MB (110891601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b43473396e5795083c86476af148fe3f0f258afd208843cc16b2a324fc8d3b`  
		Last Modified: Tue, 05 Apr 2022 04:13:37 GMT  
		Size: 4.9 MB (4906734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411147f402cae334bfe0485c46406abcaf0dba246f334c9fc098fdb2b7d98626`  
		Last Modified: Tue, 05 Apr 2022 04:13:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5c74a2e1dee8c1831544c3bf6c3368525e04eeecac99a6a3de888c847c79cb`  
		Last Modified: Tue, 05 Apr 2022 04:13:36 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384858da93c08ecacc18d9c934002579ab9c0f55d7a42eddc6910abb09ceaa2`  
		Last Modified: Tue, 05 Apr 2022 04:13:36 GMT  
		Size: 5.0 KB (5017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.1.1`

```console
$ docker pull influxdb@sha256:2f6855f9556b71dbcae60e1065f4710559f14e1cd94c7c3ee9768b64c4e1e4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.1.1` - linux; amd64

```console
$ docker pull influxdb@sha256:6c3cc5ef911b8c16979f710651675456caf5688ee61775e9d7dd8aefa188dacf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182909101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c756b1d9ee5bf83999f7cbadd8b511e748b4e0d38095bc8421d56e7e24216c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:06:12 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:06:22 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:06:22 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:06:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:06:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:06:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:06:26 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:06:27 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:06:27 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:06:27 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793e652a43b509f8be74eb5064294d379224d59cf97316124fb499858445ef1`  
		Last Modified: Wed, 30 Mar 2022 23:10:07 GMT  
		Size: 108.3 MB (108324795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b482d9f0118895e8c347c58cbd312d1dfcca4330cf1ff83adc712580775e64f`  
		Last Modified: Wed, 30 Mar 2022 23:09:59 GMT  
		Size: 5.3 MB (5324479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2947646d0e18c37cc4fcc392b2cd653b762a7940fed46ee905128f6dbca79cea`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3282f6fa09cdf60983e54f1483883179f885470a104eeb790e88ab1be5d18d0`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ed2126a186f0abce1171df1dc7e227f047395d57632f220dfc30630bbcfd2f`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.1.1` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b3905f1e9ffb41a7f9fd0ce44eed59301256f1186fd7549ea2f622141215815d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183414472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d3dc0511263ca69dbd9901272be8f4e080ce9403cda81ae40ce68d78efbef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:22:18 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:22:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:22:25 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:22:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:22:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:22:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:22:32 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:22:33 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:22:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:22:34 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:22:35 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:22:36 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:22:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:22:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:22:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6874725511156ff9e815819dffafee7879b8bab6820901484dab85ba06bf9b76`  
		Last Modified: Wed, 30 Mar 2022 23:24:26 GMT  
		Size: 110.9 MB (110891613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4fe266bd0bca43087df62a3f30c9fb7668277a6f5f8ca3b039aff3f0a02816`  
		Last Modified: Wed, 30 Mar 2022 23:24:18 GMT  
		Size: 4.9 MB (4906728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c13758147cee9ae50ab7e4622cd7b280b4931b06e268aee29bbc31d97b978fc`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea839f94b295d7eafff699c715006e4e6695743e971d7c314ccb624ea0c670e`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282331cef6cbe0a9aa18ba4dfc9d6e08a6888c6110f8b2f856e4e15e0c61fe1b`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.1.1-alpine`

```console
$ docker pull influxdb@sha256:e291151cb07898a6bda5e4089054062f680e8da3f5640739055b53eef1c32616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.1.1-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b079b754eac2179d0fb6cbd917b17dabaa61ec4b84d9043a0145aa7c843abf73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127272053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b625457991728963436e2e73df9b29da7f25ac3ee39381d20a3250aedbf21bad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:04:28 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:29 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 10:04:29 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 10:04:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 10:05:20 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 05 Apr 2022 10:05:31 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 05 Apr 2022 10:05:32 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 05 Apr 2022 10:05:34 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 05 Apr 2022 10:05:35 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Apr 2022 10:05:35 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Apr 2022 10:05:35 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Apr 2022 10:05:35 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 05 Apr 2022 10:05:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:05:35 GMT
CMD ["influxd"]
# Tue, 05 Apr 2022 10:05:35 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 10:05:36 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Apr 2022 10:05:36 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Apr 2022 10:05:36 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Apr 2022 10:05:36 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824989658cee0fcd8b3e27d03a0b79d4ae37c3b765afaff6f49d076d0d9dc42`  
		Last Modified: Tue, 05 Apr 2022 10:08:40 GMT  
		Size: 9.8 MB (9836774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fbe7d281a77910553db440ca9d0c4b709850e35385fc474a9b9b11e55db697`  
		Last Modified: Tue, 05 Apr 2022 10:08:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288cce5ed27daa2927f6bc96c87e2581197832a7210cf5813f6d6cfea28afb7e`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 960.6 KB (960617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa20fe4d2144c6d8b09c669080f4145864de9ae356d813f67bddf10ed780428`  
		Last Modified: Tue, 05 Apr 2022 10:09:05 GMT  
		Size: 108.3 MB (108324842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e25e004a13a0ffacc4e90bbdd9e5c7e28df4b9bad56bbc9ec937d480616870c`  
		Last Modified: Tue, 05 Apr 2022 10:08:58 GMT  
		Size: 5.3 MB (5324482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ec7b1f550404a6e00cc084eefd5a5848dc8048e6d5574e3c7f394a32ca496`  
		Last Modified: Tue, 05 Apr 2022 10:08:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b331187d9cf6871ee12477b3eb2b2e80ae08e4ddad74fe84755de07e7ffa25ca`  
		Last Modified: Tue, 05 Apr 2022 10:08:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f47f19904df14de1b0ee2d747e393e312a1486920fa4c780f4d00c752b740`  
		Last Modified: Tue, 05 Apr 2022 10:08:57 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4bdd7bd9a0fac859951bb481dcb08bcc509d5e6a837466175fe623918ede1419
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129091252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9771a96083d7ccceef184f3c0809a099c72f18747f4cba3e332285019ef65bd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:11:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:11:29 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 04:11:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 04:11:31 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 04:11:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 04:12:08 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 05 Apr 2022 04:12:17 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 05 Apr 2022 04:12:17 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 05 Apr 2022 04:12:21 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 05 Apr 2022 04:12:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Apr 2022 04:12:23 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Apr 2022 04:12:25 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Apr 2022 04:12:26 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 05 Apr 2022 04:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:12:27 GMT
CMD ["influxd"]
# Tue, 05 Apr 2022 04:12:28 GMT
EXPOSE 8086
# Tue, 05 Apr 2022 04:12:29 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Apr 2022 04:12:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Apr 2022 04:12:31 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Apr 2022 04:12:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a37e642510b42e25dbe3082e57f33cdcdb65bad4e9468cd5c76fdb5015c7a`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc96d3454b87ca3f120022077fc7d0ff9477f1b5d1c99519902ae6eed0d7b90`  
		Last Modified: Tue, 05 Apr 2022 04:13:16 GMT  
		Size: 9.7 MB (9672606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6c62b5230b53a6e53da9a15c422cfb18b955afc941e7b68331dd84392405c`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a900a68fae805f39a9a8461f2ef4778a30b18c30f3bc6b2b85e0e02a107e4`  
		Last Modified: Tue, 05 Apr 2022 04:13:13 GMT  
		Size: 896.1 KB (896074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1257d89608d6eb5bdb2b1dfd384f22aa999ecf1f5beb80cbdca7a7ea84462f`  
		Last Modified: Tue, 05 Apr 2022 04:13:45 GMT  
		Size: 110.9 MB (110891601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b43473396e5795083c86476af148fe3f0f258afd208843cc16b2a324fc8d3b`  
		Last Modified: Tue, 05 Apr 2022 04:13:37 GMT  
		Size: 4.9 MB (4906734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411147f402cae334bfe0485c46406abcaf0dba246f334c9fc098fdb2b7d98626`  
		Last Modified: Tue, 05 Apr 2022 04:13:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5c74a2e1dee8c1831544c3bf6c3368525e04eeecac99a6a3de888c847c79cb`  
		Last Modified: Tue, 05 Apr 2022 04:13:36 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384858da93c08ecacc18d9c934002579ab9c0f55d7a42eddc6910abb09ceaa2`  
		Last Modified: Tue, 05 Apr 2022 04:13:36 GMT  
		Size: 5.0 KB (5017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.2`

```console
$ docker pull influxdb@sha256:7b6e0d14ac7be2160805ad94437340ad873dded140b0c349d91d26b97189c806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.2` - linux; amd64

```console
$ docker pull influxdb@sha256:1ddb861a2fb072066d7cad6f19ea7fae5b0a7bed3ca0385671e7148f3f5bcd2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181847219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8002e02d05b4305cee201579d98f86bedf14e93dc990ff5c758d7b12bdf197d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Thu, 07 Apr 2022 22:23:38 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:23:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:23:45 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:23:48 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:23:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:23:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:23:48 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:23:48 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:49 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:23:49 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:23:49 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:23:49 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:23:49 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:23:49 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bda7f0a81d0368006d8496a2e5e68912e01bb77fe8ad9d1a55da256201f6c2`  
		Last Modified: Thu, 07 Apr 2022 22:26:01 GMT  
		Size: 107.2 MB (107220549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90659effdd9af74beb453d46653ccf9f47e561e8f39ba0e8a94e00df8534e192`  
		Last Modified: Thu, 07 Apr 2022 22:25:55 GMT  
		Size: 5.4 MB (5366843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4993fac67787e4d46e8bd7f90feb8b2f5839dd05bb8439975675bf0ad6509d60`  
		Last Modified: Thu, 07 Apr 2022 22:25:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e94df37fe446e518d83994d96795f9f1cdce4cbfce525c32326b430220e134`  
		Last Modified: Thu, 07 Apr 2022 22:25:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a4be4ffade7adaa97ff3ef1cb2494793c1d574bd0034861f6f125e5872a80`  
		Last Modified: Thu, 07 Apr 2022 22:25:54 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0534dd196993bcba769c4c10965e471808968762ea8004c55d73eede94b69cf9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182446729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0c668c5f9117cc5644302f77a1b4746fd0cc33868679819dc685f9ccf5745b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Thu, 07 Apr 2022 22:40:20 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:40:31 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:40:32 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:40:47 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:40:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:40:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:40:50 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:40:51 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:40:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:40:52 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:40:53 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:40:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:40:55 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:40:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:40:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dcf6c88bea65a737e30927f100004c1b26cfab698cfc049dad91b353ab9c09`  
		Last Modified: Thu, 07 Apr 2022 22:42:22 GMT  
		Size: 109.9 MB (109877972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928d47cdaea7f28fb42d30a1ad34b8b7a315dca8a9ff36654177628d7d179209`  
		Last Modified: Thu, 07 Apr 2022 22:42:14 GMT  
		Size: 5.0 MB (4952629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7113646946c8fe4025920fb8e00dfff4fe0975acfc3082246d13ee7707558c`  
		Last Modified: Thu, 07 Apr 2022 22:42:13 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416eadcf53abf682f3af46efc62622af767fb13fd231f8cabbf9b5d383fbe892`  
		Last Modified: Thu, 07 Apr 2022 22:42:13 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774b32737695c555746e8ed8900010a35d31850cad33f880dd1572f5b2964c0`  
		Last Modified: Thu, 07 Apr 2022 22:42:13 GMT  
		Size: 5.0 KB (5013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.2-alpine`

```console
$ docker pull influxdb@sha256:e54e532b67a466296fd229046de57ea364ec3fc311024fb6cf04ef8b3f826724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:944d3703e0d229c834124702b52cb9a38ba70148cbe9a91047549a6f1d4100c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126210124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f915cf00224d1e1471d7f995be37339638c7a1f48ff534622ba6de7979fa918`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:04:28 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:29 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 10:04:29 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 10:04:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Apr 2022 22:23:52 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:23:59 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:23:59 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:24:02 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:24:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:24:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:24:03 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:24:03 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Thu, 07 Apr 2022 22:24:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:24:03 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:24:03 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:24:03 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:24:03 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:24:03 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:24:03 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824989658cee0fcd8b3e27d03a0b79d4ae37c3b765afaff6f49d076d0d9dc42`  
		Last Modified: Tue, 05 Apr 2022 10:08:40 GMT  
		Size: 9.8 MB (9836774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fbe7d281a77910553db440ca9d0c4b709850e35385fc474a9b9b11e55db697`  
		Last Modified: Tue, 05 Apr 2022 10:08:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288cce5ed27daa2927f6bc96c87e2581197832a7210cf5813f6d6cfea28afb7e`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 960.6 KB (960617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda4cec68da03e4a2c0505bf914835d468d2381a18d7f5523dff04a4104548f0`  
		Last Modified: Thu, 07 Apr 2022 22:26:22 GMT  
		Size: 107.2 MB (107220530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1803721aa5af5cf4595b4f6d1ec77b85528f1d017159ee2795fbc7be1754dfd`  
		Last Modified: Thu, 07 Apr 2022 22:26:16 GMT  
		Size: 5.4 MB (5366860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698fbf636ae0f2c376b436111ab290b41ba6a62006984cba8613f717c197999a`  
		Last Modified: Thu, 07 Apr 2022 22:26:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d763963a1494238194f51588c6093ef14a5d5035d0b15370b6f8064484d6ab`  
		Last Modified: Thu, 07 Apr 2022 22:26:15 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab47c4b7f6fac482d97780e3e699c1976910bcda6881cd8ec4d264377e326bc5`  
		Last Modified: Thu, 07 Apr 2022 22:26:15 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4e04338689d6ae55cb2e51f9574dff5db9ecdabfefc979f32c19dd8109a36245
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128123536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d2948df1c4115ccad9b6da3e19299c8f6b1b80370b2aae23233b7e424d3713`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:11:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:11:29 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 04:11:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 04:11:31 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 04:11:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Apr 2022 22:41:04 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:41:14 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:41:15 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:41:19 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:41:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:41:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:41:23 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:41:24 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Thu, 07 Apr 2022 22:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:41:25 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:41:26 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:41:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:41:28 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:41:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:41:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a37e642510b42e25dbe3082e57f33cdcdb65bad4e9468cd5c76fdb5015c7a`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc96d3454b87ca3f120022077fc7d0ff9477f1b5d1c99519902ae6eed0d7b90`  
		Last Modified: Tue, 05 Apr 2022 04:13:16 GMT  
		Size: 9.7 MB (9672606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6c62b5230b53a6e53da9a15c422cfb18b955afc941e7b68331dd84392405c`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a900a68fae805f39a9a8461f2ef4778a30b18c30f3bc6b2b85e0e02a107e4`  
		Last Modified: Tue, 05 Apr 2022 04:13:13 GMT  
		Size: 896.1 KB (896074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5fa0ea408fd6ffd1ee82e3ea8008fc3465cafabaeae75f18d2cf348351c1e4`  
		Last Modified: Thu, 07 Apr 2022 22:42:47 GMT  
		Size: 109.9 MB (109877972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960db3c3158879adcdf59bc12c3c38c1af5913bd9a84977150e7d8aeb95c801a`  
		Last Modified: Thu, 07 Apr 2022 22:42:40 GMT  
		Size: 5.0 MB (4952646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df20c8d48e4fd0c3e42141cc86af9e54a4216943054d882550dd9a77be5c77dd`  
		Last Modified: Thu, 07 Apr 2022 22:42:39 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd86c97dd0108cc33d98391fe4637c43e2ff7ad8dcb9f7663237e312c2fddb8`  
		Last Modified: Thu, 07 Apr 2022 22:42:38 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6e9a8ef77f045422b81ae5a910ea9b4886105ed0d01777f0aead72441f00f`  
		Last Modified: Thu, 07 Apr 2022 22:42:38 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.2.0`

```console
$ docker pull influxdb@sha256:7b6e0d14ac7be2160805ad94437340ad873dded140b0c349d91d26b97189c806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.2.0` - linux; amd64

```console
$ docker pull influxdb@sha256:1ddb861a2fb072066d7cad6f19ea7fae5b0a7bed3ca0385671e7148f3f5bcd2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181847219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8002e02d05b4305cee201579d98f86bedf14e93dc990ff5c758d7b12bdf197d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Thu, 07 Apr 2022 22:23:38 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:23:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:23:45 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:23:48 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:23:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:23:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:23:48 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:23:48 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:49 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:23:49 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:23:49 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:23:49 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:23:49 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:23:49 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bda7f0a81d0368006d8496a2e5e68912e01bb77fe8ad9d1a55da256201f6c2`  
		Last Modified: Thu, 07 Apr 2022 22:26:01 GMT  
		Size: 107.2 MB (107220549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90659effdd9af74beb453d46653ccf9f47e561e8f39ba0e8a94e00df8534e192`  
		Last Modified: Thu, 07 Apr 2022 22:25:55 GMT  
		Size: 5.4 MB (5366843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4993fac67787e4d46e8bd7f90feb8b2f5839dd05bb8439975675bf0ad6509d60`  
		Last Modified: Thu, 07 Apr 2022 22:25:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e94df37fe446e518d83994d96795f9f1cdce4cbfce525c32326b430220e134`  
		Last Modified: Thu, 07 Apr 2022 22:25:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a4be4ffade7adaa97ff3ef1cb2494793c1d574bd0034861f6f125e5872a80`  
		Last Modified: Thu, 07 Apr 2022 22:25:54 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.2.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0534dd196993bcba769c4c10965e471808968762ea8004c55d73eede94b69cf9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182446729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0c668c5f9117cc5644302f77a1b4746fd0cc33868679819dc685f9ccf5745b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Thu, 07 Apr 2022 22:40:20 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:40:31 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:40:32 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:40:47 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:40:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:40:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:40:50 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:40:51 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:40:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:40:52 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:40:53 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:40:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:40:55 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:40:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:40:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dcf6c88bea65a737e30927f100004c1b26cfab698cfc049dad91b353ab9c09`  
		Last Modified: Thu, 07 Apr 2022 22:42:22 GMT  
		Size: 109.9 MB (109877972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928d47cdaea7f28fb42d30a1ad34b8b7a315dca8a9ff36654177628d7d179209`  
		Last Modified: Thu, 07 Apr 2022 22:42:14 GMT  
		Size: 5.0 MB (4952629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7113646946c8fe4025920fb8e00dfff4fe0975acfc3082246d13ee7707558c`  
		Last Modified: Thu, 07 Apr 2022 22:42:13 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416eadcf53abf682f3af46efc62622af767fb13fd231f8cabbf9b5d383fbe892`  
		Last Modified: Thu, 07 Apr 2022 22:42:13 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774b32737695c555746e8ed8900010a35d31850cad33f880dd1572f5b2964c0`  
		Last Modified: Thu, 07 Apr 2022 22:42:13 GMT  
		Size: 5.0 KB (5013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.2.0-alpine`

```console
$ docker pull influxdb@sha256:e54e532b67a466296fd229046de57ea364ec3fc311024fb6cf04ef8b3f826724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.2.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:944d3703e0d229c834124702b52cb9a38ba70148cbe9a91047549a6f1d4100c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126210124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f915cf00224d1e1471d7f995be37339638c7a1f48ff534622ba6de7979fa918`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:04:28 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:29 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 10:04:29 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 10:04:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Apr 2022 22:23:52 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:23:59 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:23:59 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:24:02 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:24:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:24:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:24:03 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:24:03 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Thu, 07 Apr 2022 22:24:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:24:03 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:24:03 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:24:03 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:24:03 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:24:03 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:24:03 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824989658cee0fcd8b3e27d03a0b79d4ae37c3b765afaff6f49d076d0d9dc42`  
		Last Modified: Tue, 05 Apr 2022 10:08:40 GMT  
		Size: 9.8 MB (9836774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fbe7d281a77910553db440ca9d0c4b709850e35385fc474a9b9b11e55db697`  
		Last Modified: Tue, 05 Apr 2022 10:08:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288cce5ed27daa2927f6bc96c87e2581197832a7210cf5813f6d6cfea28afb7e`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 960.6 KB (960617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda4cec68da03e4a2c0505bf914835d468d2381a18d7f5523dff04a4104548f0`  
		Last Modified: Thu, 07 Apr 2022 22:26:22 GMT  
		Size: 107.2 MB (107220530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1803721aa5af5cf4595b4f6d1ec77b85528f1d017159ee2795fbc7be1754dfd`  
		Last Modified: Thu, 07 Apr 2022 22:26:16 GMT  
		Size: 5.4 MB (5366860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698fbf636ae0f2c376b436111ab290b41ba6a62006984cba8613f717c197999a`  
		Last Modified: Thu, 07 Apr 2022 22:26:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d763963a1494238194f51588c6093ef14a5d5035d0b15370b6f8064484d6ab`  
		Last Modified: Thu, 07 Apr 2022 22:26:15 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab47c4b7f6fac482d97780e3e699c1976910bcda6881cd8ec4d264377e326bc5`  
		Last Modified: Thu, 07 Apr 2022 22:26:15 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4e04338689d6ae55cb2e51f9574dff5db9ecdabfefc979f32c19dd8109a36245
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128123536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d2948df1c4115ccad9b6da3e19299c8f6b1b80370b2aae23233b7e424d3713`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:11:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:11:29 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 04:11:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 04:11:31 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 04:11:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Apr 2022 22:41:04 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:41:14 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:41:15 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:41:19 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:41:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:41:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:41:23 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:41:24 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Thu, 07 Apr 2022 22:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:41:25 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:41:26 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:41:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:41:28 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:41:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:41:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a37e642510b42e25dbe3082e57f33cdcdb65bad4e9468cd5c76fdb5015c7a`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc96d3454b87ca3f120022077fc7d0ff9477f1b5d1c99519902ae6eed0d7b90`  
		Last Modified: Tue, 05 Apr 2022 04:13:16 GMT  
		Size: 9.7 MB (9672606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6c62b5230b53a6e53da9a15c422cfb18b955afc941e7b68331dd84392405c`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a900a68fae805f39a9a8461f2ef4778a30b18c30f3bc6b2b85e0e02a107e4`  
		Last Modified: Tue, 05 Apr 2022 04:13:13 GMT  
		Size: 896.1 KB (896074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5fa0ea408fd6ffd1ee82e3ea8008fc3465cafabaeae75f18d2cf348351c1e4`  
		Last Modified: Thu, 07 Apr 2022 22:42:47 GMT  
		Size: 109.9 MB (109877972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960db3c3158879adcdf59bc12c3c38c1af5913bd9a84977150e7d8aeb95c801a`  
		Last Modified: Thu, 07 Apr 2022 22:42:40 GMT  
		Size: 5.0 MB (4952646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df20c8d48e4fd0c3e42141cc86af9e54a4216943054d882550dd9a77be5c77dd`  
		Last Modified: Thu, 07 Apr 2022 22:42:39 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd86c97dd0108cc33d98391fe4637c43e2ff7ad8dcb9f7663237e312c2fddb8`  
		Last Modified: Thu, 07 Apr 2022 22:42:38 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6e9a8ef77f045422b81ae5a910ea9b4886105ed0d01777f0aead72441f00f`  
		Last Modified: Thu, 07 Apr 2022 22:42:38 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:e54e532b67a466296fd229046de57ea364ec3fc311024fb6cf04ef8b3f826724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:944d3703e0d229c834124702b52cb9a38ba70148cbe9a91047549a6f1d4100c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126210124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f915cf00224d1e1471d7f995be37339638c7a1f48ff534622ba6de7979fa918`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:04:28 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 10:04:29 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 10:04:29 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 10:04:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Apr 2022 22:23:52 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:23:59 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:23:59 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:24:02 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:24:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:24:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:24:03 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:24:03 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Thu, 07 Apr 2022 22:24:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:24:03 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:24:03 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:24:03 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:24:03 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:24:03 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:24:03 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824989658cee0fcd8b3e27d03a0b79d4ae37c3b765afaff6f49d076d0d9dc42`  
		Last Modified: Tue, 05 Apr 2022 10:08:40 GMT  
		Size: 9.8 MB (9836774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fbe7d281a77910553db440ca9d0c4b709850e35385fc474a9b9b11e55db697`  
		Last Modified: Tue, 05 Apr 2022 10:08:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288cce5ed27daa2927f6bc96c87e2581197832a7210cf5813f6d6cfea28afb7e`  
		Last Modified: Tue, 05 Apr 2022 10:08:36 GMT  
		Size: 960.6 KB (960617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda4cec68da03e4a2c0505bf914835d468d2381a18d7f5523dff04a4104548f0`  
		Last Modified: Thu, 07 Apr 2022 22:26:22 GMT  
		Size: 107.2 MB (107220530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1803721aa5af5cf4595b4f6d1ec77b85528f1d017159ee2795fbc7be1754dfd`  
		Last Modified: Thu, 07 Apr 2022 22:26:16 GMT  
		Size: 5.4 MB (5366860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698fbf636ae0f2c376b436111ab290b41ba6a62006984cba8613f717c197999a`  
		Last Modified: Thu, 07 Apr 2022 22:26:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d763963a1494238194f51588c6093ef14a5d5035d0b15370b6f8064484d6ab`  
		Last Modified: Thu, 07 Apr 2022 22:26:15 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab47c4b7f6fac482d97780e3e699c1976910bcda6881cd8ec4d264377e326bc5`  
		Last Modified: Thu, 07 Apr 2022 22:26:15 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4e04338689d6ae55cb2e51f9574dff5db9ecdabfefc979f32c19dd8109a36245
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128123536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d2948df1c4115ccad9b6da3e19299c8f6b1b80370b2aae23233b7e424d3713`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:11:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:11:29 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 05 Apr 2022 04:11:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 05 Apr 2022 04:11:31 GMT
ENV GOSU_VER=1.12
# Tue, 05 Apr 2022 04:11:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Apr 2022 22:41:04 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:41:14 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:41:15 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:41:19 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:41:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:41:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:41:23 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:41:24 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Thu, 07 Apr 2022 22:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:41:25 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:41:26 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:41:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:41:28 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:41:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:41:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a37e642510b42e25dbe3082e57f33cdcdb65bad4e9468cd5c76fdb5015c7a`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc96d3454b87ca3f120022077fc7d0ff9477f1b5d1c99519902ae6eed0d7b90`  
		Last Modified: Tue, 05 Apr 2022 04:13:16 GMT  
		Size: 9.7 MB (9672606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6c62b5230b53a6e53da9a15c422cfb18b955afc941e7b68331dd84392405c`  
		Last Modified: Tue, 05 Apr 2022 04:13:15 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a900a68fae805f39a9a8461f2ef4778a30b18c30f3bc6b2b85e0e02a107e4`  
		Last Modified: Tue, 05 Apr 2022 04:13:13 GMT  
		Size: 896.1 KB (896074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5fa0ea408fd6ffd1ee82e3ea8008fc3465cafabaeae75f18d2cf348351c1e4`  
		Last Modified: Thu, 07 Apr 2022 22:42:47 GMT  
		Size: 109.9 MB (109877972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960db3c3158879adcdf59bc12c3c38c1af5913bd9a84977150e7d8aeb95c801a`  
		Last Modified: Thu, 07 Apr 2022 22:42:40 GMT  
		Size: 5.0 MB (4952646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df20c8d48e4fd0c3e42141cc86af9e54a4216943054d882550dd9a77be5c77dd`  
		Last Modified: Thu, 07 Apr 2022 22:42:39 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd86c97dd0108cc33d98391fe4637c43e2ff7ad8dcb9f7663237e312c2fddb8`  
		Last Modified: Thu, 07 Apr 2022 22:42:38 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6e9a8ef77f045422b81ae5a910ea9b4886105ed0d01777f0aead72441f00f`  
		Last Modified: Thu, 07 Apr 2022 22:42:38 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:be2d5a7bd5ff0644383defcce1f7769ae89363d5867ac5b2615ae2731dcb6c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:0790872efd83e02d8fdd2faf7a2ff410f9ff50a007b58c517d14c783d48130d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117786452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276cebfb7edd0645264657425ddb00bb2bcb80b7dce64169b9281067ebc0707c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:25 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edcfcb7a5161abd03b61b6153c6f903029bcfb2d9efa4a6556918c51a064af1`  
		Last Modified: Wed, 30 Mar 2022 23:08:36 GMT  
		Size: 56.7 MB (56709163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97289aef350957936b3a19d68c846a790247f957e99f5d9f0e9c628bc74e2d0f`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1caefc2f0645fadbdce8da95cfbe3bdf21d1712e3d4b95577a26a55d97debc`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fc4496b0657c51da18c2c520e35381f811fe8d8a7eb3c3f4b15209a3b00900`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:5b6f51f9283101e2260d04e4ec6e97e6ac6b42906de0330d245556207485ff9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ffe5860e830f75f1ecc06f6d9ef5131783a4009bf8c178a202b221b7090991d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60799475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51bbfae48c946a370eace3f872988f7daf93c3ee3586f383c6165ed132c4760`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:03:43 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Thu, 07 Apr 2022 22:22:53 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:22:54 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 07 Apr 2022 22:22:54 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:22:54 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:22:54 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:22:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 07 Apr 2022 22:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:22:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d253e65fc0c40504c5ab7ed8891c7535ce694e62e9b315612518257a49a27e`  
		Last Modified: Thu, 07 Apr 2022 22:24:53 GMT  
		Size: 56.5 MB (56503671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c14b9a988386b736ef6a259676adf189b9aee692453b5a41173a23bd2aed93e`  
		Last Modified: Thu, 07 Apr 2022 22:24:46 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1e32c4578db25e99bb2f5fbd9bae12550160681dd612559a2fdb24774b6636`  
		Last Modified: Thu, 07 Apr 2022 22:24:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3641a605f831a5d23969cb82df4b923d91d0377459df0169f7c92d5a15449a9`  
		Last Modified: Thu, 07 Apr 2022 22:24:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:7b6e0d14ac7be2160805ad94437340ad873dded140b0c349d91d26b97189c806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:1ddb861a2fb072066d7cad6f19ea7fae5b0a7bed3ca0385671e7148f3f5bcd2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181847219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8002e02d05b4305cee201579d98f86bedf14e93dc990ff5c758d7b12bdf197d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Thu, 07 Apr 2022 22:23:38 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:23:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:23:45 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:23:48 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:23:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:23:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:23:48 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:23:48 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:49 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:23:49 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:23:49 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:23:49 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:23:49 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:23:49 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bda7f0a81d0368006d8496a2e5e68912e01bb77fe8ad9d1a55da256201f6c2`  
		Last Modified: Thu, 07 Apr 2022 22:26:01 GMT  
		Size: 107.2 MB (107220549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90659effdd9af74beb453d46653ccf9f47e561e8f39ba0e8a94e00df8534e192`  
		Last Modified: Thu, 07 Apr 2022 22:25:55 GMT  
		Size: 5.4 MB (5366843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4993fac67787e4d46e8bd7f90feb8b2f5839dd05bb8439975675bf0ad6509d60`  
		Last Modified: Thu, 07 Apr 2022 22:25:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e94df37fe446e518d83994d96795f9f1cdce4cbfce525c32326b430220e134`  
		Last Modified: Thu, 07 Apr 2022 22:25:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a4be4ffade7adaa97ff3ef1cb2494793c1d574bd0034861f6f125e5872a80`  
		Last Modified: Thu, 07 Apr 2022 22:25:54 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0534dd196993bcba769c4c10965e471808968762ea8004c55d73eede94b69cf9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182446729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0c668c5f9117cc5644302f77a1b4746fd0cc33868679819dc685f9ccf5745b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Thu, 07 Apr 2022 22:40:20 GMT
ENV INFLUXDB_VERSION=2.2.0
# Thu, 07 Apr 2022 22:40:31 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 07 Apr 2022 22:40:32 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 07 Apr 2022 22:40:47 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 07 Apr 2022 22:40:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 07 Apr 2022 22:40:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 07 Apr 2022 22:40:50 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 07 Apr 2022 22:40:51 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:40:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:40:52 GMT
CMD ["influxd"]
# Thu, 07 Apr 2022 22:40:53 GMT
EXPOSE 8086
# Thu, 07 Apr 2022 22:40:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 07 Apr 2022 22:40:55 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 07 Apr 2022 22:40:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 07 Apr 2022 22:40:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dcf6c88bea65a737e30927f100004c1b26cfab698cfc049dad91b353ab9c09`  
		Last Modified: Thu, 07 Apr 2022 22:42:22 GMT  
		Size: 109.9 MB (109877972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928d47cdaea7f28fb42d30a1ad34b8b7a315dca8a9ff36654177628d7d179209`  
		Last Modified: Thu, 07 Apr 2022 22:42:14 GMT  
		Size: 5.0 MB (4952629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7113646946c8fe4025920fb8e00dfff4fe0975acfc3082246d13ee7707558c`  
		Last Modified: Thu, 07 Apr 2022 22:42:13 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416eadcf53abf682f3af46efc62622af767fb13fd231f8cabbf9b5d383fbe892`  
		Last Modified: Thu, 07 Apr 2022 22:42:13 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774b32737695c555746e8ed8900010a35d31850cad33f880dd1572f5b2964c0`  
		Last Modified: Thu, 07 Apr 2022 22:42:13 GMT  
		Size: 5.0 KB (5013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:4727e7c393e16502a487921e0fcae07eaaf9e00ecf3b22b37562e86d6867188b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c50786838735ef2c78c51e7238a4404520063b935751ce517157749b2904aa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84493011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0e1d0ea12729ab4474843f41d7a88f5a1870ec065e3fe58185c6b0098c0ce1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:32 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:32 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:32 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:32 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:33 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:33 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c487c418525e877d8128d62ac4dc164cba44ce112d1bc88171390368ce61ad53`  
		Last Modified: Wed, 30 Mar 2022 23:08:52 GMT  
		Size: 23.4 MB (23416930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720a75a54e3c5d1a6d4ca4261fc76d135e3e9c04b6804de3b56615706c8fdf17`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feee196124cbe471a1e4ff40944ed9de1949b39f539001874ba0f125d28314d5`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:008db7d140fce00d44cb0f11b4e04a8d5c151222c18e20f1a6e3c40432c1b6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:06b3c6c7fdaaae61c386be3b2db8debdb79dc029c86b28fb2ddd57b7a813cca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27587601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c59c3a9d5137ca189bf5be3e9b530b46a594f7e9911d79fb7ce49a68802cbdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 10:02:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 10:03:43 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Thu, 07 Apr 2022 22:23:04 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 07 Apr 2022 22:23:04 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 07 Apr 2022 22:23:04 GMT
EXPOSE 8091
# Thu, 07 Apr 2022 22:23:04 GMT
VOLUME [/var/lib/influxdb]
# Thu, 07 Apr 2022 22:23:05 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 07 Apr 2022 22:23:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Apr 2022 22:23:05 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a82c2bf0b07bc97e48386998fdb52307a711c8cde52325fb999e1b7a0f0073`  
		Last Modified: Tue, 05 Apr 2022 10:06:22 GMT  
		Size: 1.5 MB (1475485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef0611ecd34d60d54d119ad0d5b217bf9bb505143a9a76d79a71588306f6962`  
		Last Modified: Thu, 07 Apr 2022 22:25:10 GMT  
		Size: 23.3 MB (23292997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03800bc1786c31a63f2ce29355aa6c75587b563883515d7db2faec592fe0bcc5`  
		Last Modified: Thu, 07 Apr 2022 22:25:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56614b1a615f4516c69895cb7e68ac004819d3dd52ffe4766c55c5686847eff`  
		Last Modified: Thu, 07 Apr 2022 22:25:07 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
