<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5.6`](#kapacitor156)
-	[`kapacitor:1.5.6-alpine`](#kapacitor156-alpine)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:b89a4566a57903439bd75608aa6479b98b8c10977b52ff2cf909da15cec09d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:0a9930bdc5dbcac1655ad92f5ffee3f3033e6f5dd4293ab49f1b72119faca9be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96239792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859f0e0681aec1931aa3d88f88a76f950b766d3cce976fecb83f99e3efe4aa6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:32:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 00:16:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 00:16:19 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 02 Sep 2020 00:16:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 02 Sep 2020 00:16:23 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 00:16:23 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 00:16:23 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 00:16:23 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 00:16:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:16:24 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d20988f49753a67fbf2842359c77fda4e47ccd36213a864d51fc550cb3d4bfe`  
		Last Modified: Wed, 05 Aug 2020 16:32:54 GMT  
		Size: 13.1 MB (13084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027977b65bfb7d6972f64909f085660f99749c7f9ec0f250bd25700824f5216b`  
		Last Modified: Wed, 02 Sep 2020 00:16:54 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02d5181830a7324de6fbf4a9f98f6b93f4acca3cbf816d8b38e6c28f5976d4d`  
		Last Modified: Wed, 02 Sep 2020 00:16:59 GMT  
		Size: 22.7 MB (22694289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eed621c2e54f16f6b66e3e22bd4590a61f3ae5295b70d7c2bc02e8a7406b7ba`  
		Last Modified: Wed, 02 Sep 2020 00:16:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb16d8c7bbff09b0eed56ec7273e961ab8db20546a24a796fc23a8cb82a768`  
		Last Modified: Wed, 02 Sep 2020 00:16:54 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:ec055017499e04f90f30e60f40a20c8b303bfa44ddb368cfdb5ed44c7f2bc228
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90039712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d457c93f2230ee16f80a0a823df69f0507dad60c6bbfd9908a63f8d1c5bff6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 05:29:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 01:26:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 01:26:09 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 02 Sep 2020 01:26:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 02 Sep 2020 01:26:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 01:26:55 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 01:26:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 01:27:08 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 01:27:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 01:27:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1621cafe44218577f3ed96b59c43d18d81a0d529ca3f3e5f1e20a4b917b5145e`  
		Last Modified: Wed, 05 Aug 2020 05:31:31 GMT  
		Size: 13.3 MB (13254548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ce95cfb70f0ef4517e0dbd22c936087cdb9670b42abcaf5655f09bf2118a29`  
		Last Modified: Wed, 02 Sep 2020 01:29:09 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b73d6dba3081c8634d46467ae114c423b69c9c7b26466a7976b0231b260b5c`  
		Last Modified: Wed, 02 Sep 2020 01:29:18 GMT  
		Size: 21.3 MB (21308099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6855e79b5127189ea26c49e76776807737221b12aee397d53758f8e63d8e7d77`  
		Last Modified: Wed, 02 Sep 2020 01:29:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5295c4bc4fa6e7217fb60feac5c451b057348975fc58fb848ec7653e4e52c9f2`  
		Last Modified: Wed, 02 Sep 2020 01:29:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:dd4908f889386df6541a838e0d88d4e38940036c157f0d4a2fc7a84655159a8b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91069499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36745dfdaf9d7dce714c4c0ad651fce22fc0949bf6da65612f1145955dee8a5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 01 Sep 2020 23:45:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 01 Sep 2020 23:45:40 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 01 Sep 2020 23:47:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 01 Sep 2020 23:47:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 01 Sep 2020 23:47:50 GMT
EXPOSE 9092
# Tue, 01 Sep 2020 23:48:02 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 01 Sep 2020 23:48:13 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 01 Sep 2020 23:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 23:48:40 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f0d9b28aa1c5027bb432a4fa8f9c76c3c7dc815d224e54d39735fbfdcae54`  
		Last Modified: Wed, 05 Aug 2020 07:15:46 GMT  
		Size: 12.8 MB (12791620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6abe48017537656613ca271869db382fcffed10a4b4717a32df33e5bb642f1`  
		Last Modified: Tue, 01 Sep 2020 23:50:53 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba54e0d0cb21a5dfbb4a8592e0fd9a1dd998cf18eefbe1ce302dbd7b9b40ff2`  
		Last Modified: Tue, 01 Sep 2020 23:50:59 GMT  
		Size: 21.3 MB (21307907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4bd74a477857a67c5d0dedc37e3acba5ae8c7062594be1ad8037af83171741`  
		Last Modified: Tue, 01 Sep 2020 23:50:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5d9b79a2d6fd521f43fa12d4415b0fc66cec00ba6dfb86c2787175afe4f031`  
		Last Modified: Tue, 01 Sep 2020 23:50:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:b89a4566a57903439bd75608aa6479b98b8c10977b52ff2cf909da15cec09d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:0a9930bdc5dbcac1655ad92f5ffee3f3033e6f5dd4293ab49f1b72119faca9be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96239792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859f0e0681aec1931aa3d88f88a76f950b766d3cce976fecb83f99e3efe4aa6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:32:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 00:16:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 00:16:19 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 02 Sep 2020 00:16:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 02 Sep 2020 00:16:23 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 00:16:23 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 00:16:23 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 00:16:23 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 00:16:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:16:24 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d20988f49753a67fbf2842359c77fda4e47ccd36213a864d51fc550cb3d4bfe`  
		Last Modified: Wed, 05 Aug 2020 16:32:54 GMT  
		Size: 13.1 MB (13084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027977b65bfb7d6972f64909f085660f99749c7f9ec0f250bd25700824f5216b`  
		Last Modified: Wed, 02 Sep 2020 00:16:54 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02d5181830a7324de6fbf4a9f98f6b93f4acca3cbf816d8b38e6c28f5976d4d`  
		Last Modified: Wed, 02 Sep 2020 00:16:59 GMT  
		Size: 22.7 MB (22694289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eed621c2e54f16f6b66e3e22bd4590a61f3ae5295b70d7c2bc02e8a7406b7ba`  
		Last Modified: Wed, 02 Sep 2020 00:16:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb16d8c7bbff09b0eed56ec7273e961ab8db20546a24a796fc23a8cb82a768`  
		Last Modified: Wed, 02 Sep 2020 00:16:54 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:ec055017499e04f90f30e60f40a20c8b303bfa44ddb368cfdb5ed44c7f2bc228
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90039712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d457c93f2230ee16f80a0a823df69f0507dad60c6bbfd9908a63f8d1c5bff6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 05:29:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 01:26:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 01:26:09 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 02 Sep 2020 01:26:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 02 Sep 2020 01:26:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 01:26:55 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 01:26:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 01:27:08 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 01:27:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 01:27:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1621cafe44218577f3ed96b59c43d18d81a0d529ca3f3e5f1e20a4b917b5145e`  
		Last Modified: Wed, 05 Aug 2020 05:31:31 GMT  
		Size: 13.3 MB (13254548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ce95cfb70f0ef4517e0dbd22c936087cdb9670b42abcaf5655f09bf2118a29`  
		Last Modified: Wed, 02 Sep 2020 01:29:09 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b73d6dba3081c8634d46467ae114c423b69c9c7b26466a7976b0231b260b5c`  
		Last Modified: Wed, 02 Sep 2020 01:29:18 GMT  
		Size: 21.3 MB (21308099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6855e79b5127189ea26c49e76776807737221b12aee397d53758f8e63d8e7d77`  
		Last Modified: Wed, 02 Sep 2020 01:29:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5295c4bc4fa6e7217fb60feac5c451b057348975fc58fb848ec7653e4e52c9f2`  
		Last Modified: Wed, 02 Sep 2020 01:29:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:dd4908f889386df6541a838e0d88d4e38940036c157f0d4a2fc7a84655159a8b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91069499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36745dfdaf9d7dce714c4c0ad651fce22fc0949bf6da65612f1145955dee8a5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 01 Sep 2020 23:45:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 01 Sep 2020 23:45:40 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 01 Sep 2020 23:47:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 01 Sep 2020 23:47:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 01 Sep 2020 23:47:50 GMT
EXPOSE 9092
# Tue, 01 Sep 2020 23:48:02 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 01 Sep 2020 23:48:13 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 01 Sep 2020 23:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 23:48:40 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f0d9b28aa1c5027bb432a4fa8f9c76c3c7dc815d224e54d39735fbfdcae54`  
		Last Modified: Wed, 05 Aug 2020 07:15:46 GMT  
		Size: 12.8 MB (12791620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6abe48017537656613ca271869db382fcffed10a4b4717a32df33e5bb642f1`  
		Last Modified: Tue, 01 Sep 2020 23:50:53 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba54e0d0cb21a5dfbb4a8592e0fd9a1dd998cf18eefbe1ce302dbd7b9b40ff2`  
		Last Modified: Tue, 01 Sep 2020 23:50:59 GMT  
		Size: 21.3 MB (21307907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4bd74a477857a67c5d0dedc37e3acba5ae8c7062594be1ad8037af83171741`  
		Last Modified: Tue, 01 Sep 2020 23:50:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5d9b79a2d6fd521f43fa12d4415b0fc66cec00ba6dfb86c2787175afe4f031`  
		Last Modified: Tue, 01 Sep 2020 23:50:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:708aa7a25f5d1d6e7feb3f0617bb5aada0ad6f70fa0f35b2439f056864931762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:6c56395b2767b13e4badc4cff8c58cd93e22e0aaeaf1abcd9ed3dcd4246b9caf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19677542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac1c89cbe21ec99362921876624cb874b08322c1d84a951ba836ca3752b693f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:39 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 02 Sep 2020 00:16:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:16:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 00:16:31 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 00:16:31 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 00:16:31 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 02 Sep 2020 00:16:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:16:31 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac836c5a581fe484d430996440a28eecf37316376ba156f051bf920ababfc37`  
		Last Modified: Wed, 02 Sep 2020 00:17:06 GMT  
		Size: 16.6 MB (16598563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77b99c5ea852abc105448a587360b853163d8fcdcd39d44c6d94a729a59ede1`  
		Last Modified: Wed, 02 Sep 2020 00:17:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2bf5aaf0c284238e874e05bf476763b565f10d432d8d47f7b9f3793369ba0`  
		Last Modified: Wed, 02 Sep 2020 00:17:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:708aa7a25f5d1d6e7feb3f0617bb5aada0ad6f70fa0f35b2439f056864931762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:6c56395b2767b13e4badc4cff8c58cd93e22e0aaeaf1abcd9ed3dcd4246b9caf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19677542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac1c89cbe21ec99362921876624cb874b08322c1d84a951ba836ca3752b693f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:39 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 02 Sep 2020 00:16:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 02 Sep 2020 00:16:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 00:16:31 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 00:16:31 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 00:16:31 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 02 Sep 2020 00:16:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:16:31 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac836c5a581fe484d430996440a28eecf37316376ba156f051bf920ababfc37`  
		Last Modified: Wed, 02 Sep 2020 00:17:06 GMT  
		Size: 16.6 MB (16598563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77b99c5ea852abc105448a587360b853163d8fcdcd39d44c6d94a729a59ede1`  
		Last Modified: Wed, 02 Sep 2020 00:17:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2bf5aaf0c284238e874e05bf476763b565f10d432d8d47f7b9f3793369ba0`  
		Last Modified: Wed, 02 Sep 2020 00:17:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:559325bdfe5a070245b868623566b53c596edc3c651de990d5b265c7d068c9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:5d45798cd4faf653c1fce3d5b36e1e9b80b7fbe4e4427624bd4fb6b43e023522
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109958962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7ac689eb303d2aab3e012989ac0cc69f75b5118e6c794c6af305dfba0c5d19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:32:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 00:16:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 00:16:36 GMT
ENV KAPACITOR_VERSION=1.5.6
# Wed, 02 Sep 2020 00:16:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 02 Sep 2020 00:16:39 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 00:16:39 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 00:16:40 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 00:16:40 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 00:16:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:16:40 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d20988f49753a67fbf2842359c77fda4e47ccd36213a864d51fc550cb3d4bfe`  
		Last Modified: Wed, 05 Aug 2020 16:32:54 GMT  
		Size: 13.1 MB (13084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027977b65bfb7d6972f64909f085660f99749c7f9ec0f250bd25700824f5216b`  
		Last Modified: Wed, 02 Sep 2020 00:16:54 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4934195a363c316108ae41af7572d1c23005cb595a01fd5fa2265a2e8efd6a03`  
		Last Modified: Wed, 02 Sep 2020 00:17:14 GMT  
		Size: 36.4 MB (36413460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38db87eda0d309259551c20e5537db53f717924525f4047d785dbbe6e1a62a50`  
		Last Modified: Wed, 02 Sep 2020 00:17:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5e268a43f719d7ad244767f19e687bc3e69edbf48c58e8a372ba2444b005a`  
		Last Modified: Wed, 02 Sep 2020 00:17:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:9ad7a5b703bd0ce99356d3035f499e89724c5b24e346bd110626f4a09a3a0f73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102872446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc97f011f6b7d2c56ce5edbcb657d275770edf808989adcb42226d56e33edf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 05:29:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 01:26:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 01:27:37 GMT
ENV KAPACITOR_VERSION=1.5.6
# Wed, 02 Sep 2020 01:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 02 Sep 2020 01:28:16 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 01:28:23 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 01:28:28 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 01:28:36 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 01:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 01:28:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1621cafe44218577f3ed96b59c43d18d81a0d529ca3f3e5f1e20a4b917b5145e`  
		Last Modified: Wed, 05 Aug 2020 05:31:31 GMT  
		Size: 13.3 MB (13254548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ce95cfb70f0ef4517e0dbd22c936087cdb9670b42abcaf5655f09bf2118a29`  
		Last Modified: Wed, 02 Sep 2020 01:29:09 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710eff24f040100e3f6c39922c5ee8d730545f2f815f30ebc2e984f461285fdb`  
		Last Modified: Wed, 02 Sep 2020 01:29:33 GMT  
		Size: 34.1 MB (34140836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b6d9217bfcb947cdd5e4e93437ed945ab4d508fd193d25c0b11842aa20a186`  
		Last Modified: Wed, 02 Sep 2020 01:29:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95826458684e4341364a3c6a4a2446d97a21c94c433e7a6d778199bbb4b68111`  
		Last Modified: Wed, 02 Sep 2020 01:29:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:59a76e26efe51221b70965526aa4d528206e9c395ded9b03dd0aa73d0e068dc4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103674332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a2ef7e8678582c2e5c418686b90a9fd9a70b0346cb10e2813283c7c3237ca8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 01 Sep 2020 23:45:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 01 Sep 2020 23:49:12 GMT
ENV KAPACITOR_VERSION=1.5.6
# Tue, 01 Sep 2020 23:49:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 01 Sep 2020 23:49:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 01 Sep 2020 23:49:54 GMT
EXPOSE 9092
# Tue, 01 Sep 2020 23:49:58 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 01 Sep 2020 23:50:06 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 01 Sep 2020 23:50:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 23:50:28 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f0d9b28aa1c5027bb432a4fa8f9c76c3c7dc815d224e54d39735fbfdcae54`  
		Last Modified: Wed, 05 Aug 2020 07:15:46 GMT  
		Size: 12.8 MB (12791620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6abe48017537656613ca271869db382fcffed10a4b4717a32df33e5bb642f1`  
		Last Modified: Tue, 01 Sep 2020 23:50:53 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0447c4a8f3b47f2885aa30f652a4224ac9398e9b37e3a8b2e3346583ab503585`  
		Last Modified: Tue, 01 Sep 2020 23:51:16 GMT  
		Size: 33.9 MB (33912740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1386338c8edef2b7ec5b6eea47a21e99dcdddece84746682454261908229bef`  
		Last Modified: Tue, 01 Sep 2020 23:51:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a0345cb5fd32f3b6e465e84618adefabb73a6bb976530d8c8e22b2ff05d6bf`  
		Last Modified: Tue, 01 Sep 2020 23:51:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.6`

```console
$ docker pull kapacitor@sha256:559325bdfe5a070245b868623566b53c596edc3c651de990d5b265c7d068c9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:5d45798cd4faf653c1fce3d5b36e1e9b80b7fbe4e4427624bd4fb6b43e023522
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109958962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7ac689eb303d2aab3e012989ac0cc69f75b5118e6c794c6af305dfba0c5d19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:32:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 00:16:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 00:16:36 GMT
ENV KAPACITOR_VERSION=1.5.6
# Wed, 02 Sep 2020 00:16:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 02 Sep 2020 00:16:39 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 00:16:39 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 00:16:40 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 00:16:40 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 00:16:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:16:40 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d20988f49753a67fbf2842359c77fda4e47ccd36213a864d51fc550cb3d4bfe`  
		Last Modified: Wed, 05 Aug 2020 16:32:54 GMT  
		Size: 13.1 MB (13084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027977b65bfb7d6972f64909f085660f99749c7f9ec0f250bd25700824f5216b`  
		Last Modified: Wed, 02 Sep 2020 00:16:54 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4934195a363c316108ae41af7572d1c23005cb595a01fd5fa2265a2e8efd6a03`  
		Last Modified: Wed, 02 Sep 2020 00:17:14 GMT  
		Size: 36.4 MB (36413460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38db87eda0d309259551c20e5537db53f717924525f4047d785dbbe6e1a62a50`  
		Last Modified: Wed, 02 Sep 2020 00:17:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5e268a43f719d7ad244767f19e687bc3e69edbf48c58e8a372ba2444b005a`  
		Last Modified: Wed, 02 Sep 2020 00:17:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.6` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:9ad7a5b703bd0ce99356d3035f499e89724c5b24e346bd110626f4a09a3a0f73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102872446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc97f011f6b7d2c56ce5edbcb657d275770edf808989adcb42226d56e33edf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 05:29:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 01:26:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 01:27:37 GMT
ENV KAPACITOR_VERSION=1.5.6
# Wed, 02 Sep 2020 01:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 02 Sep 2020 01:28:16 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 01:28:23 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 01:28:28 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 01:28:36 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 01:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 01:28:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1621cafe44218577f3ed96b59c43d18d81a0d529ca3f3e5f1e20a4b917b5145e`  
		Last Modified: Wed, 05 Aug 2020 05:31:31 GMT  
		Size: 13.3 MB (13254548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ce95cfb70f0ef4517e0dbd22c936087cdb9670b42abcaf5655f09bf2118a29`  
		Last Modified: Wed, 02 Sep 2020 01:29:09 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710eff24f040100e3f6c39922c5ee8d730545f2f815f30ebc2e984f461285fdb`  
		Last Modified: Wed, 02 Sep 2020 01:29:33 GMT  
		Size: 34.1 MB (34140836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b6d9217bfcb947cdd5e4e93437ed945ab4d508fd193d25c0b11842aa20a186`  
		Last Modified: Wed, 02 Sep 2020 01:29:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95826458684e4341364a3c6a4a2446d97a21c94c433e7a6d778199bbb4b68111`  
		Last Modified: Wed, 02 Sep 2020 01:29:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:59a76e26efe51221b70965526aa4d528206e9c395ded9b03dd0aa73d0e068dc4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103674332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a2ef7e8678582c2e5c418686b90a9fd9a70b0346cb10e2813283c7c3237ca8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 01 Sep 2020 23:45:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 01 Sep 2020 23:49:12 GMT
ENV KAPACITOR_VERSION=1.5.6
# Tue, 01 Sep 2020 23:49:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 01 Sep 2020 23:49:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 01 Sep 2020 23:49:54 GMT
EXPOSE 9092
# Tue, 01 Sep 2020 23:49:58 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 01 Sep 2020 23:50:06 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 01 Sep 2020 23:50:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 23:50:28 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f0d9b28aa1c5027bb432a4fa8f9c76c3c7dc815d224e54d39735fbfdcae54`  
		Last Modified: Wed, 05 Aug 2020 07:15:46 GMT  
		Size: 12.8 MB (12791620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6abe48017537656613ca271869db382fcffed10a4b4717a32df33e5bb642f1`  
		Last Modified: Tue, 01 Sep 2020 23:50:53 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0447c4a8f3b47f2885aa30f652a4224ac9398e9b37e3a8b2e3346583ab503585`  
		Last Modified: Tue, 01 Sep 2020 23:51:16 GMT  
		Size: 33.9 MB (33912740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1386338c8edef2b7ec5b6eea47a21e99dcdddece84746682454261908229bef`  
		Last Modified: Tue, 01 Sep 2020 23:51:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a0345cb5fd32f3b6e465e84618adefabb73a6bb976530d8c8e22b2ff05d6bf`  
		Last Modified: Tue, 01 Sep 2020 23:51:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.6-alpine`

```console
$ docker pull kapacitor@sha256:e13d762dc05f1585b17dceb938b2fc30661fc57b2f29699df5015dac2962cc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e577ecfb27902c925b03d76786b7f477affe6f0ed7310ff6ff4224bccf19e7b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23148296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e401a876d017d93823ee93ca22ec6e515bcebfbb929929211da5eb797214d1eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:56 GMT
ENV KAPACITOR_VERSION=1.5.6
# Tue, 01 Sep 2020 01:04:59 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 01 Sep 2020 01:05:00 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 01 Sep 2020 01:05:00 GMT
EXPOSE 9092
# Tue, 01 Sep 2020 01:05:00 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 01 Sep 2020 01:05:00 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Tue, 01 Sep 2020 01:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 01:05:01 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31df2231b553fd7994ed64b2dfc3704987ebfb21f3ba5c387b461745fa82e955`  
		Last Modified: Tue, 01 Sep 2020 01:05:33 GMT  
		Size: 20.1 MB (20069318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107199fa9da95b44b85e7b328420539c2ade672af6acb224da3cb36e8d02197`  
		Last Modified: Tue, 01 Sep 2020 01:05:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f82e6b4fcb385fac50349ebfc38fb2054f5ce7a3b39b9d1245c4e79da236b4`  
		Last Modified: Tue, 01 Sep 2020 01:05:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:e13d762dc05f1585b17dceb938b2fc30661fc57b2f29699df5015dac2962cc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e577ecfb27902c925b03d76786b7f477affe6f0ed7310ff6ff4224bccf19e7b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23148296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e401a876d017d93823ee93ca22ec6e515bcebfbb929929211da5eb797214d1eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:56 GMT
ENV KAPACITOR_VERSION=1.5.6
# Tue, 01 Sep 2020 01:04:59 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 01 Sep 2020 01:05:00 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 01 Sep 2020 01:05:00 GMT
EXPOSE 9092
# Tue, 01 Sep 2020 01:05:00 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 01 Sep 2020 01:05:00 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Tue, 01 Sep 2020 01:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 01:05:01 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31df2231b553fd7994ed64b2dfc3704987ebfb21f3ba5c387b461745fa82e955`  
		Last Modified: Tue, 01 Sep 2020 01:05:33 GMT  
		Size: 20.1 MB (20069318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107199fa9da95b44b85e7b328420539c2ade672af6acb224da3cb36e8d02197`  
		Last Modified: Tue, 01 Sep 2020 01:05:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f82e6b4fcb385fac50349ebfc38fb2054f5ce7a3b39b9d1245c4e79da236b4`  
		Last Modified: Tue, 01 Sep 2020 01:05:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:e13d762dc05f1585b17dceb938b2fc30661fc57b2f29699df5015dac2962cc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e577ecfb27902c925b03d76786b7f477affe6f0ed7310ff6ff4224bccf19e7b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23148296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e401a876d017d93823ee93ca22ec6e515bcebfbb929929211da5eb797214d1eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:38:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:04:56 GMT
ENV KAPACITOR_VERSION=1.5.6
# Tue, 01 Sep 2020 01:04:59 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 01 Sep 2020 01:05:00 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 01 Sep 2020 01:05:00 GMT
EXPOSE 9092
# Tue, 01 Sep 2020 01:05:00 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 01 Sep 2020 01:05:00 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Tue, 01 Sep 2020 01:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 01:05:01 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61626b3b2d7f1da2eb5ae3486f7e2baf21fb5b7dd993595b8fe0fbe2a34445d6`  
		Last Modified: Tue, 01 Sep 2020 00:39:25 GMT  
		Size: 280.8 KB (280831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31df2231b553fd7994ed64b2dfc3704987ebfb21f3ba5c387b461745fa82e955`  
		Last Modified: Tue, 01 Sep 2020 01:05:33 GMT  
		Size: 20.1 MB (20069318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107199fa9da95b44b85e7b328420539c2ade672af6acb224da3cb36e8d02197`  
		Last Modified: Tue, 01 Sep 2020 01:05:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f82e6b4fcb385fac50349ebfc38fb2054f5ce7a3b39b9d1245c4e79da236b4`  
		Last Modified: Tue, 01 Sep 2020 01:05:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:559325bdfe5a070245b868623566b53c596edc3c651de990d5b265c7d068c9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:5d45798cd4faf653c1fce3d5b36e1e9b80b7fbe4e4427624bd4fb6b43e023522
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109958962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7ac689eb303d2aab3e012989ac0cc69f75b5118e6c794c6af305dfba0c5d19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:32:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 00:16:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 00:16:36 GMT
ENV KAPACITOR_VERSION=1.5.6
# Wed, 02 Sep 2020 00:16:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 02 Sep 2020 00:16:39 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 00:16:39 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 00:16:40 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 00:16:40 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 00:16:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 00:16:40 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d20988f49753a67fbf2842359c77fda4e47ccd36213a864d51fc550cb3d4bfe`  
		Last Modified: Wed, 05 Aug 2020 16:32:54 GMT  
		Size: 13.1 MB (13084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027977b65bfb7d6972f64909f085660f99749c7f9ec0f250bd25700824f5216b`  
		Last Modified: Wed, 02 Sep 2020 00:16:54 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4934195a363c316108ae41af7572d1c23005cb595a01fd5fa2265a2e8efd6a03`  
		Last Modified: Wed, 02 Sep 2020 00:17:14 GMT  
		Size: 36.4 MB (36413460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38db87eda0d309259551c20e5537db53f717924525f4047d785dbbe6e1a62a50`  
		Last Modified: Wed, 02 Sep 2020 00:17:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5e268a43f719d7ad244767f19e687bc3e69edbf48c58e8a372ba2444b005a`  
		Last Modified: Wed, 02 Sep 2020 00:17:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:9ad7a5b703bd0ce99356d3035f499e89724c5b24e346bd110626f4a09a3a0f73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102872446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc97f011f6b7d2c56ce5edbcb657d275770edf808989adcb42226d56e33edf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 05:29:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 Sep 2020 01:26:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 Sep 2020 01:27:37 GMT
ENV KAPACITOR_VERSION=1.5.6
# Wed, 02 Sep 2020 01:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 02 Sep 2020 01:28:16 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 02 Sep 2020 01:28:23 GMT
EXPOSE 9092
# Wed, 02 Sep 2020 01:28:28 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 Sep 2020 01:28:36 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 02 Sep 2020 01:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Sep 2020 01:28:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1621cafe44218577f3ed96b59c43d18d81a0d529ca3f3e5f1e20a4b917b5145e`  
		Last Modified: Wed, 05 Aug 2020 05:31:31 GMT  
		Size: 13.3 MB (13254548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ce95cfb70f0ef4517e0dbd22c936087cdb9670b42abcaf5655f09bf2118a29`  
		Last Modified: Wed, 02 Sep 2020 01:29:09 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710eff24f040100e3f6c39922c5ee8d730545f2f815f30ebc2e984f461285fdb`  
		Last Modified: Wed, 02 Sep 2020 01:29:33 GMT  
		Size: 34.1 MB (34140836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b6d9217bfcb947cdd5e4e93437ed945ab4d508fd193d25c0b11842aa20a186`  
		Last Modified: Wed, 02 Sep 2020 01:29:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95826458684e4341364a3c6a4a2446d97a21c94c433e7a6d778199bbb4b68111`  
		Last Modified: Wed, 02 Sep 2020 01:29:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:59a76e26efe51221b70965526aa4d528206e9c395ded9b03dd0aa73d0e068dc4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103674332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a2ef7e8678582c2e5c418686b90a9fd9a70b0346cb10e2813283c7c3237ca8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 07:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 01 Sep 2020 23:45:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 01 Sep 2020 23:49:12 GMT
ENV KAPACITOR_VERSION=1.5.6
# Tue, 01 Sep 2020 23:49:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 01 Sep 2020 23:49:53 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 01 Sep 2020 23:49:54 GMT
EXPOSE 9092
# Tue, 01 Sep 2020 23:49:58 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 01 Sep 2020 23:50:06 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 01 Sep 2020 23:50:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 23:50:28 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f0d9b28aa1c5027bb432a4fa8f9c76c3c7dc815d224e54d39735fbfdcae54`  
		Last Modified: Wed, 05 Aug 2020 07:15:46 GMT  
		Size: 12.8 MB (12791620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6abe48017537656613ca271869db382fcffed10a4b4717a32df33e5bb642f1`  
		Last Modified: Tue, 01 Sep 2020 23:50:53 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0447c4a8f3b47f2885aa30f652a4224ac9398e9b37e3a8b2e3346583ab503585`  
		Last Modified: Tue, 01 Sep 2020 23:51:16 GMT  
		Size: 33.9 MB (33912740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1386338c8edef2b7ec5b6eea47a21e99dcdddece84746682454261908229bef`  
		Last Modified: Tue, 01 Sep 2020 23:51:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a0345cb5fd32f3b6e465e84618adefabb73a6bb976530d8c8e22b2ff05d6bf`  
		Last Modified: Tue, 01 Sep 2020 23:51:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
