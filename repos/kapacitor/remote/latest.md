## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:7ca9841052d79c42fc55744df1c8a3c4628455af55cf0e2e802806f7d526d2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:c11f17dd18be88f37051ce3f83de15da8271027a11bca96c00461a17390e596d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133609177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdcd91b8c7b48c316f0bc0eb809ca839159ea40d3b65364ad820d0cdf0440e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:33 GMT
ADD file:835effce8521d3a6cb00dc8bb358711e7a6ba1fd057b798681d9e006825dd3c1 in / 
# Fri, 03 Sep 2021 01:23:33 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:36:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Sep 2021 09:18:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 04 Sep 2021 09:18:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 04 Sep 2021 09:18:51 GMT
ENV KAPACITOR_VERSION=1.6.1
# Sat, 04 Sep 2021 09:18:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 04 Sep 2021 09:18:57 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 04 Sep 2021 09:18:58 GMT
EXPOSE 9092
# Sat, 04 Sep 2021 09:18:58 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 04 Sep 2021 09:18:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 04 Sep 2021 09:18:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 09:18:58 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c05d83e138cea8cb6ddd17442ab2138423db80e58408d93059f2ea25065952e`  
		Last Modified: Fri, 03 Sep 2021 01:31:39 GMT  
		Size: 45.4 MB (45379797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394ee1959bac9492a9fc64334844549eccd4274280678d81d6b5b19af703e2a6`  
		Last Modified: Fri, 03 Sep 2021 06:42:58 GMT  
		Size: 11.3 MB (11295763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f175d1abbc6d4a7774bd2912a927aa78b90fb04fb43d591e3dda317c9bb96`  
		Last Modified: Fri, 03 Sep 2021 06:42:57 GMT  
		Size: 4.3 MB (4342391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96751b59d3825c066fe0b32c1411674b9b506ce92a115a446826d43b73a2e2f0`  
		Last Modified: Sat, 04 Sep 2021 09:19:20 GMT  
		Size: 13.3 MB (13325864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0bf8615443fb9e9e2d73c057719cb6942a9cf30264fdde513df2b95dff5dbf`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dfd66f818a41df9fa56676b83a9589b4113020628850279f0728763a4141bd`  
		Last Modified: Sat, 04 Sep 2021 09:19:43 GMT  
		Size: 59.3 MB (59262050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f619b25d6c94fb25c90635e3cba8b315eeae743d0b3db37e46659c0225a6ce`  
		Last Modified: Sat, 04 Sep 2021 09:19:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3772a60126f73b598f830c24fd6ffe2d2298c8be96913f64908180f023c3d8b1`  
		Last Modified: Sat, 04 Sep 2021 09:19:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9c52d55020a0c2fa3865cb9dad8aa1ba1902489d2f9c80827fabbc6da7c847a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126415227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e10e46e4144963c60e7c7c17197934352599c247f881567f6d5b5c738ff3f4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:34 GMT
ADD file:3a77488ae0a72e8fd504cb1354bd111f38a4fc9f3e541ee7ebce3ebc4eb9dc49 in / 
# Fri, 03 Sep 2021 00:42:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:36:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 21:07:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 03 Sep 2021 21:08:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 21:08:20 GMT
ENV KAPACITOR_VERSION=1.6.1
# Fri, 03 Sep 2021 21:08:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 03 Sep 2021 21:08:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 03 Sep 2021 21:08:26 GMT
EXPOSE 9092
# Fri, 03 Sep 2021 21:08:26 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 03 Sep 2021 21:08:27 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 03 Sep 2021 21:08:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 21:08:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e98a9e31e599c3e38ecd12cf6b8493f4268c371026bae6d2280da418009b5bff`  
		Last Modified: Fri, 03 Sep 2021 00:52:57 GMT  
		Size: 43.2 MB (43177996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f698e334a0e8a436e04b2ef344b0ada5761244cf05829ece406e740b750b1bfa`  
		Last Modified: Fri, 03 Sep 2021 04:44:45 GMT  
		Size: 10.2 MB (10215862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eef9137c22a6fa0d9b497479b8c3ba0d211b5f01fafd237e4dc3419146e22a`  
		Last Modified: Fri, 03 Sep 2021 04:44:44 GMT  
		Size: 4.1 MB (4096542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524ec54ce2cc3514ffe7ba394bc8e3c9e9ba04493c6ba234d8be1645f4d4123`  
		Last Modified: Fri, 03 Sep 2021 21:08:49 GMT  
		Size: 13.0 MB (13027371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6cba0468ee4e125ab0563615edf0f8999ef3a0275f4b80211c9cb7f22a5f0`  
		Last Modified: Fri, 03 Sep 2021 21:08:47 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f4dc5d2890c4f7d452390bfbcaf4a6c6c01fc1870bff8a9678760d952ecc49`  
		Last Modified: Fri, 03 Sep 2021 21:09:13 GMT  
		Size: 55.9 MB (55894146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4acf031730b9c6909438592b19bd91c23eca189ea86a1e3aabc0f5434ca0e2`  
		Last Modified: Fri, 03 Sep 2021 21:09:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644a9eee361d6a8dd6c4324eaf8711e568e3f33c386174866840c15bbfcc1863`  
		Last Modified: Fri, 03 Sep 2021 21:09:04 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
