## `telegraf:latest`

```console
$ docker pull telegraf@sha256:70e00f28a351478d6bf7002b811d77dbf1eecbd1416100f72df63fab890c7d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:112ff497414774340410a646048252c4a4029014c6ef01a71118ccfae7935a67
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108279751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5023e522cf08de862c6f752ad28247e2d080c5a585eeeec5fb8f44d91f49ac53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 16:58:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:58:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Dec 2020 06:50:42 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 18 Dec 2020 06:50:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Mon, 04 Jan 2021 18:27:55 GMT
ENV TELEGRAF_VERSION=1.17.0
# Mon, 04 Jan 2021 18:27:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 04 Jan 2021 18:27:59 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 04 Jan 2021 18:27:59 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Mon, 04 Jan 2021 18:27:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Jan 2021 18:27:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef072fc32a84ef237dd4fcc7dff2c5e2a77565f24d63977d0fa654a6d8512dd8`  
		Last Modified: Thu, 17 Dec 2020 17:25:57 GMT  
		Size: 7.8 MB (7812075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0afb8e68e0bcdc1b6e05acaa713a6fe0d818086c596bd1ad99133665c4efe63`  
		Last Modified: Thu, 17 Dec 2020 17:25:58 GMT  
		Size: 10.0 MB (9996417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c329c058418191ff634a6d634864a35c05c969a884836841da022c5f1a6a1`  
		Last Modified: Fri, 18 Dec 2020 06:51:40 GMT  
		Size: 17.4 MB (17411917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e88ea3a70986f1b1bb36a8cab0da0833b330ceedf5284b26be6c7baefa456f4`  
		Last Modified: Fri, 18 Dec 2020 06:51:35 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85507263a5b5136cf6e22c8a0d68114a203c46d7e974f196eada5088da350594`  
		Last Modified: Mon, 04 Jan 2021 18:28:34 GMT  
		Size: 22.7 MB (22658559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0565c1e872a46f579a35a0a8a38a53a15858852147f169a0b9b57465299d66`  
		Last Modified: Mon, 04 Jan 2021 18:28:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8c19199a64c3279e359c677dde2a0c74277fae9c3f22fbbfbcbd761d5114ca71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99648011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7136df9355ff833c2e87c3155f2cf6c3193a1e2996866e27572ed6505be9538f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jan 2021 00:00:37 GMT
ADD file:216371f6fe8c803a0191f84e555c809a3301d1344c62b831dddb5e0c595fe0ef in / 
# Tue, 12 Jan 2021 00:00:46 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:15:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 21:04:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 21:04:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Jan 2021 21:05:25 GMT
ENV TELEGRAF_VERSION=1.17.0
# Tue, 12 Jan 2021 21:05:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Jan 2021 21:05:34 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 12 Jan 2021 21:05:35 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Tue, 12 Jan 2021 21:05:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 21:05:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d8925d905dadf63fa0ff74be912443a1cf8cd72ea5543317b0e22067d39ef948`  
		Last Modified: Tue, 12 Jan 2021 00:10:42 GMT  
		Size: 45.9 MB (45870031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd9c5a6d77413d17345fcf1f89b9dde2f3d9d6157bd070d4093cfef30107add`  
		Last Modified: Tue, 12 Jan 2021 01:29:46 GMT  
		Size: 7.1 MB (7099141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e1f8e87a65e3a71764ea79b951f915c90a885dfd516f61e57d81745acaf272`  
		Last Modified: Tue, 12 Jan 2021 01:29:46 GMT  
		Size: 9.3 MB (9343447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ec62dff3056e70cc453ec4b2d4db22debd86a42ddeaa47252e4672774bf7a8`  
		Last Modified: Tue, 12 Jan 2021 21:06:02 GMT  
		Size: 16.2 MB (16158602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e36c129df27747aced5a1d50e367b06ee3dbdd9dcdb8ac6eb7c4e7e5132bd`  
		Last Modified: Tue, 12 Jan 2021 21:05:55 GMT  
		Size: 2.9 KB (2912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11adad9bc0d174d64964f424da339b97b5e8c3e63d8f5492be3784faa4308474`  
		Last Modified: Tue, 12 Jan 2021 21:06:42 GMT  
		Size: 21.2 MB (21173695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0246e9806698bd54eddf04c9d1b8e77d4fa78f0d16d20c1e0f9fd128c09a4b42`  
		Last Modified: Tue, 12 Jan 2021 21:06:36 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9acc0454405b9cbf7f8235efa3703d11526da9f3e26e79a3acd7343f51d3ffff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104892022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827d7c029ef8bbcf5a4ac900c03c066a0938037fb2224c32c4cb8fcf256c9b11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Jan 2021 00:40:39 GMT
ADD file:849d424ecc8572facb3ca68eff836dce211bc677cb32d3c3eaa129d364d33878 in / 
# Tue, 12 Jan 2021 00:40:43 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:23:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 23:34:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 23:34:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Jan 2021 23:35:05 GMT
ENV TELEGRAF_VERSION=1.17.0
# Tue, 12 Jan 2021 23:35:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Jan 2021 23:35:11 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 12 Jan 2021 23:35:12 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Tue, 12 Jan 2021 23:35:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 23:35:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e5587ff5efa4e647ae927194fac9b961a68d46b23b68a3119c90016e58f17aa`  
		Last Modified: Tue, 12 Jan 2021 00:51:18 GMT  
		Size: 49.2 MB (49183736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439dbbb05ea0aa8484ae8a51d0fbb1c7609176a1b0d3f15dad69d52e9a83af66`  
		Last Modified: Tue, 12 Jan 2021 01:38:27 GMT  
		Size: 7.7 MB (7682325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b89c8b4e5b232c040d5905808ee62cdfcc9d697de10183d6bc4767468859d92`  
		Last Modified: Tue, 12 Jan 2021 01:38:27 GMT  
		Size: 10.0 MB (9984327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc23f43b0bc1dd7f18ad8d9c699e4f57a322ad66aeb71996e6e8c9d2020abea`  
		Last Modified: Tue, 12 Jan 2021 23:35:36 GMT  
		Size: 17.3 MB (17269787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9c730332453078e166b4df31247ee7882c51ff0125356dab99e3a9dcc73661`  
		Last Modified: Tue, 12 Jan 2021 23:35:33 GMT  
		Size: 2.9 KB (2897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27206afff310f9eaa82af5e4a0a24130840f3e096de6595a14f768278187c972`  
		Last Modified: Tue, 12 Jan 2021 23:36:05 GMT  
		Size: 20.8 MB (20768767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c781d809f5ce93e141ee7e1ee0d1908b83ea09ad17f215dbec6e71d68ac2d14`  
		Last Modified: Tue, 12 Jan 2021 23:35:59 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
