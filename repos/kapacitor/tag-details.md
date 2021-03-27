<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:1.5.8`](#kapacitor158)
-	[`kapacitor:1.5.8-alpine`](#kapacitor158-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:bc8d57a6875840e903252847111a6d110c0730f4390813dcdd1b865b0d6fd926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:1e64e6aeda6cecfa26df9db8ee87f3e216fd1277743e8d88708cfcb4a102dc28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96970580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a408da54922b898bf26ffd6ad832188bf396265af5462789458d590ab0391a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:31:52 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 20:31:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 20:31:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:31:56 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:31:56 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:31:56 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:31:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:31:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473f39bb5ac5870cdede8897911c55fe1279666c3ddf7d3147c598ab93a3337c`  
		Last Modified: Sat, 27 Mar 2021 20:32:32 GMT  
		Size: 22.7 MB (22695441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb819cb9874f896ac76f6b558815ba5e4554e4c033fd5aaf9c31b688b1080b`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a817a17222887d9a00748d2d75db3f39d72607ea9318427186136ae3ae54c`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:ccecc2174867a4b78d7c70cc924137164e342aceb5902cf3c8735dc915f69d8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90734598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0797aa45760da35f5deb3683fdb2719ad615676454177717e71307d58c501f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:15 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 09:07:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:27 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:07:28 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:07:28 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:07:30 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:07:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:07:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360770c5a31ae0607cbf09cd7d020eaecfdfa816afc6035c48600e9ffcd3d53b`  
		Last Modified: Sat, 27 Mar 2021 09:08:32 GMT  
		Size: 21.3 MB (21309019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c416ea00897389d4739bfb9d2cd098ffb86fe3293471bfc7f6a6f890bb04e31`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd21dd5fb4748e21e4c36bf5da2b22698ba5ec1ef4d20220fe59cd8c7f1305f`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:4398de26903cde0bc726e4921d8909897cc81df390b7aabfc60eb8ae8c91f16c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91734069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1715ab7f802b1c8c58f0fcf92ff7e9e8f5c6238b4296c1ac54a98446629480ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:19 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 12 Mar 2021 19:49:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:27 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:28 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:29 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:49:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1307305943643ac11712d67690ec9923d71f6a115f0ab69b3e844d1f12dc41c1`  
		Last Modified: Fri, 12 Mar 2021 19:50:24 GMT  
		Size: 21.3 MB (21308559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c61f0130c88777b09865eacd2723cc1402dfbcbdf1f6a81c56063bc37e3bd4`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36299ac46be373b41ce5c5697ac0090679ca75e0ee7b7a14520a2518bef0a910`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:54a6209f0269a3c3dcdaa302c2d0649fe8db1dcdd3aa7dd84731546cf65ed45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b550e6807fc912340d2801c376672a1a11430367cdfdfe37faa6e2208fcbd75a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19679814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed38b5e46c1e806aa08222730a72f63c2ea8cc5b8369089ca2b8b548aa475d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:22:49 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 26 Mar 2021 08:22:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:22:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:22:54 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:22:54 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:22:54 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:22:54 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dc843fb1f362c9d9f9a5cb89ddcbc78e3ad79f2ae8bd830fe5f679d0c386ed`  
		Last Modified: Fri, 26 Mar 2021 08:23:29 GMT  
		Size: 16.6 MB (16598543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e875139b687500fa7b3e558749354b4e74fd98b31d035ee8c59638d90aeeeeb`  
		Last Modified: Fri, 26 Mar 2021 08:23:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5703f1fbcb9d90bb8ff7ba69f8c5ed12b12f2c7d42263356b3289a43239fc3`  
		Last Modified: Fri, 26 Mar 2021 08:23:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:bc8d57a6875840e903252847111a6d110c0730f4390813dcdd1b865b0d6fd926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:1e64e6aeda6cecfa26df9db8ee87f3e216fd1277743e8d88708cfcb4a102dc28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96970580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a408da54922b898bf26ffd6ad832188bf396265af5462789458d590ab0391a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:31:52 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 20:31:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 20:31:56 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:31:56 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:31:56 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:31:56 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:31:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:31:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473f39bb5ac5870cdede8897911c55fe1279666c3ddf7d3147c598ab93a3337c`  
		Last Modified: Sat, 27 Mar 2021 20:32:32 GMT  
		Size: 22.7 MB (22695441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb819cb9874f896ac76f6b558815ba5e4554e4c033fd5aaf9c31b688b1080b`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a817a17222887d9a00748d2d75db3f39d72607ea9318427186136ae3ae54c`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:ccecc2174867a4b78d7c70cc924137164e342aceb5902cf3c8735dc915f69d8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90734598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0797aa45760da35f5deb3683fdb2719ad615676454177717e71307d58c501f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:15 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 27 Mar 2021 09:07:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:27 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:07:28 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:07:28 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:07:30 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:07:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:07:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360770c5a31ae0607cbf09cd7d020eaecfdfa816afc6035c48600e9ffcd3d53b`  
		Last Modified: Sat, 27 Mar 2021 09:08:32 GMT  
		Size: 21.3 MB (21309019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c416ea00897389d4739bfb9d2cd098ffb86fe3293471bfc7f6a6f890bb04e31`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd21dd5fb4748e21e4c36bf5da2b22698ba5ec1ef4d20220fe59cd8c7f1305f`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:4398de26903cde0bc726e4921d8909897cc81df390b7aabfc60eb8ae8c91f16c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91734069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1715ab7f802b1c8c58f0fcf92ff7e9e8f5c6238b4296c1ac54a98446629480ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:19 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 12 Mar 2021 19:49:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:27 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:28 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:29 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:49:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1307305943643ac11712d67690ec9923d71f6a115f0ab69b3e844d1f12dc41c1`  
		Last Modified: Fri, 12 Mar 2021 19:50:24 GMT  
		Size: 21.3 MB (21308559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c61f0130c88777b09865eacd2723cc1402dfbcbdf1f6a81c56063bc37e3bd4`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36299ac46be373b41ce5c5697ac0090679ca75e0ee7b7a14520a2518bef0a910`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:54a6209f0269a3c3dcdaa302c2d0649fe8db1dcdd3aa7dd84731546cf65ed45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b550e6807fc912340d2801c376672a1a11430367cdfdfe37faa6e2208fcbd75a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19679814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed38b5e46c1e806aa08222730a72f63c2ea8cc5b8369089ca2b8b548aa475d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:22:49 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 26 Mar 2021 08:22:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:22:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:22:54 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:22:54 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:22:54 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:22:54 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dc843fb1f362c9d9f9a5cb89ddcbc78e3ad79f2ae8bd830fe5f679d0c386ed`  
		Last Modified: Fri, 26 Mar 2021 08:23:29 GMT  
		Size: 16.6 MB (16598543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e875139b687500fa7b3e558749354b4e74fd98b31d035ee8c59638d90aeeeeb`  
		Last Modified: Fri, 26 Mar 2021 08:23:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5703f1fbcb9d90bb8ff7ba69f8c5ed12b12f2c7d42263356b3289a43239fc3`  
		Last Modified: Fri, 26 Mar 2021 08:23:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:d7787880d22b5a293c8a48f606f29330f974298e21b2487a57a5141f8ac6ab40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:3ab61e2059a4f3cafacff7d1cfdc3d4d7d2911f61ced6468fef57a1c08e72ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111449500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada42dea1083fd4a68ed700a926cafbed4dec691e19ad952d054b58ee462d467`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:32:02 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 20:32:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 20:32:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:32:08 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:32:08 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:32:08 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:32:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:32:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bf00bbc3dfb229dd261e340cf51cd7ab2c521606bf33a31c0151957364fb66`  
		Last Modified: Sat, 27 Mar 2021 20:32:48 GMT  
		Size: 37.2 MB (37174360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e093880828ab1d78f8852129cd98780c9b79e7f1f029b830991e8469b145b21`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c239f527a9508c7200c46a24012866348a320a71d4df24fad6fea341f793e679`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:b906902169272e864f480f9086430f53c626dc49250202c66aa2d5fe4c7833cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104164159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7abeabbf2891b8bccfcf54b68a002c8132809ae3da54988d773b3013dffc2038`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:46 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 09:07:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:08:01 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:08:02 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:08:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:08:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a314e91b9ff7f5d05bb6d8035d6ca93b5cc938ae5339ce34e4c6206ae42995b`  
		Last Modified: Sat, 27 Mar 2021 09:08:48 GMT  
		Size: 34.7 MB (34738582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4220b10e3575373f9809be75ac373fd7d3ed227ed82a1a35a48482d78666fc`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664b33bbc1108e9b0e1dcb52fea68f46fd64ac4bdde359973d3a2782508b5ff3`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:70a98cc2a5b1383ca4cd272f3a80488ed37d3a6d8b4fd4f532dcf95ced2d8ff7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104956048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ba9a22131ba6ef611a858b5b84743158c0a2ec51528ceb9469c4e36c13ca67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:41 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 12 Mar 2021 19:49:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:54 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:56 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:50:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:50:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ca8163a29990c822d8f62cfb3bf6070630b4ada98c6bf9f0ab5d2f4cb7dab3`  
		Last Modified: Fri, 12 Mar 2021 19:50:38 GMT  
		Size: 34.5 MB (34530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775afa8d832dd476f9725b517911cefee1b3f9daa733bf8e4d55521311c96fc5`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fc817d3fb61dec22dbcfc8067ea0381b89ce5e107f282bb7cc4aff5f800ecb`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:684a895ed468b04f098a03081339331035942409718bfe72ea1ea2b9660f1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e778dca7174b8237484b939711d1e6cce324c71ab655f31f03ab5dfa1cb0dbef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22598232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51adc0fc1da945b01596c8be1d037467be8b5f0e48bb5f52777b92ee484f2557`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:23:00 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 26 Mar 2021 08:23:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:23:05 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:23:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:23:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:23:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50319ecf6cd5028d57c8a15888eff67a9c5ef9549ff4d40452dd713ad65dc254`  
		Last Modified: Fri, 26 Mar 2021 08:23:48 GMT  
		Size: 19.5 MB (19516959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cce72b7cf74eaf6267dde03d9ddaac716790a02d9af5ac5894b9d7ab414b27d`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba736aa2bc582298f5370c9d3b7b5688b8cfdb37ee0b8292196b72a49574ff1`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.8`

```console
$ docker pull kapacitor@sha256:d7787880d22b5a293c8a48f606f29330f974298e21b2487a57a5141f8ac6ab40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:3ab61e2059a4f3cafacff7d1cfdc3d4d7d2911f61ced6468fef57a1c08e72ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111449500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada42dea1083fd4a68ed700a926cafbed4dec691e19ad952d054b58ee462d467`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:32:02 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 20:32:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 20:32:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:32:08 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:32:08 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:32:08 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:32:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:32:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bf00bbc3dfb229dd261e340cf51cd7ab2c521606bf33a31c0151957364fb66`  
		Last Modified: Sat, 27 Mar 2021 20:32:48 GMT  
		Size: 37.2 MB (37174360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e093880828ab1d78f8852129cd98780c9b79e7f1f029b830991e8469b145b21`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c239f527a9508c7200c46a24012866348a320a71d4df24fad6fea341f793e679`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.8` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:b906902169272e864f480f9086430f53c626dc49250202c66aa2d5fe4c7833cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104164159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7abeabbf2891b8bccfcf54b68a002c8132809ae3da54988d773b3013dffc2038`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:46 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 09:07:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:08:01 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:08:02 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:08:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:08:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a314e91b9ff7f5d05bb6d8035d6ca93b5cc938ae5339ce34e4c6206ae42995b`  
		Last Modified: Sat, 27 Mar 2021 09:08:48 GMT  
		Size: 34.7 MB (34738582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4220b10e3575373f9809be75ac373fd7d3ed227ed82a1a35a48482d78666fc`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664b33bbc1108e9b0e1dcb52fea68f46fd64ac4bdde359973d3a2782508b5ff3`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:70a98cc2a5b1383ca4cd272f3a80488ed37d3a6d8b4fd4f532dcf95ced2d8ff7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104956048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ba9a22131ba6ef611a858b5b84743158c0a2ec51528ceb9469c4e36c13ca67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:41 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 12 Mar 2021 19:49:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:54 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:56 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:50:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:50:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ca8163a29990c822d8f62cfb3bf6070630b4ada98c6bf9f0ab5d2f4cb7dab3`  
		Last Modified: Fri, 12 Mar 2021 19:50:38 GMT  
		Size: 34.5 MB (34530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775afa8d832dd476f9725b517911cefee1b3f9daa733bf8e4d55521311c96fc5`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fc817d3fb61dec22dbcfc8067ea0381b89ce5e107f282bb7cc4aff5f800ecb`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.8-alpine`

```console
$ docker pull kapacitor@sha256:684a895ed468b04f098a03081339331035942409718bfe72ea1ea2b9660f1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e778dca7174b8237484b939711d1e6cce324c71ab655f31f03ab5dfa1cb0dbef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22598232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51adc0fc1da945b01596c8be1d037467be8b5f0e48bb5f52777b92ee484f2557`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:23:00 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 26 Mar 2021 08:23:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:23:05 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:23:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:23:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:23:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50319ecf6cd5028d57c8a15888eff67a9c5ef9549ff4d40452dd713ad65dc254`  
		Last Modified: Fri, 26 Mar 2021 08:23:48 GMT  
		Size: 19.5 MB (19516959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cce72b7cf74eaf6267dde03d9ddaac716790a02d9af5ac5894b9d7ab414b27d`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba736aa2bc582298f5370c9d3b7b5688b8cfdb37ee0b8292196b72a49574ff1`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:684a895ed468b04f098a03081339331035942409718bfe72ea1ea2b9660f1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e778dca7174b8237484b939711d1e6cce324c71ab655f31f03ab5dfa1cb0dbef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22598232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51adc0fc1da945b01596c8be1d037467be8b5f0e48bb5f52777b92ee484f2557`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:40:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 26 Mar 2021 08:23:00 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 26 Mar 2021 08:23:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Mar 2021 08:23:05 GMT
EXPOSE 9092
# Fri, 26 Mar 2021 08:23:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Mar 2021 08:23:05 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 26 Mar 2021 08:23:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:23:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496828ab4972e79f1f4703990b2ca8339bccc53b23b09661bad5a86079d7ce44`  
		Last Modified: Fri, 26 Mar 2021 02:42:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f4fdff4d2de3741ff5301f2ca4d71dfb5041fbd5f4aa01cfd6823ac6693f9`  
		Last Modified: Fri, 26 Mar 2021 02:42:07 GMT  
		Size: 280.9 KB (280877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50319ecf6cd5028d57c8a15888eff67a9c5ef9549ff4d40452dd713ad65dc254`  
		Last Modified: Fri, 26 Mar 2021 08:23:48 GMT  
		Size: 19.5 MB (19516959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cce72b7cf74eaf6267dde03d9ddaac716790a02d9af5ac5894b9d7ab414b27d`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba736aa2bc582298f5370c9d3b7b5688b8cfdb37ee0b8292196b72a49574ff1`  
		Last Modified: Fri, 26 Mar 2021 08:23:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:d7787880d22b5a293c8a48f606f29330f974298e21b2487a57a5141f8ac6ab40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:3ab61e2059a4f3cafacff7d1cfdc3d4d7d2911f61ced6468fef57a1c08e72ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111449500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada42dea1083fd4a68ed700a926cafbed4dec691e19ad952d054b58ee462d467`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:57:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:57:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 20:31:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 20:31:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 20:32:02 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 20:32:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 20:32:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 20:32:08 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 20:32:08 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 20:32:08 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 20:32:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 20:32:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b11a61e4b8cbb37a4a570baf51ae6bbc8cbf231f56401403e21dea70144d`  
		Last Modified: Sat, 27 Mar 2021 06:06:53 GMT  
		Size: 11.3 MB (11286512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006eb4a69e602dcb61f4680d7e4a0d4853902062ab1230263e33125ae86b2700`  
		Last Modified: Sat, 27 Mar 2021 06:06:52 GMT  
		Size: 4.3 MB (4342442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76ee30b85b7d3497e854fa24f0482c85bc7f03147cbf4ad118aba7dbfb8f4a`  
		Last Modified: Sat, 27 Mar 2021 20:32:28 GMT  
		Size: 13.3 MB (13263366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa725840a3b91b97f154b6edaaaa8eb15d3870ac4a828a76eb8b32061d52e7`  
		Last Modified: Sat, 27 Mar 2021 20:32:27 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bf00bbc3dfb229dd261e340cf51cd7ab2c521606bf33a31c0151957364fb66`  
		Last Modified: Sat, 27 Mar 2021 20:32:48 GMT  
		Size: 37.2 MB (37174360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e093880828ab1d78f8852129cd98780c9b79e7f1f029b830991e8469b145b21`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c239f527a9508c7200c46a24012866348a320a71d4df24fad6fea341f793e679`  
		Last Modified: Sat, 27 Mar 2021 20:32:43 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:b906902169272e864f480f9086430f53c626dc49250202c66aa2d5fe4c7833cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104164159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7abeabbf2891b8bccfcf54b68a002c8132809ae3da54988d773b3013dffc2038`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 09:07:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 27 Mar 2021 09:07:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 27 Mar 2021 09:07:46 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 27 Mar 2021 09:07:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 27 Mar 2021 09:07:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Mar 2021 09:08:01 GMT
EXPOSE 9092
# Sat, 27 Mar 2021 09:08:02 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Mar 2021 09:08:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 27 Mar 2021 09:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Mar 2021 09:08:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee4d56297605ceebbf2d176ca94adfd0c6eb965a4cb38cc4c0e6c352df3816`  
		Last Modified: Sat, 27 Mar 2021 09:08:25 GMT  
		Size: 13.4 MB (13441409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7a8fd04a34e994787e72ef37ac86a76604388e5fc0c98c9bad3154bbd9ffa`  
		Last Modified: Sat, 27 Mar 2021 09:08:23 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a314e91b9ff7f5d05bb6d8035d6ca93b5cc938ae5339ce34e4c6206ae42995b`  
		Last Modified: Sat, 27 Mar 2021 09:08:48 GMT  
		Size: 34.7 MB (34738582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4220b10e3575373f9809be75ac373fd7d3ed227ed82a1a35a48482d78666fc`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664b33bbc1108e9b0e1dcb52fea68f46fd64ac4bdde359973d3a2782508b5ff3`  
		Last Modified: Sat, 27 Mar 2021 09:08:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:70a98cc2a5b1383ca4cd272f3a80488ed37d3a6d8b4fd4f532dcf95ced2d8ff7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104956048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ba9a22131ba6ef611a858b5b84743158c0a2ec51528ceb9469c4e36c13ca67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:41 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 12 Mar 2021 19:49:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:54 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:56 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:50:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:50:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ca8163a29990c822d8f62cfb3bf6070630b4ada98c6bf9f0ab5d2f4cb7dab3`  
		Last Modified: Fri, 12 Mar 2021 19:50:38 GMT  
		Size: 34.5 MB (34530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775afa8d832dd476f9725b517911cefee1b3f9daa733bf8e4d55521311c96fc5`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fc817d3fb61dec22dbcfc8067ea0381b89ce5e107f282bb7cc4aff5f800ecb`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
