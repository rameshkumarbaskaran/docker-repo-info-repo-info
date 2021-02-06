<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5.8`](#kapacitor158)
-	[`kapacitor:1.5.8-alpine`](#kapacitor158-alpine)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:5c6b018c7ad3244bdcc0a025808171db7b8b829fb6b1d189bec9f5dcdf64171d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:ea35a0814241287b07ab4afb003d387f59e28a1e654923dbaec28d594c4ddbae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96930343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896319b28c0c086b0dcdfc39ce22f7b5c631be5c691b66510548e35db346aad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:05 GMT
ADD file:166cd044a29ad501c753917f07d638932f2ce960a8570b12d9155e8c38d1e917 in / 
# Tue, 12 Jan 2021 00:35:06 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:20:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 00:34:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 00:34:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 00:34:13 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 06 Feb 2021 00:34:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 06 Feb 2021 00:34:18 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 00:34:18 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 00:34:18 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 00:34:18 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 00:34:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 00:34:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2587235a7635c6991dfee9791c7977ab29694cf73bc64c3c5a79097ca99364d1`  
		Last Modified: Tue, 12 Jan 2021 00:43:05 GMT  
		Size: 45.4 MB (45380014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ae0ade158685a8e718a6afd2289fa52e5c5a38342a07ad5e1b3b2fdd1c46bd`  
		Last Modified: Fri, 05 Feb 2021 22:27:08 GMT  
		Size: 11.3 MB (11268539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911674ee9a5463a175abbfc4306db7b2debd5f54db613c089a57891c574b105e`  
		Last Modified: Fri, 05 Feb 2021 22:27:07 GMT  
		Size: 4.3 MB (4341873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85448296a98e89417030cbaa2637eb7f3ca25a8c0df10224dddc81b14f2711d2`  
		Last Modified: Sat, 06 Feb 2021 00:34:55 GMT  
		Size: 13.2 MB (13241611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbad8d39af10a56b6a2dc1d95c0d7d9f87dd876a81631246a598023852dace4`  
		Last Modified: Sat, 06 Feb 2021 00:34:54 GMT  
		Size: 2.8 KB (2825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7189a68c404d49db302a2642bd2ac3e361429e3bbd3c9aa74ef93cc312ecbb`  
		Last Modified: Sat, 06 Feb 2021 00:35:00 GMT  
		Size: 22.7 MB (22695022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f595adc8679b76c16b421a7ca34d075145a1530a88976ce09438a3f81dacba`  
		Last Modified: Sat, 06 Feb 2021 00:34:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca817c82b53cb322b3cfc64233b117d62339d3139b26edcdf6c40a1b56f24260`  
		Last Modified: Sat, 06 Feb 2021 00:34:54 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:6a85a34bb3825d0abdb0424fbc5d8d77f2f2fbce3d279836b42f65419a1a2175
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90686011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc43f6df9989eba5ffa3b3b6039b6287ebc530dd13b12ae0877748b0205e548`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:05:19 GMT
ADD file:9c744a203d36aa8c515bbc11873a4a479cdf3fe9f020ca1ef207b53e6b3a251e in / 
# Tue, 12 Jan 2021 00:05:23 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:59:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:24:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:25:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:25:03 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 06 Feb 2021 01:25:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 06 Feb 2021 01:25:10 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:25:11 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:25:11 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:25:12 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:25:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:25:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f5de2649c1cd9091872f81b8ceb6a67890124f113d9fce9c52bf60d5a6e19f43`  
		Last Modified: Tue, 12 Jan 2021 00:15:23 GMT  
		Size: 42.1 MB (42119951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f99bbdd939756c4a7dcb124462edc660d09e2897b4a63494756911fd90c7530`  
		Last Modified: Fri, 05 Feb 2021 23:09:05 GMT  
		Size: 9.9 MB (9913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1c64fd0b124f851aba2921933249306613c6e9294e28c79e41b8c960a6bcb7`  
		Last Modified: Fri, 05 Feb 2021 23:09:03 GMT  
		Size: 3.9 MB (3921097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee73179dd694f5c92608201effc9cf06624062c27a3741cbda76be77af4823e8`  
		Last Modified: Sat, 06 Feb 2021 01:25:53 GMT  
		Size: 13.4 MB (13418821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc2403d2c08e78f2c0b95147904778e32293164e9ba437a0969dc860ebb5914`  
		Last Modified: Sat, 06 Feb 2021 01:25:50 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b7edb326b588b6255f39e9449ef6646da336eea89198151fd258feb3097fa`  
		Last Modified: Sat, 06 Feb 2021 01:26:00 GMT  
		Size: 21.3 MB (21309001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896fd8c5e9beedea776f4549cd470ced7da9d588475823cd4533f1bbe4dd827f`  
		Last Modified: Sat, 06 Feb 2021 01:25:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87de30c4c2b62837c53d8696bebd5ec91f241d61295c4e9694cd9212394d5af`  
		Last Modified: Sat, 06 Feb 2021 01:25:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:69c2c8c2af52e1c9f8e96fe2c02e11c23bd247ca29414745501cdb7c9258a93e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91715479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6396ea2097dfb6c2150086ea7656a00eb680ab502174aba0876a1b6b0e1aa7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:18 GMT
ADD file:bc4af94773a01defa7a79adb22199dde2229843dae224d13d3385c522cb71652 in / 
# Tue, 12 Jan 2021 00:45:22 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:41:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:41:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:33:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:33:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:33:12 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 06 Feb 2021 01:33:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 06 Feb 2021 01:33:18 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:33:19 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:33:19 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:33:20 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:33:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:33:22 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ec4f0a0f30ab1b4fc2e412a926b8608502de98203ca1994c7916de2017136729`  
		Last Modified: Tue, 12 Jan 2021 00:54:45 GMT  
		Size: 43.2 MB (43177964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25980bf93101cf6e28f2866b5d55dde2a817c6c5e5c9e82be93f55c872b9a9f`  
		Last Modified: Fri, 05 Feb 2021 22:48:57 GMT  
		Size: 10.2 MB (10182590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117548f2863b6d36f3c3df656a2e64c9847e7e6ee40e86ee1619be68045f47d9`  
		Last Modified: Fri, 05 Feb 2021 22:48:56 GMT  
		Size: 4.1 MB (4096578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db01b86ad60544e2a0123a7b740d67480ae14c5dd94aaababe1ef8d56a9c1d`  
		Last Modified: Sat, 06 Feb 2021 01:33:58 GMT  
		Size: 12.9 MB (12946468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ada99c8862f9fe966b9447c1ef535e8bb40474cfa6c02946033f204f93bdcdf`  
		Last Modified: Sat, 06 Feb 2021 01:33:55 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8955b55666f4dd5022e0c658c2f91543b3ac069a2d85d3a05b06d0e4f1347c`  
		Last Modified: Sat, 06 Feb 2021 01:34:02 GMT  
		Size: 21.3 MB (21308569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125bea1036218f8cadc66b1c3dcfffa172f45013777805b3ab8ea3723c90f7f9`  
		Last Modified: Sat, 06 Feb 2021 01:33:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f3a5712a94539cd65a33bb639336b3869708d10679d5b9db30147e3b901bb`  
		Last Modified: Sat, 06 Feb 2021 01:33:55 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:5c6b018c7ad3244bdcc0a025808171db7b8b829fb6b1d189bec9f5dcdf64171d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:ea35a0814241287b07ab4afb003d387f59e28a1e654923dbaec28d594c4ddbae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96930343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896319b28c0c086b0dcdfc39ce22f7b5c631be5c691b66510548e35db346aad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:05 GMT
ADD file:166cd044a29ad501c753917f07d638932f2ce960a8570b12d9155e8c38d1e917 in / 
# Tue, 12 Jan 2021 00:35:06 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:20:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 00:34:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 00:34:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 00:34:13 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 06 Feb 2021 00:34:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 06 Feb 2021 00:34:18 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 00:34:18 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 00:34:18 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 00:34:18 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 00:34:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 00:34:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2587235a7635c6991dfee9791c7977ab29694cf73bc64c3c5a79097ca99364d1`  
		Last Modified: Tue, 12 Jan 2021 00:43:05 GMT  
		Size: 45.4 MB (45380014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ae0ade158685a8e718a6afd2289fa52e5c5a38342a07ad5e1b3b2fdd1c46bd`  
		Last Modified: Fri, 05 Feb 2021 22:27:08 GMT  
		Size: 11.3 MB (11268539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911674ee9a5463a175abbfc4306db7b2debd5f54db613c089a57891c574b105e`  
		Last Modified: Fri, 05 Feb 2021 22:27:07 GMT  
		Size: 4.3 MB (4341873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85448296a98e89417030cbaa2637eb7f3ca25a8c0df10224dddc81b14f2711d2`  
		Last Modified: Sat, 06 Feb 2021 00:34:55 GMT  
		Size: 13.2 MB (13241611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbad8d39af10a56b6a2dc1d95c0d7d9f87dd876a81631246a598023852dace4`  
		Last Modified: Sat, 06 Feb 2021 00:34:54 GMT  
		Size: 2.8 KB (2825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7189a68c404d49db302a2642bd2ac3e361429e3bbd3c9aa74ef93cc312ecbb`  
		Last Modified: Sat, 06 Feb 2021 00:35:00 GMT  
		Size: 22.7 MB (22695022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f595adc8679b76c16b421a7ca34d075145a1530a88976ce09438a3f81dacba`  
		Last Modified: Sat, 06 Feb 2021 00:34:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca817c82b53cb322b3cfc64233b117d62339d3139b26edcdf6c40a1b56f24260`  
		Last Modified: Sat, 06 Feb 2021 00:34:54 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:6a85a34bb3825d0abdb0424fbc5d8d77f2f2fbce3d279836b42f65419a1a2175
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90686011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc43f6df9989eba5ffa3b3b6039b6287ebc530dd13b12ae0877748b0205e548`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:05:19 GMT
ADD file:9c744a203d36aa8c515bbc11873a4a479cdf3fe9f020ca1ef207b53e6b3a251e in / 
# Tue, 12 Jan 2021 00:05:23 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:59:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:24:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:25:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:25:03 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 06 Feb 2021 01:25:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 06 Feb 2021 01:25:10 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:25:11 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:25:11 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:25:12 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:25:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:25:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f5de2649c1cd9091872f81b8ceb6a67890124f113d9fce9c52bf60d5a6e19f43`  
		Last Modified: Tue, 12 Jan 2021 00:15:23 GMT  
		Size: 42.1 MB (42119951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f99bbdd939756c4a7dcb124462edc660d09e2897b4a63494756911fd90c7530`  
		Last Modified: Fri, 05 Feb 2021 23:09:05 GMT  
		Size: 9.9 MB (9913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1c64fd0b124f851aba2921933249306613c6e9294e28c79e41b8c960a6bcb7`  
		Last Modified: Fri, 05 Feb 2021 23:09:03 GMT  
		Size: 3.9 MB (3921097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee73179dd694f5c92608201effc9cf06624062c27a3741cbda76be77af4823e8`  
		Last Modified: Sat, 06 Feb 2021 01:25:53 GMT  
		Size: 13.4 MB (13418821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc2403d2c08e78f2c0b95147904778e32293164e9ba437a0969dc860ebb5914`  
		Last Modified: Sat, 06 Feb 2021 01:25:50 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b7edb326b588b6255f39e9449ef6646da336eea89198151fd258feb3097fa`  
		Last Modified: Sat, 06 Feb 2021 01:26:00 GMT  
		Size: 21.3 MB (21309001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896fd8c5e9beedea776f4549cd470ced7da9d588475823cd4533f1bbe4dd827f`  
		Last Modified: Sat, 06 Feb 2021 01:25:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87de30c4c2b62837c53d8696bebd5ec91f241d61295c4e9694cd9212394d5af`  
		Last Modified: Sat, 06 Feb 2021 01:25:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:69c2c8c2af52e1c9f8e96fe2c02e11c23bd247ca29414745501cdb7c9258a93e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91715479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6396ea2097dfb6c2150086ea7656a00eb680ab502174aba0876a1b6b0e1aa7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:18 GMT
ADD file:bc4af94773a01defa7a79adb22199dde2229843dae224d13d3385c522cb71652 in / 
# Tue, 12 Jan 2021 00:45:22 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:41:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:41:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:33:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:33:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:33:12 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 06 Feb 2021 01:33:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 06 Feb 2021 01:33:18 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:33:19 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:33:19 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:33:20 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:33:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:33:22 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ec4f0a0f30ab1b4fc2e412a926b8608502de98203ca1994c7916de2017136729`  
		Last Modified: Tue, 12 Jan 2021 00:54:45 GMT  
		Size: 43.2 MB (43177964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25980bf93101cf6e28f2866b5d55dde2a817c6c5e5c9e82be93f55c872b9a9f`  
		Last Modified: Fri, 05 Feb 2021 22:48:57 GMT  
		Size: 10.2 MB (10182590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117548f2863b6d36f3c3df656a2e64c9847e7e6ee40e86ee1619be68045f47d9`  
		Last Modified: Fri, 05 Feb 2021 22:48:56 GMT  
		Size: 4.1 MB (4096578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db01b86ad60544e2a0123a7b740d67480ae14c5dd94aaababe1ef8d56a9c1d`  
		Last Modified: Sat, 06 Feb 2021 01:33:58 GMT  
		Size: 12.9 MB (12946468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ada99c8862f9fe966b9447c1ef535e8bb40474cfa6c02946033f204f93bdcdf`  
		Last Modified: Sat, 06 Feb 2021 01:33:55 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8955b55666f4dd5022e0c658c2f91543b3ac069a2d85d3a05b06d0e4f1347c`  
		Last Modified: Sat, 06 Feb 2021 01:34:02 GMT  
		Size: 21.3 MB (21308569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125bea1036218f8cadc66b1c3dcfffa172f45013777805b3ab8ea3723c90f7f9`  
		Last Modified: Sat, 06 Feb 2021 01:33:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3f3a5712a94539cd65a33bb639336b3869708d10679d5b9db30147e3b901bb`  
		Last Modified: Sat, 06 Feb 2021 01:33:55 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:797102b5cdb633ea9bcd98f02e6df6b81b4ae92971315d982f497676251bb1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a3cd5f7ac34d6ed8bb02192555ef40a3078e4194187e91829fb8690ed985592e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19678995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a6cbb3d71432ffe9773020bff6a82308d8bbcdd4796b2befb8b2539249498`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:23:31 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 17 Dec 2020 13:23:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:23:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 13:23:35 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 13:23:35 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 13:23:35 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 17 Dec 2020 13:23:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:23:36 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2700961e2aa9d8b1a747e151bac0e7e85eaf621a73e665aa091034cdbb9fa`  
		Last Modified: Thu, 17 Dec 2020 13:24:11 GMT  
		Size: 16.6 MB (16598520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f0945c6384dc59f39c26a68228e5e75d062e8b903846f0dac9ec9822fddba6`  
		Last Modified: Thu, 17 Dec 2020 13:24:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5717d74957dbfe0e93c0cfe6e49d336e9533eea3f7ae7141f42aa72c708d3c63`  
		Last Modified: Thu, 17 Dec 2020 13:24:07 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:797102b5cdb633ea9bcd98f02e6df6b81b4ae92971315d982f497676251bb1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a3cd5f7ac34d6ed8bb02192555ef40a3078e4194187e91829fb8690ed985592e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19678995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a6cbb3d71432ffe9773020bff6a82308d8bbcdd4796b2befb8b2539249498`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 17 Dec 2020 13:23:31 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 17 Dec 2020 13:23:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 17 Dec 2020 13:23:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Dec 2020 13:23:35 GMT
EXPOSE 9092
# Thu, 17 Dec 2020 13:23:35 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Dec 2020 13:23:35 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 17 Dec 2020 13:23:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Dec 2020 13:23:36 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2700961e2aa9d8b1a747e151bac0e7e85eaf621a73e665aa091034cdbb9fa`  
		Last Modified: Thu, 17 Dec 2020 13:24:11 GMT  
		Size: 16.6 MB (16598520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f0945c6384dc59f39c26a68228e5e75d062e8b903846f0dac9ec9822fddba6`  
		Last Modified: Thu, 17 Dec 2020 13:24:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5717d74957dbfe0e93c0cfe6e49d336e9533eea3f7ae7141f42aa72c708d3c63`  
		Last Modified: Thu, 17 Dec 2020 13:24:07 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:1a0da6ac13394b5e1927a0ce65fa8db2b173678044eaa89de6fa27f2375cc757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:e069696a9ce88a53c9731b19ff6c570b4dbce699ca8cf1212a3ba598da08d12c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111409370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5fce69def3c60c8198860552549dd860756a314c08f4b601768a06e00a20d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:05 GMT
ADD file:166cd044a29ad501c753917f07d638932f2ce960a8570b12d9155e8c38d1e917 in / 
# Tue, 12 Jan 2021 00:35:06 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:20:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 00:34:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 00:34:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 00:34:28 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 06 Feb 2021 00:34:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 06 Feb 2021 00:34:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 00:34:33 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 00:34:33 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 00:34:34 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 00:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 00:34:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2587235a7635c6991dfee9791c7977ab29694cf73bc64c3c5a79097ca99364d1`  
		Last Modified: Tue, 12 Jan 2021 00:43:05 GMT  
		Size: 45.4 MB (45380014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ae0ade158685a8e718a6afd2289fa52e5c5a38342a07ad5e1b3b2fdd1c46bd`  
		Last Modified: Fri, 05 Feb 2021 22:27:08 GMT  
		Size: 11.3 MB (11268539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911674ee9a5463a175abbfc4306db7b2debd5f54db613c089a57891c574b105e`  
		Last Modified: Fri, 05 Feb 2021 22:27:07 GMT  
		Size: 4.3 MB (4341873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85448296a98e89417030cbaa2637eb7f3ca25a8c0df10224dddc81b14f2711d2`  
		Last Modified: Sat, 06 Feb 2021 00:34:55 GMT  
		Size: 13.2 MB (13241611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbad8d39af10a56b6a2dc1d95c0d7d9f87dd876a81631246a598023852dace4`  
		Last Modified: Sat, 06 Feb 2021 00:34:54 GMT  
		Size: 2.8 KB (2825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce99d388eecedfef51e277c4b93be8395bc054ebac47afa3425d39ca2fc38a2`  
		Last Modified: Sat, 06 Feb 2021 00:35:11 GMT  
		Size: 37.2 MB (37174051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62282a8635bcdb6a46aa91c2c785b5b06b3a08193eb4370c461c115eaebe9b50`  
		Last Modified: Sat, 06 Feb 2021 00:35:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7950436a783095ad9f9a5f4087a1a4a5706114e44ae827005ffe7bdb0028a13`  
		Last Modified: Sat, 06 Feb 2021 00:35:06 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:45e64edb2765b2ab06676df0122a39a672058fe91e23ab527f11f10904b46587
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104115588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643128fd7781ccebd57babdb5e681f707e7759dba81c8a6999600231a6bf403a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:05:19 GMT
ADD file:9c744a203d36aa8c515bbc11873a4a479cdf3fe9f020ca1ef207b53e6b3a251e in / 
# Tue, 12 Jan 2021 00:05:23 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:59:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:24:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:25:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:25:24 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 06 Feb 2021 01:25:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 06 Feb 2021 01:25:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:25:32 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:25:32 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:25:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:25:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:25:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f5de2649c1cd9091872f81b8ceb6a67890124f113d9fce9c52bf60d5a6e19f43`  
		Last Modified: Tue, 12 Jan 2021 00:15:23 GMT  
		Size: 42.1 MB (42119951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f99bbdd939756c4a7dcb124462edc660d09e2897b4a63494756911fd90c7530`  
		Last Modified: Fri, 05 Feb 2021 23:09:05 GMT  
		Size: 9.9 MB (9913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1c64fd0b124f851aba2921933249306613c6e9294e28c79e41b8c960a6bcb7`  
		Last Modified: Fri, 05 Feb 2021 23:09:03 GMT  
		Size: 3.9 MB (3921097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee73179dd694f5c92608201effc9cf06624062c27a3741cbda76be77af4823e8`  
		Last Modified: Sat, 06 Feb 2021 01:25:53 GMT  
		Size: 13.4 MB (13418821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc2403d2c08e78f2c0b95147904778e32293164e9ba437a0969dc860ebb5914`  
		Last Modified: Sat, 06 Feb 2021 01:25:50 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aac232bbce4e3a5d27e96e841997a6c66688fed6b174ff58e86735767bc7d16`  
		Last Modified: Sat, 06 Feb 2021 01:26:16 GMT  
		Size: 34.7 MB (34738580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec20b7a97a2ca4769435cefa527072c13425b11e4b481d31109a70ca7f44888d`  
		Last Modified: Sat, 06 Feb 2021 01:26:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee31f9e1e9e43af02694547cdb5f2ebad564317746fb49d0156bb4d0925caab5`  
		Last Modified: Sat, 06 Feb 2021 01:26:07 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:a595c8e14ee4ac495db3fb816af1c0f936e7c789ab332e666813d58c049f595c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104937449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf10207f83e3cac60dad7bf55046f3d2ae7953713eaf0602320ea3baac9d04f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:18 GMT
ADD file:bc4af94773a01defa7a79adb22199dde2229843dae224d13d3385c522cb71652 in / 
# Tue, 12 Jan 2021 00:45:22 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:41:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:41:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:33:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:33:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:33:32 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 06 Feb 2021 01:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 06 Feb 2021 01:33:38 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:33:39 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:33:40 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:33:40 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:33:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:33:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ec4f0a0f30ab1b4fc2e412a926b8608502de98203ca1994c7916de2017136729`  
		Last Modified: Tue, 12 Jan 2021 00:54:45 GMT  
		Size: 43.2 MB (43177964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25980bf93101cf6e28f2866b5d55dde2a817c6c5e5c9e82be93f55c872b9a9f`  
		Last Modified: Fri, 05 Feb 2021 22:48:57 GMT  
		Size: 10.2 MB (10182590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117548f2863b6d36f3c3df656a2e64c9847e7e6ee40e86ee1619be68045f47d9`  
		Last Modified: Fri, 05 Feb 2021 22:48:56 GMT  
		Size: 4.1 MB (4096578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db01b86ad60544e2a0123a7b740d67480ae14c5dd94aaababe1ef8d56a9c1d`  
		Last Modified: Sat, 06 Feb 2021 01:33:58 GMT  
		Size: 12.9 MB (12946468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ada99c8862f9fe966b9447c1ef535e8bb40474cfa6c02946033f204f93bdcdf`  
		Last Modified: Sat, 06 Feb 2021 01:33:55 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e106e61520d23c3c3b3fe5c21885e9d02019c4d158b8a9fba34a2541c15b96`  
		Last Modified: Sat, 06 Feb 2021 01:34:17 GMT  
		Size: 34.5 MB (34530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1cea72594acc3df7161d8ea6752180c161c667a618a3f8d96327df48444199`  
		Last Modified: Sat, 06 Feb 2021 01:34:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f13d259a5d3a70793da85269f646a6ca5ce81c76150b79ca7fe249aa883f2c`  
		Last Modified: Sat, 06 Feb 2021 01:34:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.8`

```console
$ docker pull kapacitor@sha256:1a0da6ac13394b5e1927a0ce65fa8db2b173678044eaa89de6fa27f2375cc757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:e069696a9ce88a53c9731b19ff6c570b4dbce699ca8cf1212a3ba598da08d12c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111409370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5fce69def3c60c8198860552549dd860756a314c08f4b601768a06e00a20d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:05 GMT
ADD file:166cd044a29ad501c753917f07d638932f2ce960a8570b12d9155e8c38d1e917 in / 
# Tue, 12 Jan 2021 00:35:06 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:20:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 00:34:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 00:34:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 00:34:28 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 06 Feb 2021 00:34:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 06 Feb 2021 00:34:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 00:34:33 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 00:34:33 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 00:34:34 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 00:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 00:34:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2587235a7635c6991dfee9791c7977ab29694cf73bc64c3c5a79097ca99364d1`  
		Last Modified: Tue, 12 Jan 2021 00:43:05 GMT  
		Size: 45.4 MB (45380014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ae0ade158685a8e718a6afd2289fa52e5c5a38342a07ad5e1b3b2fdd1c46bd`  
		Last Modified: Fri, 05 Feb 2021 22:27:08 GMT  
		Size: 11.3 MB (11268539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911674ee9a5463a175abbfc4306db7b2debd5f54db613c089a57891c574b105e`  
		Last Modified: Fri, 05 Feb 2021 22:27:07 GMT  
		Size: 4.3 MB (4341873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85448296a98e89417030cbaa2637eb7f3ca25a8c0df10224dddc81b14f2711d2`  
		Last Modified: Sat, 06 Feb 2021 00:34:55 GMT  
		Size: 13.2 MB (13241611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbad8d39af10a56b6a2dc1d95c0d7d9f87dd876a81631246a598023852dace4`  
		Last Modified: Sat, 06 Feb 2021 00:34:54 GMT  
		Size: 2.8 KB (2825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce99d388eecedfef51e277c4b93be8395bc054ebac47afa3425d39ca2fc38a2`  
		Last Modified: Sat, 06 Feb 2021 00:35:11 GMT  
		Size: 37.2 MB (37174051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62282a8635bcdb6a46aa91c2c785b5b06b3a08193eb4370c461c115eaebe9b50`  
		Last Modified: Sat, 06 Feb 2021 00:35:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7950436a783095ad9f9a5f4087a1a4a5706114e44ae827005ffe7bdb0028a13`  
		Last Modified: Sat, 06 Feb 2021 00:35:06 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.8` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:45e64edb2765b2ab06676df0122a39a672058fe91e23ab527f11f10904b46587
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104115588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643128fd7781ccebd57babdb5e681f707e7759dba81c8a6999600231a6bf403a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:05:19 GMT
ADD file:9c744a203d36aa8c515bbc11873a4a479cdf3fe9f020ca1ef207b53e6b3a251e in / 
# Tue, 12 Jan 2021 00:05:23 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:59:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:24:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:25:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:25:24 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 06 Feb 2021 01:25:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 06 Feb 2021 01:25:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:25:32 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:25:32 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:25:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:25:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:25:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f5de2649c1cd9091872f81b8ceb6a67890124f113d9fce9c52bf60d5a6e19f43`  
		Last Modified: Tue, 12 Jan 2021 00:15:23 GMT  
		Size: 42.1 MB (42119951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f99bbdd939756c4a7dcb124462edc660d09e2897b4a63494756911fd90c7530`  
		Last Modified: Fri, 05 Feb 2021 23:09:05 GMT  
		Size: 9.9 MB (9913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1c64fd0b124f851aba2921933249306613c6e9294e28c79e41b8c960a6bcb7`  
		Last Modified: Fri, 05 Feb 2021 23:09:03 GMT  
		Size: 3.9 MB (3921097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee73179dd694f5c92608201effc9cf06624062c27a3741cbda76be77af4823e8`  
		Last Modified: Sat, 06 Feb 2021 01:25:53 GMT  
		Size: 13.4 MB (13418821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc2403d2c08e78f2c0b95147904778e32293164e9ba437a0969dc860ebb5914`  
		Last Modified: Sat, 06 Feb 2021 01:25:50 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aac232bbce4e3a5d27e96e841997a6c66688fed6b174ff58e86735767bc7d16`  
		Last Modified: Sat, 06 Feb 2021 01:26:16 GMT  
		Size: 34.7 MB (34738580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec20b7a97a2ca4769435cefa527072c13425b11e4b481d31109a70ca7f44888d`  
		Last Modified: Sat, 06 Feb 2021 01:26:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee31f9e1e9e43af02694547cdb5f2ebad564317746fb49d0156bb4d0925caab5`  
		Last Modified: Sat, 06 Feb 2021 01:26:07 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:a595c8e14ee4ac495db3fb816af1c0f936e7c789ab332e666813d58c049f595c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104937449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf10207f83e3cac60dad7bf55046f3d2ae7953713eaf0602320ea3baac9d04f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:18 GMT
ADD file:bc4af94773a01defa7a79adb22199dde2229843dae224d13d3385c522cb71652 in / 
# Tue, 12 Jan 2021 00:45:22 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:41:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:41:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:33:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:33:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:33:32 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 06 Feb 2021 01:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 06 Feb 2021 01:33:38 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:33:39 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:33:40 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:33:40 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:33:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:33:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ec4f0a0f30ab1b4fc2e412a926b8608502de98203ca1994c7916de2017136729`  
		Last Modified: Tue, 12 Jan 2021 00:54:45 GMT  
		Size: 43.2 MB (43177964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25980bf93101cf6e28f2866b5d55dde2a817c6c5e5c9e82be93f55c872b9a9f`  
		Last Modified: Fri, 05 Feb 2021 22:48:57 GMT  
		Size: 10.2 MB (10182590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117548f2863b6d36f3c3df656a2e64c9847e7e6ee40e86ee1619be68045f47d9`  
		Last Modified: Fri, 05 Feb 2021 22:48:56 GMT  
		Size: 4.1 MB (4096578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db01b86ad60544e2a0123a7b740d67480ae14c5dd94aaababe1ef8d56a9c1d`  
		Last Modified: Sat, 06 Feb 2021 01:33:58 GMT  
		Size: 12.9 MB (12946468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ada99c8862f9fe966b9447c1ef535e8bb40474cfa6c02946033f204f93bdcdf`  
		Last Modified: Sat, 06 Feb 2021 01:33:55 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e106e61520d23c3c3b3fe5c21885e9d02019c4d158b8a9fba34a2541c15b96`  
		Last Modified: Sat, 06 Feb 2021 01:34:17 GMT  
		Size: 34.5 MB (34530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1cea72594acc3df7161d8ea6752180c161c667a618a3f8d96327df48444199`  
		Last Modified: Sat, 06 Feb 2021 01:34:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f13d259a5d3a70793da85269f646a6ca5ce81c76150b79ca7fe249aa883f2c`  
		Last Modified: Sat, 06 Feb 2021 01:34:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.8-alpine`

```console
$ docker pull kapacitor@sha256:fbd4868cae4b9120a0ff967d8b9566d3dec6d3f2a4dabf343a10c8367e4a17db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:72221f66afde98ab75b9c11110d88bcb73cfb317a85c5547eeeafd4caedb9481
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22597445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8176b8540df511d9259ce17ccbc98abaa07629d5cf9a9373c7b52d5ed60b87f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 28 Jan 2021 23:20:49 GMT
ENV KAPACITOR_VERSION=1.5.8
# Thu, 28 Jan 2021 23:20:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 28 Jan 2021 23:20:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 28 Jan 2021 23:20:53 GMT
EXPOSE 9092
# Thu, 28 Jan 2021 23:20:53 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 28 Jan 2021 23:20:54 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 28 Jan 2021 23:20:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Jan 2021 23:20:54 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4490cc4730a688f4c1e98ef48da92bfb00684539e9a8d0c3851e9ba007ea0c26`  
		Last Modified: Thu, 28 Jan 2021 23:21:27 GMT  
		Size: 19.5 MB (19516971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966d57ac7304061eec1a6d3e58cfc72b50607e1e0030a3d049c2449c4d2c10fd`  
		Last Modified: Thu, 28 Jan 2021 23:21:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adab7b964a7a37e3d6a62e6298dd36b1f04116f35302a5a4235f6f27018bb53c`  
		Last Modified: Thu, 28 Jan 2021 23:21:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:fbd4868cae4b9120a0ff967d8b9566d3dec6d3f2a4dabf343a10c8367e4a17db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:72221f66afde98ab75b9c11110d88bcb73cfb317a85c5547eeeafd4caedb9481
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22597445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8176b8540df511d9259ce17ccbc98abaa07629d5cf9a9373c7b52d5ed60b87f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 28 Jan 2021 23:20:49 GMT
ENV KAPACITOR_VERSION=1.5.8
# Thu, 28 Jan 2021 23:20:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 28 Jan 2021 23:20:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 28 Jan 2021 23:20:53 GMT
EXPOSE 9092
# Thu, 28 Jan 2021 23:20:53 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 28 Jan 2021 23:20:54 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 28 Jan 2021 23:20:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Jan 2021 23:20:54 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4490cc4730a688f4c1e98ef48da92bfb00684539e9a8d0c3851e9ba007ea0c26`  
		Last Modified: Thu, 28 Jan 2021 23:21:27 GMT  
		Size: 19.5 MB (19516971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966d57ac7304061eec1a6d3e58cfc72b50607e1e0030a3d049c2449c4d2c10fd`  
		Last Modified: Thu, 28 Jan 2021 23:21:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adab7b964a7a37e3d6a62e6298dd36b1f04116f35302a5a4235f6f27018bb53c`  
		Last Modified: Thu, 28 Jan 2021 23:21:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:fbd4868cae4b9120a0ff967d8b9566d3dec6d3f2a4dabf343a10c8367e4a17db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:72221f66afde98ab75b9c11110d88bcb73cfb317a85c5547eeeafd4caedb9481
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22597445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8176b8540df511d9259ce17ccbc98abaa07629d5cf9a9373c7b52d5ed60b87f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:07:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Dec 2020 13:07:54 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 28 Jan 2021 23:20:49 GMT
ENV KAPACITOR_VERSION=1.5.8
# Thu, 28 Jan 2021 23:20:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 28 Jan 2021 23:20:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 28 Jan 2021 23:20:53 GMT
EXPOSE 9092
# Thu, 28 Jan 2021 23:20:53 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 28 Jan 2021 23:20:54 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 28 Jan 2021 23:20:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Jan 2021 23:20:54 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210e4df99beaffbde65dfe580e9923c2bef3b5dd07f0ac7d364e47dc2fac52`  
		Last Modified: Thu, 17 Dec 2020 13:09:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a689ddee3aadca4971508078c3d8f60b8fdbeb3ee260f4212e3b37c6548cf`  
		Last Modified: Thu, 17 Dec 2020 13:09:08 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4490cc4730a688f4c1e98ef48da92bfb00684539e9a8d0c3851e9ba007ea0c26`  
		Last Modified: Thu, 28 Jan 2021 23:21:27 GMT  
		Size: 19.5 MB (19516971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966d57ac7304061eec1a6d3e58cfc72b50607e1e0030a3d049c2449c4d2c10fd`  
		Last Modified: Thu, 28 Jan 2021 23:21:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adab7b964a7a37e3d6a62e6298dd36b1f04116f35302a5a4235f6f27018bb53c`  
		Last Modified: Thu, 28 Jan 2021 23:21:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:1a0da6ac13394b5e1927a0ce65fa8db2b173678044eaa89de6fa27f2375cc757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:e069696a9ce88a53c9731b19ff6c570b4dbce699ca8cf1212a3ba598da08d12c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111409370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5fce69def3c60c8198860552549dd860756a314c08f4b601768a06e00a20d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:05 GMT
ADD file:166cd044a29ad501c753917f07d638932f2ce960a8570b12d9155e8c38d1e917 in / 
# Tue, 12 Jan 2021 00:35:06 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:20:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 00:34:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 00:34:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 00:34:28 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 06 Feb 2021 00:34:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 06 Feb 2021 00:34:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 00:34:33 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 00:34:33 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 00:34:34 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 00:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 00:34:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2587235a7635c6991dfee9791c7977ab29694cf73bc64c3c5a79097ca99364d1`  
		Last Modified: Tue, 12 Jan 2021 00:43:05 GMT  
		Size: 45.4 MB (45380014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ae0ade158685a8e718a6afd2289fa52e5c5a38342a07ad5e1b3b2fdd1c46bd`  
		Last Modified: Fri, 05 Feb 2021 22:27:08 GMT  
		Size: 11.3 MB (11268539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911674ee9a5463a175abbfc4306db7b2debd5f54db613c089a57891c574b105e`  
		Last Modified: Fri, 05 Feb 2021 22:27:07 GMT  
		Size: 4.3 MB (4341873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85448296a98e89417030cbaa2637eb7f3ca25a8c0df10224dddc81b14f2711d2`  
		Last Modified: Sat, 06 Feb 2021 00:34:55 GMT  
		Size: 13.2 MB (13241611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbad8d39af10a56b6a2dc1d95c0d7d9f87dd876a81631246a598023852dace4`  
		Last Modified: Sat, 06 Feb 2021 00:34:54 GMT  
		Size: 2.8 KB (2825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce99d388eecedfef51e277c4b93be8395bc054ebac47afa3425d39ca2fc38a2`  
		Last Modified: Sat, 06 Feb 2021 00:35:11 GMT  
		Size: 37.2 MB (37174051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62282a8635bcdb6a46aa91c2c785b5b06b3a08193eb4370c461c115eaebe9b50`  
		Last Modified: Sat, 06 Feb 2021 00:35:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7950436a783095ad9f9a5f4087a1a4a5706114e44ae827005ffe7bdb0028a13`  
		Last Modified: Sat, 06 Feb 2021 00:35:06 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:45e64edb2765b2ab06676df0122a39a672058fe91e23ab527f11f10904b46587
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104115588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643128fd7781ccebd57babdb5e681f707e7759dba81c8a6999600231a6bf403a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:05:19 GMT
ADD file:9c744a203d36aa8c515bbc11873a4a479cdf3fe9f020ca1ef207b53e6b3a251e in / 
# Tue, 12 Jan 2021 00:05:23 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:59:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:24:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:25:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:25:24 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 06 Feb 2021 01:25:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 06 Feb 2021 01:25:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:25:32 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:25:32 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:25:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:25:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:25:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f5de2649c1cd9091872f81b8ceb6a67890124f113d9fce9c52bf60d5a6e19f43`  
		Last Modified: Tue, 12 Jan 2021 00:15:23 GMT  
		Size: 42.1 MB (42119951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f99bbdd939756c4a7dcb124462edc660d09e2897b4a63494756911fd90c7530`  
		Last Modified: Fri, 05 Feb 2021 23:09:05 GMT  
		Size: 9.9 MB (9913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1c64fd0b124f851aba2921933249306613c6e9294e28c79e41b8c960a6bcb7`  
		Last Modified: Fri, 05 Feb 2021 23:09:03 GMT  
		Size: 3.9 MB (3921097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee73179dd694f5c92608201effc9cf06624062c27a3741cbda76be77af4823e8`  
		Last Modified: Sat, 06 Feb 2021 01:25:53 GMT  
		Size: 13.4 MB (13418821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc2403d2c08e78f2c0b95147904778e32293164e9ba437a0969dc860ebb5914`  
		Last Modified: Sat, 06 Feb 2021 01:25:50 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aac232bbce4e3a5d27e96e841997a6c66688fed6b174ff58e86735767bc7d16`  
		Last Modified: Sat, 06 Feb 2021 01:26:16 GMT  
		Size: 34.7 MB (34738580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec20b7a97a2ca4769435cefa527072c13425b11e4b481d31109a70ca7f44888d`  
		Last Modified: Sat, 06 Feb 2021 01:26:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee31f9e1e9e43af02694547cdb5f2ebad564317746fb49d0156bb4d0925caab5`  
		Last Modified: Sat, 06 Feb 2021 01:26:07 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:a595c8e14ee4ac495db3fb816af1c0f936e7c789ab332e666813d58c049f595c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104937449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf10207f83e3cac60dad7bf55046f3d2ae7953713eaf0602320ea3baac9d04f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:18 GMT
ADD file:bc4af94773a01defa7a79adb22199dde2229843dae224d13d3385c522cb71652 in / 
# Tue, 12 Jan 2021 00:45:22 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:41:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:41:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 06 Feb 2021 01:33:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 06 Feb 2021 01:33:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 06 Feb 2021 01:33:32 GMT
ENV KAPACITOR_VERSION=1.5.8
# Sat, 06 Feb 2021 01:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 06 Feb 2021 01:33:38 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 06 Feb 2021 01:33:39 GMT
EXPOSE 9092
# Sat, 06 Feb 2021 01:33:40 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 06 Feb 2021 01:33:40 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 06 Feb 2021 01:33:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Feb 2021 01:33:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:ec4f0a0f30ab1b4fc2e412a926b8608502de98203ca1994c7916de2017136729`  
		Last Modified: Tue, 12 Jan 2021 00:54:45 GMT  
		Size: 43.2 MB (43177964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25980bf93101cf6e28f2866b5d55dde2a817c6c5e5c9e82be93f55c872b9a9f`  
		Last Modified: Fri, 05 Feb 2021 22:48:57 GMT  
		Size: 10.2 MB (10182590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117548f2863b6d36f3c3df656a2e64c9847e7e6ee40e86ee1619be68045f47d9`  
		Last Modified: Fri, 05 Feb 2021 22:48:56 GMT  
		Size: 4.1 MB (4096578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db01b86ad60544e2a0123a7b740d67480ae14c5dd94aaababe1ef8d56a9c1d`  
		Last Modified: Sat, 06 Feb 2021 01:33:58 GMT  
		Size: 12.9 MB (12946468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ada99c8862f9fe966b9447c1ef535e8bb40474cfa6c02946033f204f93bdcdf`  
		Last Modified: Sat, 06 Feb 2021 01:33:55 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e106e61520d23c3c3b3fe5c21885e9d02019c4d158b8a9fba34a2541c15b96`  
		Last Modified: Sat, 06 Feb 2021 01:34:17 GMT  
		Size: 34.5 MB (34530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1cea72594acc3df7161d8ea6752180c161c667a618a3f8d96327df48444199`  
		Last Modified: Sat, 06 Feb 2021 01:34:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f13d259a5d3a70793da85269f646a6ca5ce81c76150b79ca7fe249aa883f2c`  
		Last Modified: Sat, 06 Feb 2021 01:34:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
