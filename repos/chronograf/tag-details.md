<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:1af53fbb3069147bf74eeeaaf17a4deba17a30474fa8642302e676aa6a784efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:70b667a17282f4759e22ccb3d92f003469ca1bf9b43e41cf8c6b88dc1ef43880
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49397889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd6c0f131d65571e79b70365992fc8bc78244fd1534cffeb16aa85db58fcddb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:20 GMT
ADD file:cfad5912b6dd7590713979e5a5e231b1b6873200fde725cb7baf75110d7fa138 in / 
# Thu, 23 Jun 2022 00:22:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:03:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:03:40 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 23 Jun 2022 01:03:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:03:48 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:03:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:03:48 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:03:49 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:03:49 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:03:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:03:49 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bff3e048017eab8adaed886bad4b3c5c81f7d952b65b056dca8d6dbc198222dd`  
		Last Modified: Thu, 23 Jun 2022 00:30:01 GMT  
		Size: 22.6 MB (22567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b5498e1d3acd0f9ff62393ea37f571882a0eec6680617ecb40142cd977a4d4`  
		Last Modified: Thu, 23 Jun 2022 01:05:10 GMT  
		Size: 6.8 MB (6760409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e53ac4f7c306dbbff3ed6070a3e4bb1064345503f79625f8ba1fe206dd2cd3`  
		Last Modified: Thu, 23 Jun 2022 01:05:12 GMT  
		Size: 20.0 MB (20045624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d48cfd8d3ee5e2efa84bf652c47c516de588fb29f36a835a7b082dbcb905f7`  
		Last Modified: Thu, 23 Jun 2022 01:05:09 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f3849f106bcba131de9e8cd92bccedf13183beeb78ffa565ce73ffca7197fd`  
		Last Modified: Thu, 23 Jun 2022 01:05:09 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be8bc5cfad025ac058cc8ab54533a4d0b6c7057c7453000a98fd19a4c3380`  
		Last Modified: Thu, 23 Jun 2022 01:05:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a27c0cbaa413d31dab0a4217073f6153f8d9881ab1cb5d0dcfadd4c179098950
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e4ec0535f8f4e188f3cfda17b51b5f4165d4a48d17dd4154f318d548fba951`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:55:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sun, 29 May 2022 10:56:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:56:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:56:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:56:09 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:56:10 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:56:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:56:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a2187321b4fa5f3d4fc36a89db14d30a6c14bc705ed54f11a0c70a9a7f1aaa`  
		Last Modified: Sun, 29 May 2022 10:59:38 GMT  
		Size: 18.8 MB (18820986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767d837ef6cb92e710393907f4986d32cf436f4d346b3354d230ed25ad7ca59b`  
		Last Modified: Sun, 29 May 2022 10:59:26 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4987ac849dd128de031a98b494760cff7f4d15ceecf174f939a290628f7d3ac2`  
		Last Modified: Sun, 29 May 2022 10:59:25 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b57912442eff406b610500e2193c3b5ab692f444d9775f2ecab133053dc1064`  
		Last Modified: Sun, 29 May 2022 10:59:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f52ed2f2fab6d8f1293176b446884075d4a539f6f3d837d3f134b0b725d026d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45457259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17eca1164e22f0f5463188aeff9909238f9b12fa2e561a988003a9aff00c388b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:59 GMT
ADD file:c1bdac846ff41ceb56a44de5da778cfb7c3db7ccf4d689b7c1c22c0b80381c49 in / 
# Thu, 23 Jun 2022 00:42:59 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:27:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:27:20 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 23 Jun 2022 01:27:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:27:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:27:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:27:30 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:27:31 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:27:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:27:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:27:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:45f14b91a40fe8177f16f6b6526ada782d0d63a7958757d4e07c543e574ea7a8`  
		Last Modified: Thu, 23 Jun 2022 00:51:46 GMT  
		Size: 20.4 MB (20423990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba5c15f7bd5dfe32b1718aade52f008519a7ffa497114d413766119a3dbd4f8`  
		Last Modified: Thu, 23 Jun 2022 01:29:14 GMT  
		Size: 6.0 MB (6047312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2fe174fded1e6bbab973e46933621989f01d511bf87a681fdacb11bc0c6550`  
		Last Modified: Thu, 23 Jun 2022 01:29:16 GMT  
		Size: 19.0 MB (18961565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542933e37201dabb5bbe1daefc6274ffcf5b391a1e01ee8ba9b669b2b49acc16`  
		Last Modified: Thu, 23 Jun 2022 01:29:13 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c46645c7e500a2c98d858dae361ab37fb202595a64a3381f9101696d1cff8c`  
		Last Modified: Thu, 23 Jun 2022 01:29:13 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb68906a3c40e5c62b26804b2712777dd64b3276632378430815e626dbd09a5`  
		Last Modified: Thu, 23 Jun 2022 01:29:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:23417672f50b4d8e10c2afe16fb30256ea18d11c8b18476774bb7d582d31d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6f8f433011148165c541c6c2b5a4e5b6a0e17ed7a30e489da79572ffb65511b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14852447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7955bca787a43198659959f56224c8b4bcdcec4f04756f3179ed0041b6b3c97a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:16 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 05 Apr 2022 04:26:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:20 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:21 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:21 GMT
CMD ["chronograf"]
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
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec6a02657fcad83f14ccaebfe65596c725dc1a85062cc10c59315a08a6b4139`  
		Last Modified: Tue, 05 Apr 2022 04:27:21 GMT  
		Size: 11.7 MB (11737836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f48b6b7852557acd0c24a3412aff3571ae06abe1235cec3ae3c10d78c63a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216f28bcf9418aa7355c3934973e69b52e1bba48dd0e758a66049eaef57cbd96`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d36456c8c8f7725ba610682fd161c3b25b5bc41b4a3e2a9d384a197f9d65cc0`  
		Last Modified: Tue, 05 Apr 2022 04:27:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:1af53fbb3069147bf74eeeaaf17a4deba17a30474fa8642302e676aa6a784efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:70b667a17282f4759e22ccb3d92f003469ca1bf9b43e41cf8c6b88dc1ef43880
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49397889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd6c0f131d65571e79b70365992fc8bc78244fd1534cffeb16aa85db58fcddb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:20 GMT
ADD file:cfad5912b6dd7590713979e5a5e231b1b6873200fde725cb7baf75110d7fa138 in / 
# Thu, 23 Jun 2022 00:22:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:03:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:03:40 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 23 Jun 2022 01:03:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:03:48 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:03:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:03:48 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:03:49 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:03:49 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:03:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:03:49 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bff3e048017eab8adaed886bad4b3c5c81f7d952b65b056dca8d6dbc198222dd`  
		Last Modified: Thu, 23 Jun 2022 00:30:01 GMT  
		Size: 22.6 MB (22567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b5498e1d3acd0f9ff62393ea37f571882a0eec6680617ecb40142cd977a4d4`  
		Last Modified: Thu, 23 Jun 2022 01:05:10 GMT  
		Size: 6.8 MB (6760409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e53ac4f7c306dbbff3ed6070a3e4bb1064345503f79625f8ba1fe206dd2cd3`  
		Last Modified: Thu, 23 Jun 2022 01:05:12 GMT  
		Size: 20.0 MB (20045624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d48cfd8d3ee5e2efa84bf652c47c516de588fb29f36a835a7b082dbcb905f7`  
		Last Modified: Thu, 23 Jun 2022 01:05:09 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f3849f106bcba131de9e8cd92bccedf13183beeb78ffa565ce73ffca7197fd`  
		Last Modified: Thu, 23 Jun 2022 01:05:09 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be8bc5cfad025ac058cc8ab54533a4d0b6c7057c7453000a98fd19a4c3380`  
		Last Modified: Thu, 23 Jun 2022 01:05:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a27c0cbaa413d31dab0a4217073f6153f8d9881ab1cb5d0dcfadd4c179098950
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e4ec0535f8f4e188f3cfda17b51b5f4165d4a48d17dd4154f318d548fba951`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:55:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sun, 29 May 2022 10:56:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:56:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:56:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:56:09 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:56:10 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:56:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:56:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:56:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a2187321b4fa5f3d4fc36a89db14d30a6c14bc705ed54f11a0c70a9a7f1aaa`  
		Last Modified: Sun, 29 May 2022 10:59:38 GMT  
		Size: 18.8 MB (18820986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767d837ef6cb92e710393907f4986d32cf436f4d346b3354d230ed25ad7ca59b`  
		Last Modified: Sun, 29 May 2022 10:59:26 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4987ac849dd128de031a98b494760cff7f4d15ceecf174f939a290628f7d3ac2`  
		Last Modified: Sun, 29 May 2022 10:59:25 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b57912442eff406b610500e2193c3b5ab692f444d9775f2ecab133053dc1064`  
		Last Modified: Sun, 29 May 2022 10:59:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f52ed2f2fab6d8f1293176b446884075d4a539f6f3d837d3f134b0b725d026d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45457259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17eca1164e22f0f5463188aeff9909238f9b12fa2e561a988003a9aff00c388b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:59 GMT
ADD file:c1bdac846ff41ceb56a44de5da778cfb7c3db7ccf4d689b7c1c22c0b80381c49 in / 
# Thu, 23 Jun 2022 00:42:59 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:27:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:27:20 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 23 Jun 2022 01:27:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:27:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:27:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:27:30 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:27:31 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:27:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:27:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:27:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:45f14b91a40fe8177f16f6b6526ada782d0d63a7958757d4e07c543e574ea7a8`  
		Last Modified: Thu, 23 Jun 2022 00:51:46 GMT  
		Size: 20.4 MB (20423990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba5c15f7bd5dfe32b1718aade52f008519a7ffa497114d413766119a3dbd4f8`  
		Last Modified: Thu, 23 Jun 2022 01:29:14 GMT  
		Size: 6.0 MB (6047312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2fe174fded1e6bbab973e46933621989f01d511bf87a681fdacb11bc0c6550`  
		Last Modified: Thu, 23 Jun 2022 01:29:16 GMT  
		Size: 19.0 MB (18961565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542933e37201dabb5bbe1daefc6274ffcf5b391a1e01ee8ba9b669b2b49acc16`  
		Last Modified: Thu, 23 Jun 2022 01:29:13 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c46645c7e500a2c98d858dae361ab37fb202595a64a3381f9101696d1cff8c`  
		Last Modified: Thu, 23 Jun 2022 01:29:13 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb68906a3c40e5c62b26804b2712777dd64b3276632378430815e626dbd09a5`  
		Last Modified: Thu, 23 Jun 2022 01:29:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:23417672f50b4d8e10c2afe16fb30256ea18d11c8b18476774bb7d582d31d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6f8f433011148165c541c6c2b5a4e5b6a0e17ed7a30e489da79572ffb65511b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14852447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7955bca787a43198659959f56224c8b4bcdcec4f04756f3179ed0041b6b3c97a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:16 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 05 Apr 2022 04:26:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:20 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:21 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:21 GMT
CMD ["chronograf"]
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
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec6a02657fcad83f14ccaebfe65596c725dc1a85062cc10c59315a08a6b4139`  
		Last Modified: Tue, 05 Apr 2022 04:27:21 GMT  
		Size: 11.7 MB (11737836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f48b6b7852557acd0c24a3412aff3571ae06abe1235cec3ae3c10d78c63a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216f28bcf9418aa7355c3934973e69b52e1bba48dd0e758a66049eaef57cbd96`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d36456c8c8f7725ba610682fd161c3b25b5bc41b4a3e2a9d384a197f9d65cc0`  
		Last Modified: Tue, 05 Apr 2022 04:27:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:220f059603a102a0b68205a954bfb08bcab3b4d88b9a173987961cdf20dbf302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:c5cae25dce4df401c1c8f91b16c4caab3fc4fa19f6620b716e4d9fe8fed4e99f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f420e13fb6cec22c8d940263fcc76f69cf0f114af1998d310630ed38034f21b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:20 GMT
ADD file:cfad5912b6dd7590713979e5a5e231b1b6873200fde725cb7baf75110d7fa138 in / 
# Thu, 23 Jun 2022 00:22:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:04:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:04:03 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 23 Jun 2022 01:04:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:04:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:04:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:04:14 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:04:14 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:04:15 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:04:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:04:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bff3e048017eab8adaed886bad4b3c5c81f7d952b65b056dca8d6dbc198222dd`  
		Last Modified: Thu, 23 Jun 2022 00:30:01 GMT  
		Size: 22.6 MB (22567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f498f06d4ed9111864f2ab866f548535967b7a27356e24751b496239c5cd48`  
		Last Modified: Thu, 23 Jun 2022 01:05:23 GMT  
		Size: 4.5 MB (4506747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcdfa28a81d1b8e1e01f3559e494476d77efa27b677497075efea8937251e40`  
		Last Modified: Thu, 23 Jun 2022 01:05:28 GMT  
		Size: 38.3 MB (38328483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08cc1b0dfc1406fbf7318d2c168494aa8dd06ecde735e45faff3a9cf7836294`  
		Last Modified: Thu, 23 Jun 2022 01:05:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8995808b815f6b1ac983ee510f22df4c6edfc8521de517d0850234ba2d25a486`  
		Last Modified: Thu, 23 Jun 2022 01:05:23 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2be6170b31a796c94d1f4c620cd8e03aed67489d41ef7bc7737d118ed303078`  
		Last Modified: Thu, 23 Jun 2022 01:05:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3ab9c3ae4dbe93d0c68b2b13a6f5f1a6693eb318c8ef96d429a0ea95931012fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59047797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710d8146a656c6b6260367fdbfe3c7ab297bc0818936a6852aec4166c31e5753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:56:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:56:45 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sun, 29 May 2022 10:57:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:57:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:57:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:57:17 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:57:17 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:57:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:57:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:57:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be570855153de9294811361809dbf8420e01f00470116c7f002ef9e8428ef71f`  
		Last Modified: Sun, 29 May 2022 10:59:51 GMT  
		Size: 3.9 MB (3880111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e9c5c6e4c4643ac7a75a35d35080940f4dde2c6372b4de4a7745bd416b32c2`  
		Last Modified: Sun, 29 May 2022 11:00:09 GMT  
		Size: 35.8 MB (35783472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50aff1f4d8cf55ec3328e89533e93a50fa6d37466aecbe52bfbd6ff8ba527d1`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebaf2e61cba1434d8eae96da6e40f1adeb21e55401ffed7af372e4bcbbb9ba`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13de0aaa586114a36f64e0985b4bb3f8c2af13d6f745bea44cb13c415d2fb1b2`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8d166be109cff4bf91830a92c5f923c96adbaafa124065f43ef32ffee0fd1eb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8e02065a47aeb30163b563e0c4c31efe9a9ee4e060dd635f83029f757b1b8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:59 GMT
ADD file:c1bdac846ff41ceb56a44de5da778cfb7c3db7ccf4d689b7c1c22c0b80381c49 in / 
# Thu, 23 Jun 2022 00:42:59 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:27:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:27:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 23 Jun 2022 01:27:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:28:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:28:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:28:01 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:28:02 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:28:04 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:28:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:45f14b91a40fe8177f16f6b6526ada782d0d63a7958757d4e07c543e574ea7a8`  
		Last Modified: Thu, 23 Jun 2022 00:51:46 GMT  
		Size: 20.4 MB (20423990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac8b9598caa4b3c56f37f213c384246bc7d1f7af45b3322d773660d9bf5de4f`  
		Last Modified: Thu, 23 Jun 2022 01:29:28 GMT  
		Size: 3.9 MB (3893941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5426d04d01602e2f8b696af6b30401fb6fd4138203bf457189063bcdb3c733`  
		Last Modified: Thu, 23 Jun 2022 01:29:32 GMT  
		Size: 36.0 MB (35986784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67971835240decaa81a59fa355c46e2788fe76785c7acbea4f72ca41d65414f1`  
		Last Modified: Thu, 23 Jun 2022 01:29:28 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcb2163bc786a80e47d18b390e3bff9bd2abb60b9957002a2048ce6cd36ef67`  
		Last Modified: Thu, 23 Jun 2022 01:29:28 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef11897af2ff779b380dc88b7350055a885ef55b11dd72b504f87d627c1b7e2`  
		Last Modified: Thu, 23 Jun 2022 01:29:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:990421b8bc9b5dd6d472bd68efb5b165bf5f909c1b4a841756198933b14513d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:386f11aba61ccd79dd3d8105edce283d4eac402a7c92b802beb7ad89cf3136a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22670798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c75f57862ead544bf92efebf86f59028a171990d14514c9cc621d7807042a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:26 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 05 Apr 2022 04:26:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:31 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:32 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:32 GMT
CMD ["chronograf"]
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
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8ba42ef9e34fc8eb0a6b88a3cd9242247e7029eaaed6b3d13f3f77eba9bb4f`  
		Last Modified: Tue, 05 Apr 2022 04:27:35 GMT  
		Size: 19.6 MB (19556196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e98e5f05434dd7e69e4acfb1c9682f93ab2c0d204b09dac76ccbc8fac82952`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12636f40cb960e763e7c41f0b801007ade339c74aac79418124da7df48f27a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7c964b7b93ca840cc02a49bcee2e824dccd67e40f48c0d16b239cc3b3e2be1`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:220f059603a102a0b68205a954bfb08bcab3b4d88b9a173987961cdf20dbf302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:c5cae25dce4df401c1c8f91b16c4caab3fc4fa19f6620b716e4d9fe8fed4e99f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f420e13fb6cec22c8d940263fcc76f69cf0f114af1998d310630ed38034f21b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:20 GMT
ADD file:cfad5912b6dd7590713979e5a5e231b1b6873200fde725cb7baf75110d7fa138 in / 
# Thu, 23 Jun 2022 00:22:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:04:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:04:03 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 23 Jun 2022 01:04:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:04:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:04:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:04:14 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:04:14 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:04:15 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:04:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:04:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bff3e048017eab8adaed886bad4b3c5c81f7d952b65b056dca8d6dbc198222dd`  
		Last Modified: Thu, 23 Jun 2022 00:30:01 GMT  
		Size: 22.6 MB (22567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f498f06d4ed9111864f2ab866f548535967b7a27356e24751b496239c5cd48`  
		Last Modified: Thu, 23 Jun 2022 01:05:23 GMT  
		Size: 4.5 MB (4506747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcdfa28a81d1b8e1e01f3559e494476d77efa27b677497075efea8937251e40`  
		Last Modified: Thu, 23 Jun 2022 01:05:28 GMT  
		Size: 38.3 MB (38328483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08cc1b0dfc1406fbf7318d2c168494aa8dd06ecde735e45faff3a9cf7836294`  
		Last Modified: Thu, 23 Jun 2022 01:05:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8995808b815f6b1ac983ee510f22df4c6edfc8521de517d0850234ba2d25a486`  
		Last Modified: Thu, 23 Jun 2022 01:05:23 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2be6170b31a796c94d1f4c620cd8e03aed67489d41ef7bc7737d118ed303078`  
		Last Modified: Thu, 23 Jun 2022 01:05:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3ab9c3ae4dbe93d0c68b2b13a6f5f1a6693eb318c8ef96d429a0ea95931012fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59047797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710d8146a656c6b6260367fdbfe3c7ab297bc0818936a6852aec4166c31e5753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:56:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:56:45 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sun, 29 May 2022 10:57:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:57:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:57:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:57:17 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:57:17 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:57:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:57:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:57:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be570855153de9294811361809dbf8420e01f00470116c7f002ef9e8428ef71f`  
		Last Modified: Sun, 29 May 2022 10:59:51 GMT  
		Size: 3.9 MB (3880111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e9c5c6e4c4643ac7a75a35d35080940f4dde2c6372b4de4a7745bd416b32c2`  
		Last Modified: Sun, 29 May 2022 11:00:09 GMT  
		Size: 35.8 MB (35783472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50aff1f4d8cf55ec3328e89533e93a50fa6d37466aecbe52bfbd6ff8ba527d1`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebaf2e61cba1434d8eae96da6e40f1adeb21e55401ffed7af372e4bcbbb9ba`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13de0aaa586114a36f64e0985b4bb3f8c2af13d6f745bea44cb13c415d2fb1b2`  
		Last Modified: Sun, 29 May 2022 10:59:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8d166be109cff4bf91830a92c5f923c96adbaafa124065f43ef32ffee0fd1eb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8e02065a47aeb30163b563e0c4c31efe9a9ee4e060dd635f83029f757b1b8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:59 GMT
ADD file:c1bdac846ff41ceb56a44de5da778cfb7c3db7ccf4d689b7c1c22c0b80381c49 in / 
# Thu, 23 Jun 2022 00:42:59 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:27:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:27:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 23 Jun 2022 01:27:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:28:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:28:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:28:01 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:28:02 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:28:04 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:28:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:45f14b91a40fe8177f16f6b6526ada782d0d63a7958757d4e07c543e574ea7a8`  
		Last Modified: Thu, 23 Jun 2022 00:51:46 GMT  
		Size: 20.4 MB (20423990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac8b9598caa4b3c56f37f213c384246bc7d1f7af45b3322d773660d9bf5de4f`  
		Last Modified: Thu, 23 Jun 2022 01:29:28 GMT  
		Size: 3.9 MB (3893941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5426d04d01602e2f8b696af6b30401fb6fd4138203bf457189063bcdb3c733`  
		Last Modified: Thu, 23 Jun 2022 01:29:32 GMT  
		Size: 36.0 MB (35986784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67971835240decaa81a59fa355c46e2788fe76785c7acbea4f72ca41d65414f1`  
		Last Modified: Thu, 23 Jun 2022 01:29:28 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcb2163bc786a80e47d18b390e3bff9bd2abb60b9957002a2048ce6cd36ef67`  
		Last Modified: Thu, 23 Jun 2022 01:29:28 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef11897af2ff779b380dc88b7350055a885ef55b11dd72b504f87d627c1b7e2`  
		Last Modified: Thu, 23 Jun 2022 01:29:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:990421b8bc9b5dd6d472bd68efb5b165bf5f909c1b4a841756198933b14513d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:386f11aba61ccd79dd3d8105edce283d4eac402a7c92b802beb7ad89cf3136a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22670798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c75f57862ead544bf92efebf86f59028a171990d14514c9cc621d7807042a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:26 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 05 Apr 2022 04:26:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:31 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:32 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:32 GMT
CMD ["chronograf"]
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
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8ba42ef9e34fc8eb0a6b88a3cd9242247e7029eaaed6b3d13f3f77eba9bb4f`  
		Last Modified: Tue, 05 Apr 2022 04:27:35 GMT  
		Size: 19.6 MB (19556196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e98e5f05434dd7e69e4acfb1c9682f93ab2c0d204b09dac76ccbc8fac82952`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12636f40cb960e763e7c41f0b801007ade339c74aac79418124da7df48f27a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7c964b7b93ca840cc02a49bcee2e824dccd67e40f48c0d16b239cc3b3e2be1`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:0d47744b345fe442c15feb15de4ae39666d5b24957ce5b96eaab46b4c9fecbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:63caf9f0f528e26b71300621aaf5e006d1db4320f0611c9de314deef1b29da7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66278888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd374f64eac84b9357bda804cee1d8c976d03532a09dbaed36744c6bb58dba11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:20 GMT
ADD file:cfad5912b6dd7590713979e5a5e231b1b6873200fde725cb7baf75110d7fa138 in / 
# Thu, 23 Jun 2022 00:22:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:03:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:04:21 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 23 Jun 2022 01:04:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:04:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:04:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:04:30 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:04:30 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:04:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:04:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:04:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bff3e048017eab8adaed886bad4b3c5c81f7d952b65b056dca8d6dbc198222dd`  
		Last Modified: Thu, 23 Jun 2022 00:30:01 GMT  
		Size: 22.6 MB (22567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b5498e1d3acd0f9ff62393ea37f571882a0eec6680617ecb40142cd977a4d4`  
		Last Modified: Thu, 23 Jun 2022 01:05:10 GMT  
		Size: 6.8 MB (6760409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571224894ea1d72616a619e9884699ec937cf0611294c58271749705282eb42`  
		Last Modified: Thu, 23 Jun 2022 01:05:44 GMT  
		Size: 36.9 MB (36926628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80abaef4bc317c3286ed790449ac193fc9593858ba90d3172992d734f8868f2f`  
		Last Modified: Thu, 23 Jun 2022 01:05:39 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d28eeb4e3f820fa4c1809d2bdb2ef78bdef4edf847c63dbfeaef74592f70799`  
		Last Modified: Thu, 23 Jun 2022 01:05:39 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e36896bec5c1d1566f204be387023e292e163d8abe950865c11a8e8fb6870aa`  
		Last Modified: Thu, 23 Jun 2022 01:05:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9ec0fca2836243cd7e7abd7d91f0465501bf87596c3b6d8482ca3cfcf18e6e7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59677074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2a75af0bb3fb2c325af4810fa40d8d240a2668c567de0ed6b73782a5321ebb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:57:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sun, 29 May 2022 10:57:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:57:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:57:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:57:59 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:57:59 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f14c826331b3b2a0e3043566e5772143c4f83fc4390794920fb3f01e3babc2`  
		Last Modified: Sun, 29 May 2022 11:00:38 GMT  
		Size: 34.5 MB (34511923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a134a1318b6432dc1727dfe33e397408cb8d0df0d46154780d048760482aec`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ead8c2fb766463e52625a816b0ed0174a76a8be377cebf594520b8fe74edd`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b75dff010c7ee6697b5b21fa5ef81c730ad02e409fe440ae8b064884fc801d`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c604e20e46ed81d4e09f3138a1e5558ae6df6eda8e5d1ff0b89d62f116e9b7b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60927292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eceadb48d0f5d4f735bc6a8c9573e4414903782ef6d731d7b1598c4ab2a56d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:59 GMT
ADD file:c1bdac846ff41ceb56a44de5da778cfb7c3db7ccf4d689b7c1c22c0b80381c49 in / 
# Thu, 23 Jun 2022 00:42:59 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:27:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:28:10 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 23 Jun 2022 01:28:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:28:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:28:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:28:21 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:28:22 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:28:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:28:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:45f14b91a40fe8177f16f6b6526ada782d0d63a7958757d4e07c543e574ea7a8`  
		Last Modified: Thu, 23 Jun 2022 00:51:46 GMT  
		Size: 20.4 MB (20423990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba5c15f7bd5dfe32b1718aade52f008519a7ffa497114d413766119a3dbd4f8`  
		Last Modified: Thu, 23 Jun 2022 01:29:14 GMT  
		Size: 6.0 MB (6047312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c1a8cb2336b85ea9a994dbce5e4a24a55bf674f2f99de4d6ace760d7500e69`  
		Last Modified: Thu, 23 Jun 2022 01:29:48 GMT  
		Size: 34.4 MB (34431598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c15f181ea0049ba7b848851ca06b65650fd20f80fe36b50d2539cdc744d8386`  
		Last Modified: Thu, 23 Jun 2022 01:29:43 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbaa4b067e7757a8dfbd975c1a6e477396433d160f700e17652803c8c50fc2b`  
		Last Modified: Thu, 23 Jun 2022 01:29:43 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbab753cfbe0ef9907ea289d72732370b4ca5cd6b650c1a85f992af3ef56bd9`  
		Last Modified: Thu, 23 Jun 2022 01:29:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:d3e3bbce6ab55cead013b905eba19cdd95cc418e5f2acfb421159ccc1bf8cbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b28beb85949241c005e5be21181999ce565e4b29dd96295f7e2f7d8ff833a80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22318581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb7b4f19d3448b5e558e8d6e7857db12751a4b8a0928e3f0fa36efaa296650b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 05 Apr 2022 04:26:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:43 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:43 GMT
CMD ["chronograf"]
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
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e780df476439b3a8749d6d1ec5009124d7cb47b7328d520390e5c1df5e5260f7`  
		Last Modified: Tue, 05 Apr 2022 04:27:49 GMT  
		Size: 19.2 MB (19203976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770779eb24c794631aa560ebb5145f2fd7a4bf2972a43459d9321581fc47084e`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1701788eafedc43dca0570322f1ab0c00388a8d9a882173a472e4cc23774b`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eec10863e13223024d57ee99337a425873b97b7b2829d8f207c267a414b201`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:0d47744b345fe442c15feb15de4ae39666d5b24957ce5b96eaab46b4c9fecbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:63caf9f0f528e26b71300621aaf5e006d1db4320f0611c9de314deef1b29da7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66278888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd374f64eac84b9357bda804cee1d8c976d03532a09dbaed36744c6bb58dba11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:20 GMT
ADD file:cfad5912b6dd7590713979e5a5e231b1b6873200fde725cb7baf75110d7fa138 in / 
# Thu, 23 Jun 2022 00:22:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:03:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:04:21 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 23 Jun 2022 01:04:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:04:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:04:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:04:30 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:04:30 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:04:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:04:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:04:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bff3e048017eab8adaed886bad4b3c5c81f7d952b65b056dca8d6dbc198222dd`  
		Last Modified: Thu, 23 Jun 2022 00:30:01 GMT  
		Size: 22.6 MB (22567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b5498e1d3acd0f9ff62393ea37f571882a0eec6680617ecb40142cd977a4d4`  
		Last Modified: Thu, 23 Jun 2022 01:05:10 GMT  
		Size: 6.8 MB (6760409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571224894ea1d72616a619e9884699ec937cf0611294c58271749705282eb42`  
		Last Modified: Thu, 23 Jun 2022 01:05:44 GMT  
		Size: 36.9 MB (36926628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80abaef4bc317c3286ed790449ac193fc9593858ba90d3172992d734f8868f2f`  
		Last Modified: Thu, 23 Jun 2022 01:05:39 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d28eeb4e3f820fa4c1809d2bdb2ef78bdef4edf847c63dbfeaef74592f70799`  
		Last Modified: Thu, 23 Jun 2022 01:05:39 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e36896bec5c1d1566f204be387023e292e163d8abe950865c11a8e8fb6870aa`  
		Last Modified: Thu, 23 Jun 2022 01:05:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9ec0fca2836243cd7e7abd7d91f0465501bf87596c3b6d8482ca3cfcf18e6e7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59677074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2a75af0bb3fb2c325af4810fa40d8d240a2668c567de0ed6b73782a5321ebb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:57:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sun, 29 May 2022 10:57:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:57:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:57:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:57:59 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:57:59 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f14c826331b3b2a0e3043566e5772143c4f83fc4390794920fb3f01e3babc2`  
		Last Modified: Sun, 29 May 2022 11:00:38 GMT  
		Size: 34.5 MB (34511923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a134a1318b6432dc1727dfe33e397408cb8d0df0d46154780d048760482aec`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ead8c2fb766463e52625a816b0ed0174a76a8be377cebf594520b8fe74edd`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b75dff010c7ee6697b5b21fa5ef81c730ad02e409fe440ae8b064884fc801d`  
		Last Modified: Sun, 29 May 2022 11:00:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c604e20e46ed81d4e09f3138a1e5558ae6df6eda8e5d1ff0b89d62f116e9b7b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60927292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eceadb48d0f5d4f735bc6a8c9573e4414903782ef6d731d7b1598c4ab2a56d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:59 GMT
ADD file:c1bdac846ff41ceb56a44de5da778cfb7c3db7ccf4d689b7c1c22c0b80381c49 in / 
# Thu, 23 Jun 2022 00:42:59 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:27:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:28:10 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 23 Jun 2022 01:28:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:28:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:28:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:28:21 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:28:22 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:28:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:28:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:45f14b91a40fe8177f16f6b6526ada782d0d63a7958757d4e07c543e574ea7a8`  
		Last Modified: Thu, 23 Jun 2022 00:51:46 GMT  
		Size: 20.4 MB (20423990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba5c15f7bd5dfe32b1718aade52f008519a7ffa497114d413766119a3dbd4f8`  
		Last Modified: Thu, 23 Jun 2022 01:29:14 GMT  
		Size: 6.0 MB (6047312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c1a8cb2336b85ea9a994dbce5e4a24a55bf674f2f99de4d6ace760d7500e69`  
		Last Modified: Thu, 23 Jun 2022 01:29:48 GMT  
		Size: 34.4 MB (34431598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c15f181ea0049ba7b848851ca06b65650fd20f80fe36b50d2539cdc744d8386`  
		Last Modified: Thu, 23 Jun 2022 01:29:43 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbaa4b067e7757a8dfbd975c1a6e477396433d160f700e17652803c8c50fc2b`  
		Last Modified: Thu, 23 Jun 2022 01:29:43 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbab753cfbe0ef9907ea289d72732370b4ca5cd6b650c1a85f992af3ef56bd9`  
		Last Modified: Thu, 23 Jun 2022 01:29:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:d3e3bbce6ab55cead013b905eba19cdd95cc418e5f2acfb421159ccc1bf8cbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b28beb85949241c005e5be21181999ce565e4b29dd96295f7e2f7d8ff833a80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22318581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb7b4f19d3448b5e558e8d6e7857db12751a4b8a0928e3f0fa36efaa296650b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 05 Apr 2022 04:26:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:43 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:43 GMT
CMD ["chronograf"]
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
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e780df476439b3a8749d6d1ec5009124d7cb47b7328d520390e5c1df5e5260f7`  
		Last Modified: Tue, 05 Apr 2022 04:27:49 GMT  
		Size: 19.2 MB (19203976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770779eb24c794631aa560ebb5145f2fd7a4bf2972a43459d9321581fc47084e`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1701788eafedc43dca0570322f1ab0c00388a8d9a882173a472e4cc23774b`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eec10863e13223024d57ee99337a425873b97b7b2829d8f207c267a414b201`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:b0fde4588fe9939d31fc2a69facc676eca838d7e6beb87dfb33c28dea9290896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:f17e9512b8d3019b3e7304a27104b93e804ca748b4b7ae6bf70fe6e8eb670dbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfe22ae70d4b13903558a6a9361bb8987c312e7ffb6eff9b993a83bfc1fa29c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:20 GMT
ADD file:cfad5912b6dd7590713979e5a5e231b1b6873200fde725cb7baf75110d7fa138 in / 
# Thu, 23 Jun 2022 00:22:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:03:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:04:34 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Jun 2022 01:04:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:04:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:04:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:04:44 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:04:44 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:04:44 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:04:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:04:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bff3e048017eab8adaed886bad4b3c5c81f7d952b65b056dca8d6dbc198222dd`  
		Last Modified: Thu, 23 Jun 2022 00:30:01 GMT  
		Size: 22.6 MB (22567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b5498e1d3acd0f9ff62393ea37f571882a0eec6680617ecb40142cd977a4d4`  
		Last Modified: Thu, 23 Jun 2022 01:05:10 GMT  
		Size: 6.8 MB (6760409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa682df4ed7265161d790b536e4d0c183299a4d68fb350df760037392c48cae`  
		Last Modified: Thu, 23 Jun 2022 01:05:59 GMT  
		Size: 37.6 MB (37570412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64122926f1c38ece9730eb059c7a59bfbf86dca2e952162b527012d9b3ed7f1`  
		Last Modified: Thu, 23 Jun 2022 01:05:54 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e912b66168d1ebc8e41b42c475e211579caa5bcb17cc5bb033fb89b6d2a77c4b`  
		Last Modified: Thu, 23 Jun 2022 01:05:54 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059c52a2c8401210a0c468e477ad83f5a23cea31ea7fb6064ab631ab296af992`  
		Last Modified: Thu, 23 Jun 2022 01:05:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:91792d93db64802b69b8550319078ecd42dd7af182f1fbb9a145f1d20e606743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1891d59a62b2ba570f788d9d27aeab62f92c6563eeeb70f6ec610214c0ae07c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sun, 29 May 2022 10:58:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:58:34 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:58:34 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b381ef66ac88214907ef3be818d7b4dcbb3a61bccc080616900e4ed66ea8187`  
		Last Modified: Sun, 29 May 2022 11:01:08 GMT  
		Size: 35.3 MB (35291426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bae757276901132b7c6f04689b796e75800914327608c507a8a8ea435f9482`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6e25a9bf1a83179b4080db85af01b6aae433301906a10261e0dd8748fda3e`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b559a4d6864b3e1599e4207a2c01cc2014d7b5e895ee3ca48b77dbf144aedc`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d5dfa6b4fc06d5183c2fffc72832fe0aeadecb2fac2a02adb08592f924fe47d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6515bd8a31c397aec3531e07859da02f7b6e487896be7f6c2e0af789d214eaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:59 GMT
ADD file:c1bdac846ff41ceb56a44de5da778cfb7c3db7ccf4d689b7c1c22c0b80381c49 in / 
# Thu, 23 Jun 2022 00:42:59 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:27:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:28:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Jun 2022 01:28:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:28:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:28:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:28:43 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:28:44 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:28:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:28:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:28:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:45f14b91a40fe8177f16f6b6526ada782d0d63a7958757d4e07c543e574ea7a8`  
		Last Modified: Thu, 23 Jun 2022 00:51:46 GMT  
		Size: 20.4 MB (20423990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba5c15f7bd5dfe32b1718aade52f008519a7ffa497114d413766119a3dbd4f8`  
		Last Modified: Thu, 23 Jun 2022 01:29:14 GMT  
		Size: 6.0 MB (6047312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35008848465d6270ff38da08a7514053d62632985429e2326581b33946d6761b`  
		Last Modified: Thu, 23 Jun 2022 01:30:04 GMT  
		Size: 35.2 MB (35174017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75069e610add6e199c1abfd85f6596a3f7e15bc912230ddb1e0cdab0b41d71d`  
		Last Modified: Thu, 23 Jun 2022 01:29:59 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cdbd4a0e6503bdb63b1ce28ad92eeb99798ed8df1d1cf91cf4b53eabb8b192`  
		Last Modified: Thu, 23 Jun 2022 01:29:59 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6cb9709f043f81dc4d6f60f562a1d82615eb06ff08d1d6ed5544c34ad0fea3`  
		Last Modified: Thu, 23 Jun 2022 01:29:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:64529a79e1f42f21063f77e88d3b17a66dd5fe12b361ba459a496564f60deae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:617112048d88886c7c56a0298d5022925bf60cea583bf42950f85da0b1543c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f641fefba39a03a8fb9f9a028aeeecec9f62c81b6a89da22334192b42afee733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 05 Apr 2022 04:26:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:55 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:56 GMT
CMD ["chronograf"]
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
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048cd652ea5c71fdf0fb436e4b84f533bce10501e6f8f75b34a3f5499ec3bc`  
		Last Modified: Tue, 05 Apr 2022 04:28:03 GMT  
		Size: 19.7 MB (19672143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafdf6394d7dc10583226357da386688d2d1aa89d90e9d6c3e02d059d1ff7a0`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9df35e5b1a70215f7fa195a06d17ece074a61ec14d91da8c065c6f5426b8bc`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eab2c8d98b5fdc4d6ed0e531c9766afacad54ccd952085aa98da4d57c5519a`  
		Last Modified: Tue, 05 Apr 2022 04:28:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:b0fde4588fe9939d31fc2a69facc676eca838d7e6beb87dfb33c28dea9290896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:f17e9512b8d3019b3e7304a27104b93e804ca748b4b7ae6bf70fe6e8eb670dbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfe22ae70d4b13903558a6a9361bb8987c312e7ffb6eff9b993a83bfc1fa29c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:20 GMT
ADD file:cfad5912b6dd7590713979e5a5e231b1b6873200fde725cb7baf75110d7fa138 in / 
# Thu, 23 Jun 2022 00:22:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:03:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:04:34 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Jun 2022 01:04:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:04:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:04:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:04:44 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:04:44 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:04:44 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:04:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:04:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bff3e048017eab8adaed886bad4b3c5c81f7d952b65b056dca8d6dbc198222dd`  
		Last Modified: Thu, 23 Jun 2022 00:30:01 GMT  
		Size: 22.6 MB (22567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b5498e1d3acd0f9ff62393ea37f571882a0eec6680617ecb40142cd977a4d4`  
		Last Modified: Thu, 23 Jun 2022 01:05:10 GMT  
		Size: 6.8 MB (6760409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa682df4ed7265161d790b536e4d0c183299a4d68fb350df760037392c48cae`  
		Last Modified: Thu, 23 Jun 2022 01:05:59 GMT  
		Size: 37.6 MB (37570412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64122926f1c38ece9730eb059c7a59bfbf86dca2e952162b527012d9b3ed7f1`  
		Last Modified: Thu, 23 Jun 2022 01:05:54 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e912b66168d1ebc8e41b42c475e211579caa5bcb17cc5bb033fb89b6d2a77c4b`  
		Last Modified: Thu, 23 Jun 2022 01:05:54 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059c52a2c8401210a0c468e477ad83f5a23cea31ea7fb6064ab631ab296af992`  
		Last Modified: Thu, 23 Jun 2022 01:05:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:91792d93db64802b69b8550319078ecd42dd7af182f1fbb9a145f1d20e606743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1891d59a62b2ba570f788d9d27aeab62f92c6563eeeb70f6ec610214c0ae07c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sun, 29 May 2022 10:58:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:58:34 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:58:34 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b381ef66ac88214907ef3be818d7b4dcbb3a61bccc080616900e4ed66ea8187`  
		Last Modified: Sun, 29 May 2022 11:01:08 GMT  
		Size: 35.3 MB (35291426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bae757276901132b7c6f04689b796e75800914327608c507a8a8ea435f9482`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6e25a9bf1a83179b4080db85af01b6aae433301906a10261e0dd8748fda3e`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b559a4d6864b3e1599e4207a2c01cc2014d7b5e895ee3ca48b77dbf144aedc`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d5dfa6b4fc06d5183c2fffc72832fe0aeadecb2fac2a02adb08592f924fe47d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6515bd8a31c397aec3531e07859da02f7b6e487896be7f6c2e0af789d214eaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:59 GMT
ADD file:c1bdac846ff41ceb56a44de5da778cfb7c3db7ccf4d689b7c1c22c0b80381c49 in / 
# Thu, 23 Jun 2022 00:42:59 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:27:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:28:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Jun 2022 01:28:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:28:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:28:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:28:43 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:28:44 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:28:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:28:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:28:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:45f14b91a40fe8177f16f6b6526ada782d0d63a7958757d4e07c543e574ea7a8`  
		Last Modified: Thu, 23 Jun 2022 00:51:46 GMT  
		Size: 20.4 MB (20423990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba5c15f7bd5dfe32b1718aade52f008519a7ffa497114d413766119a3dbd4f8`  
		Last Modified: Thu, 23 Jun 2022 01:29:14 GMT  
		Size: 6.0 MB (6047312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35008848465d6270ff38da08a7514053d62632985429e2326581b33946d6761b`  
		Last Modified: Thu, 23 Jun 2022 01:30:04 GMT  
		Size: 35.2 MB (35174017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75069e610add6e199c1abfd85f6596a3f7e15bc912230ddb1e0cdab0b41d71d`  
		Last Modified: Thu, 23 Jun 2022 01:29:59 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cdbd4a0e6503bdb63b1ce28ad92eeb99798ed8df1d1cf91cf4b53eabb8b192`  
		Last Modified: Thu, 23 Jun 2022 01:29:59 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6cb9709f043f81dc4d6f60f562a1d82615eb06ff08d1d6ed5544c34ad0fea3`  
		Last Modified: Thu, 23 Jun 2022 01:29:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:64529a79e1f42f21063f77e88d3b17a66dd5fe12b361ba459a496564f60deae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:617112048d88886c7c56a0298d5022925bf60cea583bf42950f85da0b1543c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f641fefba39a03a8fb9f9a028aeeecec9f62c81b6a89da22334192b42afee733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 05 Apr 2022 04:26:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:55 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:56 GMT
CMD ["chronograf"]
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
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048cd652ea5c71fdf0fb436e4b84f533bce10501e6f8f75b34a3f5499ec3bc`  
		Last Modified: Tue, 05 Apr 2022 04:28:03 GMT  
		Size: 19.7 MB (19672143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafdf6394d7dc10583226357da386688d2d1aa89d90e9d6c3e02d059d1ff7a0`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9df35e5b1a70215f7fa195a06d17ece074a61ec14d91da8c065c6f5426b8bc`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eab2c8d98b5fdc4d6ed0e531c9766afacad54ccd952085aa98da4d57c5519a`  
		Last Modified: Tue, 05 Apr 2022 04:28:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:64529a79e1f42f21063f77e88d3b17a66dd5fe12b361ba459a496564f60deae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:617112048d88886c7c56a0298d5022925bf60cea583bf42950f85da0b1543c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f641fefba39a03a8fb9f9a028aeeecec9f62c81b6a89da22334192b42afee733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 05 Apr 2022 04:26:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:55 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:56 GMT
CMD ["chronograf"]
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
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048cd652ea5c71fdf0fb436e4b84f533bce10501e6f8f75b34a3f5499ec3bc`  
		Last Modified: Tue, 05 Apr 2022 04:28:03 GMT  
		Size: 19.7 MB (19672143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafdf6394d7dc10583226357da386688d2d1aa89d90e9d6c3e02d059d1ff7a0`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9df35e5b1a70215f7fa195a06d17ece074a61ec14d91da8c065c6f5426b8bc`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eab2c8d98b5fdc4d6ed0e531c9766afacad54ccd952085aa98da4d57c5519a`  
		Last Modified: Tue, 05 Apr 2022 04:28:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:b0fde4588fe9939d31fc2a69facc676eca838d7e6beb87dfb33c28dea9290896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:f17e9512b8d3019b3e7304a27104b93e804ca748b4b7ae6bf70fe6e8eb670dbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfe22ae70d4b13903558a6a9361bb8987c312e7ffb6eff9b993a83bfc1fa29c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:20 GMT
ADD file:cfad5912b6dd7590713979e5a5e231b1b6873200fde725cb7baf75110d7fa138 in / 
# Thu, 23 Jun 2022 00:22:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:03:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:04:34 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Jun 2022 01:04:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:04:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:04:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:04:44 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:04:44 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:04:44 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:04:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:04:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bff3e048017eab8adaed886bad4b3c5c81f7d952b65b056dca8d6dbc198222dd`  
		Last Modified: Thu, 23 Jun 2022 00:30:01 GMT  
		Size: 22.6 MB (22567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b5498e1d3acd0f9ff62393ea37f571882a0eec6680617ecb40142cd977a4d4`  
		Last Modified: Thu, 23 Jun 2022 01:05:10 GMT  
		Size: 6.8 MB (6760409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa682df4ed7265161d790b536e4d0c183299a4d68fb350df760037392c48cae`  
		Last Modified: Thu, 23 Jun 2022 01:05:59 GMT  
		Size: 37.6 MB (37570412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64122926f1c38ece9730eb059c7a59bfbf86dca2e952162b527012d9b3ed7f1`  
		Last Modified: Thu, 23 Jun 2022 01:05:54 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e912b66168d1ebc8e41b42c475e211579caa5bcb17cc5bb033fb89b6d2a77c4b`  
		Last Modified: Thu, 23 Jun 2022 01:05:54 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059c52a2c8401210a0c468e477ad83f5a23cea31ea7fb6064ab631ab296af992`  
		Last Modified: Thu, 23 Jun 2022 01:05:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:91792d93db64802b69b8550319078ecd42dd7af182f1fbb9a145f1d20e606743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1891d59a62b2ba570f788d9d27aeab62f92c6563eeeb70f6ec610214c0ae07c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 May 2022 01:05:51 GMT
ADD file:4dd5baef6913cbeaba8b4abeb9fa3860736e9c421334170bf9a435f002176781 in / 
# Sat, 28 May 2022 01:05:52 GMT
CMD ["bash"]
# Sun, 29 May 2022 10:55:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 10:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sun, 29 May 2022 10:58:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 29 May 2022 10:58:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 29 May 2022 10:58:34 GMT
EXPOSE 8888
# Sun, 29 May 2022 10:58:34 GMT
VOLUME [/var/lib/chronograf]
# Sun, 29 May 2022 10:58:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 29 May 2022 10:58:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 10:58:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1bc9eb7248815be774e7f369470fa41493ff76db8a85f10e545b1538909d9d7`  
		Last Modified: Sat, 28 May 2022 01:22:13 GMT  
		Size: 19.4 MB (19359814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119ba187328a107b9db1a52f6838ddab5d6c6b8647c5dcff3fa9af4baf486a4`  
		Last Modified: Sun, 29 May 2022 10:59:28 GMT  
		Size: 5.8 MB (5780942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b381ef66ac88214907ef3be818d7b4dcbb3a61bccc080616900e4ed66ea8187`  
		Last Modified: Sun, 29 May 2022 11:01:08 GMT  
		Size: 35.3 MB (35291426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bae757276901132b7c6f04689b796e75800914327608c507a8a8ea435f9482`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6e25a9bf1a83179b4080db85af01b6aae433301906a10261e0dd8748fda3e`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b559a4d6864b3e1599e4207a2c01cc2014d7b5e895ee3ca48b77dbf144aedc`  
		Last Modified: Sun, 29 May 2022 11:00:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d5dfa6b4fc06d5183c2fffc72832fe0aeadecb2fac2a02adb08592f924fe47d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6515bd8a31c397aec3531e07859da02f7b6e487896be7f6c2e0af789d214eaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:59 GMT
ADD file:c1bdac846ff41ceb56a44de5da778cfb7c3db7ccf4d689b7c1c22c0b80381c49 in / 
# Thu, 23 Jun 2022 00:42:59 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:27:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 01:28:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Jun 2022 01:28:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Jun 2022 01:28:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Jun 2022 01:28:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Jun 2022 01:28:43 GMT
EXPOSE 8888
# Thu, 23 Jun 2022 01:28:44 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Jun 2022 01:28:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Jun 2022 01:28:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 01:28:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:45f14b91a40fe8177f16f6b6526ada782d0d63a7958757d4e07c543e574ea7a8`  
		Last Modified: Thu, 23 Jun 2022 00:51:46 GMT  
		Size: 20.4 MB (20423990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba5c15f7bd5dfe32b1718aade52f008519a7ffa497114d413766119a3dbd4f8`  
		Last Modified: Thu, 23 Jun 2022 01:29:14 GMT  
		Size: 6.0 MB (6047312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35008848465d6270ff38da08a7514053d62632985429e2326581b33946d6761b`  
		Last Modified: Thu, 23 Jun 2022 01:30:04 GMT  
		Size: 35.2 MB (35174017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75069e610add6e199c1abfd85f6596a3f7e15bc912230ddb1e0cdab0b41d71d`  
		Last Modified: Thu, 23 Jun 2022 01:29:59 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cdbd4a0e6503bdb63b1ce28ad92eeb99798ed8df1d1cf91cf4b53eabb8b192`  
		Last Modified: Thu, 23 Jun 2022 01:29:59 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6cb9709f043f81dc4d6f60f562a1d82615eb06ff08d1d6ed5544c34ad0fea3`  
		Last Modified: Thu, 23 Jun 2022 01:29:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
