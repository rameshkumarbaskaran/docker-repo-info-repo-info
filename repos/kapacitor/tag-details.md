<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5.7`](#kapacitor157)
-	[`kapacitor:1.5.7-alpine`](#kapacitor157-alpine)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:313ba223874a8c5905e3f508a2e327c78852721f315d4d6c5d3bb1e89e7ef046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:da236ecc8536176ab609f0dfe5b9f539af1914701a5c1cc742b6869c6f647e13
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96329588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0394f0b9e5139c5669ce7ecaef5d7256c03707d68f6e81c860da87f24f8189b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:27:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 13 Oct 2020 23:28:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:28:01 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 13 Oct 2020 23:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 23:28:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 13 Oct 2020 23:28:06 GMT
EXPOSE 9092
# Tue, 13 Oct 2020 23:28:06 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 13 Oct 2020 23:28:06 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 13 Oct 2020 23:28:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:28:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddcd7b1d32dba2ff27539e272b23ef5c09f4b3777b1fd6cdca8cca7ce6c0254`  
		Last Modified: Tue, 13 Oct 2020 23:28:40 GMT  
		Size: 13.2 MB (13173587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8620385d89b76a759c4d7ced3d2e60ab0f02b6e0014a283611307a6c53b413c7`  
		Last Modified: Tue, 13 Oct 2020 23:28:37 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd176e0f54ed36d638b0ab701bc5316f26f9f7e63e14f5bf468b6b2507c51a9d`  
		Last Modified: Tue, 13 Oct 2020 23:28:45 GMT  
		Size: 22.7 MB (22694289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a1da1489019f2bce0f489f55967f265a3ee2db58b299352c8b537c0685c4f5`  
		Last Modified: Tue, 13 Oct 2020 23:28:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a499ebbb20658a39eefca568648bfed439c82601882d414c8197ea121eea61f`  
		Last Modified: Tue, 13 Oct 2020 23:28:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:1fd51a7bba4a6deb9539a7a948d766cd3bc470f90f561b57baff023a26e0ba4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90209420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa161de47dc35d30908b01b31e29591c3c62d3318ddc88c369d7e1145d125ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:47 GMT
ADD file:58b80132bbfb3cae1eb2a9345e362cce1e39de41055fdcef8e5a8a8a447f69b0 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:57:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:57:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:28:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 19:28:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:28:19 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 18 Nov 2020 19:28:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 19:28:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 19:28:27 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 19:28:27 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 19:28:28 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 19:28:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:28:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cfc77fa15d772230821249f78cfbb69a8fc6596f6867601b9dad16aedb424325`  
		Last Modified: Tue, 17 Nov 2020 20:35:24 GMT  
		Size: 42.1 MB (42117734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1d24dbd0f85452f20a934ea14ebc3dadfdd8493317dfe8f7f2aa1772937953`  
		Last Modified: Tue, 17 Nov 2020 22:12:47 GMT  
		Size: 9.4 MB (9444101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90255e5a0a934b36df89ac1c1842d07d8d7ed4b3531898af64fdab8372662e3e`  
		Last Modified: Tue, 17 Nov 2020 22:12:46 GMT  
		Size: 3.9 MB (3919908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2039951b2be730d749377ed10abb75898d5083ea38568d8cd4972e7a791e8a34`  
		Last Modified: Wed, 18 Nov 2020 19:29:07 GMT  
		Size: 13.4 MB (13416267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4f166820e128a7f6172218770b80b3de48fe84639f56364ba3200ca580822e`  
		Last Modified: Wed, 18 Nov 2020 19:29:05 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6262df5e229150558930d8efc235d2c2e58db3534a95b643e82010d794742e1c`  
		Last Modified: Wed, 18 Nov 2020 19:29:12 GMT  
		Size: 21.3 MB (21308100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e1ec912c7b5c64bfc55449664e24b23c75e0fa4c13e90d818bb31aa7d69e83`  
		Last Modified: Wed, 18 Nov 2020 19:29:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e076640b3196e40522338e9b7c54aaea80468e964514ca4d217cdb2f6f8aaf0`  
		Last Modified: Wed, 18 Nov 2020 19:29:05 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:3916c73f5ba4c32ae47bea8722f22af38051805bc8d57326f4a16c78db75522f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91197712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7d2880c5eb1442b3e42d4a9e2254d4f75bfffd663825f9ecc38b51f0a29b13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:28:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 21:15:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:15:01 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 18 Nov 2020 21:15:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 21:15:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 21:15:08 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 21:15:09 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 21:15:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 21:15:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:15:11 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9b3adbe4ac4ca73818d8b79e94d2ff2b6ceafc1225d7c036ec4d384f0804a`  
		Last Modified: Tue, 17 Nov 2020 22:40:38 GMT  
		Size: 9.7 MB (9702292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052ba804da6ef34fd9dddf0ca298b1e0551ac8cf3ea14fc371fa1fa51cbd7f7c`  
		Last Modified: Tue, 17 Nov 2020 22:40:36 GMT  
		Size: 4.1 MB (4095219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d0115aaf8aea01788d62c5180c53c44f5b525f2a9dddfd2859576f55f219b`  
		Last Modified: Wed, 18 Nov 2020 21:15:45 GMT  
		Size: 12.9 MB (12912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f61bf00eecdaa1ba088593162e6892a588b4bdebc909c2cbf006fe9d2b0332a`  
		Last Modified: Wed, 18 Nov 2020 21:15:42 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c933cf9017283815ffdb326dc7a95075238243af1c7fd53f4c61817e3703dc3`  
		Last Modified: Wed, 18 Nov 2020 21:15:50 GMT  
		Size: 21.3 MB (21307888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d548a97c64cd97d4e4ba9b7d50b22f6f935279941bf7f54c467c5bb34c00cddc`  
		Last Modified: Wed, 18 Nov 2020 21:15:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4c8e7573c067a188b43422916a291461da80c7cfd0294df4201b42235318b`  
		Last Modified: Wed, 18 Nov 2020 21:15:44 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:313ba223874a8c5905e3f508a2e327c78852721f315d4d6c5d3bb1e89e7ef046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:da236ecc8536176ab609f0dfe5b9f539af1914701a5c1cc742b6869c6f647e13
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96329588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0394f0b9e5139c5669ce7ecaef5d7256c03707d68f6e81c860da87f24f8189b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:27:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 13 Oct 2020 23:28:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 13 Oct 2020 23:28:01 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 13 Oct 2020 23:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 13 Oct 2020 23:28:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 13 Oct 2020 23:28:06 GMT
EXPOSE 9092
# Tue, 13 Oct 2020 23:28:06 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 13 Oct 2020 23:28:06 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 13 Oct 2020 23:28:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 23:28:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddcd7b1d32dba2ff27539e272b23ef5c09f4b3777b1fd6cdca8cca7ce6c0254`  
		Last Modified: Tue, 13 Oct 2020 23:28:40 GMT  
		Size: 13.2 MB (13173587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8620385d89b76a759c4d7ced3d2e60ab0f02b6e0014a283611307a6c53b413c7`  
		Last Modified: Tue, 13 Oct 2020 23:28:37 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd176e0f54ed36d638b0ab701bc5316f26f9f7e63e14f5bf468b6b2507c51a9d`  
		Last Modified: Tue, 13 Oct 2020 23:28:45 GMT  
		Size: 22.7 MB (22694289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a1da1489019f2bce0f489f55967f265a3ee2db58b299352c8b537c0685c4f5`  
		Last Modified: Tue, 13 Oct 2020 23:28:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a499ebbb20658a39eefca568648bfed439c82601882d414c8197ea121eea61f`  
		Last Modified: Tue, 13 Oct 2020 23:28:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:1fd51a7bba4a6deb9539a7a948d766cd3bc470f90f561b57baff023a26e0ba4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90209420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa161de47dc35d30908b01b31e29591c3c62d3318ddc88c369d7e1145d125ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:47 GMT
ADD file:58b80132bbfb3cae1eb2a9345e362cce1e39de41055fdcef8e5a8a8a447f69b0 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:57:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:57:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:28:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 19:28:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:28:19 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 18 Nov 2020 19:28:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 19:28:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 19:28:27 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 19:28:27 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 19:28:28 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 19:28:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:28:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cfc77fa15d772230821249f78cfbb69a8fc6596f6867601b9dad16aedb424325`  
		Last Modified: Tue, 17 Nov 2020 20:35:24 GMT  
		Size: 42.1 MB (42117734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1d24dbd0f85452f20a934ea14ebc3dadfdd8493317dfe8f7f2aa1772937953`  
		Last Modified: Tue, 17 Nov 2020 22:12:47 GMT  
		Size: 9.4 MB (9444101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90255e5a0a934b36df89ac1c1842d07d8d7ed4b3531898af64fdab8372662e3e`  
		Last Modified: Tue, 17 Nov 2020 22:12:46 GMT  
		Size: 3.9 MB (3919908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2039951b2be730d749377ed10abb75898d5083ea38568d8cd4972e7a791e8a34`  
		Last Modified: Wed, 18 Nov 2020 19:29:07 GMT  
		Size: 13.4 MB (13416267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4f166820e128a7f6172218770b80b3de48fe84639f56364ba3200ca580822e`  
		Last Modified: Wed, 18 Nov 2020 19:29:05 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6262df5e229150558930d8efc235d2c2e58db3534a95b643e82010d794742e1c`  
		Last Modified: Wed, 18 Nov 2020 19:29:12 GMT  
		Size: 21.3 MB (21308100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e1ec912c7b5c64bfc55449664e24b23c75e0fa4c13e90d818bb31aa7d69e83`  
		Last Modified: Wed, 18 Nov 2020 19:29:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e076640b3196e40522338e9b7c54aaea80468e964514ca4d217cdb2f6f8aaf0`  
		Last Modified: Wed, 18 Nov 2020 19:29:05 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:3916c73f5ba4c32ae47bea8722f22af38051805bc8d57326f4a16c78db75522f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91197712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7d2880c5eb1442b3e42d4a9e2254d4f75bfffd663825f9ecc38b51f0a29b13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:28:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 21:15:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:15:01 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 18 Nov 2020 21:15:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 18 Nov 2020 21:15:07 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 21:15:08 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 21:15:09 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 21:15:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 21:15:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:15:11 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9b3adbe4ac4ca73818d8b79e94d2ff2b6ceafc1225d7c036ec4d384f0804a`  
		Last Modified: Tue, 17 Nov 2020 22:40:38 GMT  
		Size: 9.7 MB (9702292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052ba804da6ef34fd9dddf0ca298b1e0551ac8cf3ea14fc371fa1fa51cbd7f7c`  
		Last Modified: Tue, 17 Nov 2020 22:40:36 GMT  
		Size: 4.1 MB (4095219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d0115aaf8aea01788d62c5180c53c44f5b525f2a9dddfd2859576f55f219b`  
		Last Modified: Wed, 18 Nov 2020 21:15:45 GMT  
		Size: 12.9 MB (12912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f61bf00eecdaa1ba088593162e6892a588b4bdebc909c2cbf006fe9d2b0332a`  
		Last Modified: Wed, 18 Nov 2020 21:15:42 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c933cf9017283815ffdb326dc7a95075238243af1c7fd53f4c61817e3703dc3`  
		Last Modified: Wed, 18 Nov 2020 21:15:50 GMT  
		Size: 21.3 MB (21307888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d548a97c64cd97d4e4ba9b7d50b22f6f935279941bf7f54c467c5bb34c00cddc`  
		Last Modified: Wed, 18 Nov 2020 21:15:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4c8e7573c067a188b43422916a291461da80c7cfd0294df4201b42235318b`  
		Last Modified: Wed, 18 Nov 2020 21:15:44 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:257f369add6955f5416b94294518b299039f0f9540a393e6c6a3a0c117599b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:885d696bbfe8429f088a140814b551d96aaacf768e208b7c145709a924d27324
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19676809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93864a1bae7155066b80a99ea2c63111568576393ed3fd05d85c917bd0f28b2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:55:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:41:59 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 22 Oct 2020 04:42:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:42:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 22 Oct 2020 04:42:05 GMT
EXPOSE 9092
# Thu, 22 Oct 2020 04:42:05 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 22 Oct 2020 04:42:06 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 22 Oct 2020 04:42:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:42:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea603847a3b82b32a20eba9b8d97e8d5da78d7491d9412b148947a123d8c4ffd`  
		Last Modified: Thu, 22 Oct 2020 02:56:04 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf3e77e1e9247969c5b16910f9a4898ae6394a57c4a80d461025d0827b8b063`  
		Last Modified: Thu, 22 Oct 2020 04:42:47 GMT  
		Size: 16.6 MB (16598530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24678d04efb6505bb143989463be8957b4b66b02e026a6c8eb24c9ed47647a4`  
		Last Modified: Thu, 22 Oct 2020 04:42:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1e246c068c706db512c1a7e860bc30daa7fe7ac618ab959bdc9cdde44181cf`  
		Last Modified: Thu, 22 Oct 2020 04:42:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:257f369add6955f5416b94294518b299039f0f9540a393e6c6a3a0c117599b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:885d696bbfe8429f088a140814b551d96aaacf768e208b7c145709a924d27324
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19676809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93864a1bae7155066b80a99ea2c63111568576393ed3fd05d85c917bd0f28b2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:55:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 22 Oct 2020 04:41:59 GMT
ENV KAPACITOR_VERSION=1.4.1
# Thu, 22 Oct 2020 04:42:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 22 Oct 2020 04:42:05 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 22 Oct 2020 04:42:05 GMT
EXPOSE 9092
# Thu, 22 Oct 2020 04:42:05 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 22 Oct 2020 04:42:06 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 22 Oct 2020 04:42:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Oct 2020 04:42:06 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea603847a3b82b32a20eba9b8d97e8d5da78d7491d9412b148947a123d8c4ffd`  
		Last Modified: Thu, 22 Oct 2020 02:56:04 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf3e77e1e9247969c5b16910f9a4898ae6394a57c4a80d461025d0827b8b063`  
		Last Modified: Thu, 22 Oct 2020 04:42:47 GMT  
		Size: 16.6 MB (16598530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24678d04efb6505bb143989463be8957b4b66b02e026a6c8eb24c9ed47647a4`  
		Last Modified: Thu, 22 Oct 2020 04:42:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1e246c068c706db512c1a7e860bc30daa7fe7ac618ab959bdc9cdde44181cf`  
		Last Modified: Thu, 22 Oct 2020 04:42:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:47232cec363506128b66e4d17410505ba9398a6cef5dbeca04f3e7b5e82031c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:9e0e736b570a93a7323df6f7e77e31714a1c747423b69a2677b030206e1f2e47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110089906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8633002ed21494f7233dcc93e74874bf6808978caa138675de4791e7962bf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:27:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 13 Oct 2020 23:28:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Mon, 16 Nov 2020 19:25:10 GMT
ENV KAPACITOR_VERSION=1.5.7
# Mon, 16 Nov 2020 19:25:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 16 Nov 2020 19:25:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 16 Nov 2020 19:25:14 GMT
EXPOSE 9092
# Mon, 16 Nov 2020 19:25:14 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 16 Nov 2020 19:25:14 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 16 Nov 2020 19:25:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Nov 2020 19:25:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddcd7b1d32dba2ff27539e272b23ef5c09f4b3777b1fd6cdca8cca7ce6c0254`  
		Last Modified: Tue, 13 Oct 2020 23:28:40 GMT  
		Size: 13.2 MB (13173587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8620385d89b76a759c4d7ced3d2e60ab0f02b6e0014a283611307a6c53b413c7`  
		Last Modified: Tue, 13 Oct 2020 23:28:37 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef715b38d07da58ce4193c1355aed097e099f378fa90e648801c81cd853ffaf0`  
		Last Modified: Mon, 16 Nov 2020 19:25:43 GMT  
		Size: 36.5 MB (36454607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d308844fbb1ca81e41af5932cad72ee0ab598d58e94c841a1490b101a6540f2c`  
		Last Modified: Mon, 16 Nov 2020 19:25:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d0659a36907a18faa571a1ba169a1d4f397a3713b4e6eca5e373b6409f68af`  
		Last Modified: Mon, 16 Nov 2020 19:25:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:dbb5d180da09ac439451e3369f70c982ec0e10fcd75a7caf3aa8fbdf337fcafa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103073367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dc9158c2d49677fe79ba913d3232b5adcc4ef71510d07943f703226157278a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:47 GMT
ADD file:58b80132bbfb3cae1eb2a9345e362cce1e39de41055fdcef8e5a8a8a447f69b0 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:57:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:57:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:28:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 19:28:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:28:39 GMT
ENV KAPACITOR_VERSION=1.5.7
# Wed, 18 Nov 2020 19:28:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 19:28:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 19:28:48 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 19:28:49 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 19:28:50 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 19:28:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:28:52 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cfc77fa15d772230821249f78cfbb69a8fc6596f6867601b9dad16aedb424325`  
		Last Modified: Tue, 17 Nov 2020 20:35:24 GMT  
		Size: 42.1 MB (42117734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1d24dbd0f85452f20a934ea14ebc3dadfdd8493317dfe8f7f2aa1772937953`  
		Last Modified: Tue, 17 Nov 2020 22:12:47 GMT  
		Size: 9.4 MB (9444101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90255e5a0a934b36df89ac1c1842d07d8d7ed4b3531898af64fdab8372662e3e`  
		Last Modified: Tue, 17 Nov 2020 22:12:46 GMT  
		Size: 3.9 MB (3919908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2039951b2be730d749377ed10abb75898d5083ea38568d8cd4972e7a791e8a34`  
		Last Modified: Wed, 18 Nov 2020 19:29:07 GMT  
		Size: 13.4 MB (13416267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4f166820e128a7f6172218770b80b3de48fe84639f56364ba3200ca580822e`  
		Last Modified: Wed, 18 Nov 2020 19:29:05 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0142c470d43c630e19772a73a56985e7d1b5bc8d58598800e20b062778901ee6`  
		Last Modified: Wed, 18 Nov 2020 19:29:28 GMT  
		Size: 34.2 MB (34172045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21079ad338808a272865afc17d11c43928a709bc37e13236b7fae0eda714711c`  
		Last Modified: Wed, 18 Nov 2020 19:29:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cad50e60a834d8bdd7201d17c37a51f596df750b0b8d94b9e6cb2ccc27fa3`  
		Last Modified: Wed, 18 Nov 2020 19:29:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5b20fed30b4e8c9f89c0dad6d8d172e1d76fad60cf53706bf54fe8b031f81c56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103862482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430779a890d64071bec0487e68fc1ccc6a775930a8edd400d8d3d2c8d58dd693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:28:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 21:15:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:15:19 GMT
ENV KAPACITOR_VERSION=1.5.7
# Wed, 18 Nov 2020 21:15:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 21:15:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 21:15:27 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 21:15:27 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 21:15:28 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 21:15:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:15:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9b3adbe4ac4ca73818d8b79e94d2ff2b6ceafc1225d7c036ec4d384f0804a`  
		Last Modified: Tue, 17 Nov 2020 22:40:38 GMT  
		Size: 9.7 MB (9702292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052ba804da6ef34fd9dddf0ca298b1e0551ac8cf3ea14fc371fa1fa51cbd7f7c`  
		Last Modified: Tue, 17 Nov 2020 22:40:36 GMT  
		Size: 4.1 MB (4095219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d0115aaf8aea01788d62c5180c53c44f5b525f2a9dddfd2859576f55f219b`  
		Last Modified: Wed, 18 Nov 2020 21:15:45 GMT  
		Size: 12.9 MB (12912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f61bf00eecdaa1ba088593162e6892a588b4bdebc909c2cbf006fe9d2b0332a`  
		Last Modified: Wed, 18 Nov 2020 21:15:42 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8814f25006190778f6d5c4c287f922d620ed7720f89d70b0be24eb7f1db4f0`  
		Last Modified: Wed, 18 Nov 2020 21:16:05 GMT  
		Size: 34.0 MB (33972658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b1a95a3f1063ac127f86a44a5a9cd8a68d6de59df05c3d9455088ddbceab29`  
		Last Modified: Wed, 18 Nov 2020 21:15:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57e1ccfd78a9919f64e08d48f8712b319bf7c4e2058563501c2aa3e4bc640fb`  
		Last Modified: Wed, 18 Nov 2020 21:15:58 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.7`

```console
$ docker pull kapacitor@sha256:47232cec363506128b66e4d17410505ba9398a6cef5dbeca04f3e7b5e82031c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:9e0e736b570a93a7323df6f7e77e31714a1c747423b69a2677b030206e1f2e47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110089906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8633002ed21494f7233dcc93e74874bf6808978caa138675de4791e7962bf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:27:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 13 Oct 2020 23:28:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Mon, 16 Nov 2020 19:25:10 GMT
ENV KAPACITOR_VERSION=1.5.7
# Mon, 16 Nov 2020 19:25:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 16 Nov 2020 19:25:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 16 Nov 2020 19:25:14 GMT
EXPOSE 9092
# Mon, 16 Nov 2020 19:25:14 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 16 Nov 2020 19:25:14 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 16 Nov 2020 19:25:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Nov 2020 19:25:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddcd7b1d32dba2ff27539e272b23ef5c09f4b3777b1fd6cdca8cca7ce6c0254`  
		Last Modified: Tue, 13 Oct 2020 23:28:40 GMT  
		Size: 13.2 MB (13173587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8620385d89b76a759c4d7ced3d2e60ab0f02b6e0014a283611307a6c53b413c7`  
		Last Modified: Tue, 13 Oct 2020 23:28:37 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef715b38d07da58ce4193c1355aed097e099f378fa90e648801c81cd853ffaf0`  
		Last Modified: Mon, 16 Nov 2020 19:25:43 GMT  
		Size: 36.5 MB (36454607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d308844fbb1ca81e41af5932cad72ee0ab598d58e94c841a1490b101a6540f2c`  
		Last Modified: Mon, 16 Nov 2020 19:25:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d0659a36907a18faa571a1ba169a1d4f397a3713b4e6eca5e373b6409f68af`  
		Last Modified: Mon, 16 Nov 2020 19:25:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.7` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:dbb5d180da09ac439451e3369f70c982ec0e10fcd75a7caf3aa8fbdf337fcafa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103073367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dc9158c2d49677fe79ba913d3232b5adcc4ef71510d07943f703226157278a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:47 GMT
ADD file:58b80132bbfb3cae1eb2a9345e362cce1e39de41055fdcef8e5a8a8a447f69b0 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:57:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:57:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:28:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 19:28:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:28:39 GMT
ENV KAPACITOR_VERSION=1.5.7
# Wed, 18 Nov 2020 19:28:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 19:28:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 19:28:48 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 19:28:49 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 19:28:50 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 19:28:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:28:52 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cfc77fa15d772230821249f78cfbb69a8fc6596f6867601b9dad16aedb424325`  
		Last Modified: Tue, 17 Nov 2020 20:35:24 GMT  
		Size: 42.1 MB (42117734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1d24dbd0f85452f20a934ea14ebc3dadfdd8493317dfe8f7f2aa1772937953`  
		Last Modified: Tue, 17 Nov 2020 22:12:47 GMT  
		Size: 9.4 MB (9444101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90255e5a0a934b36df89ac1c1842d07d8d7ed4b3531898af64fdab8372662e3e`  
		Last Modified: Tue, 17 Nov 2020 22:12:46 GMT  
		Size: 3.9 MB (3919908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2039951b2be730d749377ed10abb75898d5083ea38568d8cd4972e7a791e8a34`  
		Last Modified: Wed, 18 Nov 2020 19:29:07 GMT  
		Size: 13.4 MB (13416267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4f166820e128a7f6172218770b80b3de48fe84639f56364ba3200ca580822e`  
		Last Modified: Wed, 18 Nov 2020 19:29:05 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0142c470d43c630e19772a73a56985e7d1b5bc8d58598800e20b062778901ee6`  
		Last Modified: Wed, 18 Nov 2020 19:29:28 GMT  
		Size: 34.2 MB (34172045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21079ad338808a272865afc17d11c43928a709bc37e13236b7fae0eda714711c`  
		Last Modified: Wed, 18 Nov 2020 19:29:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cad50e60a834d8bdd7201d17c37a51f596df750b0b8d94b9e6cb2ccc27fa3`  
		Last Modified: Wed, 18 Nov 2020 19:29:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5b20fed30b4e8c9f89c0dad6d8d172e1d76fad60cf53706bf54fe8b031f81c56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103862482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430779a890d64071bec0487e68fc1ccc6a775930a8edd400d8d3d2c8d58dd693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:28:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 21:15:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:15:19 GMT
ENV KAPACITOR_VERSION=1.5.7
# Wed, 18 Nov 2020 21:15:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 21:15:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 21:15:27 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 21:15:27 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 21:15:28 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 21:15:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:15:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9b3adbe4ac4ca73818d8b79e94d2ff2b6ceafc1225d7c036ec4d384f0804a`  
		Last Modified: Tue, 17 Nov 2020 22:40:38 GMT  
		Size: 9.7 MB (9702292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052ba804da6ef34fd9dddf0ca298b1e0551ac8cf3ea14fc371fa1fa51cbd7f7c`  
		Last Modified: Tue, 17 Nov 2020 22:40:36 GMT  
		Size: 4.1 MB (4095219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d0115aaf8aea01788d62c5180c53c44f5b525f2a9dddfd2859576f55f219b`  
		Last Modified: Wed, 18 Nov 2020 21:15:45 GMT  
		Size: 12.9 MB (12912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f61bf00eecdaa1ba088593162e6892a588b4bdebc909c2cbf006fe9d2b0332a`  
		Last Modified: Wed, 18 Nov 2020 21:15:42 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8814f25006190778f6d5c4c287f922d620ed7720f89d70b0be24eb7f1db4f0`  
		Last Modified: Wed, 18 Nov 2020 21:16:05 GMT  
		Size: 34.0 MB (33972658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b1a95a3f1063ac127f86a44a5a9cd8a68d6de59df05c3d9455088ddbceab29`  
		Last Modified: Wed, 18 Nov 2020 21:15:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57e1ccfd78a9919f64e08d48f8712b319bf7c4e2058563501c2aa3e4bc640fb`  
		Last Modified: Wed, 18 Nov 2020 21:15:58 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.7-alpine`

```console
$ docker pull kapacitor@sha256:62c81e890355680a75d8625e3c576f28a8c0ea65c0c5c6882075ed92782f939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:46edc2279d0db43ad60d0e90505709a2b7bbcafb70ff947a9aa0d4a778edcbdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23178880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3734e75b088f1912286da510906557a9407b318575e2ee8bc7b4752c3eeda058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:55:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 16 Nov 2020 19:25:20 GMT
ENV KAPACITOR_VERSION=1.5.7
# Mon, 16 Nov 2020 19:25:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 16 Nov 2020 19:25:23 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 16 Nov 2020 19:25:24 GMT
EXPOSE 9092
# Mon, 16 Nov 2020 19:25:24 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 16 Nov 2020 19:25:24 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Mon, 16 Nov 2020 19:25:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Nov 2020 19:25:24 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea603847a3b82b32a20eba9b8d97e8d5da78d7491d9412b148947a123d8c4ffd`  
		Last Modified: Thu, 22 Oct 2020 02:56:04 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a223a353c442a39f3d33072e3083a566649afc7172097634f2b9a318605c8b68`  
		Last Modified: Mon, 16 Nov 2020 19:25:54 GMT  
		Size: 20.1 MB (20100603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbebfafb26eb6ba627a30a9616b7d1a6412546b4f216e401a638d15cf0c155d`  
		Last Modified: Mon, 16 Nov 2020 19:25:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742d9a2c4f0636602533e1feb0dfd8bbf1140a0d6f62bcb1b92c2b50fcd5969b`  
		Last Modified: Mon, 16 Nov 2020 19:25:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:62c81e890355680a75d8625e3c576f28a8c0ea65c0c5c6882075ed92782f939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:46edc2279d0db43ad60d0e90505709a2b7bbcafb70ff947a9aa0d4a778edcbdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23178880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3734e75b088f1912286da510906557a9407b318575e2ee8bc7b4752c3eeda058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:55:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 16 Nov 2020 19:25:20 GMT
ENV KAPACITOR_VERSION=1.5.7
# Mon, 16 Nov 2020 19:25:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 16 Nov 2020 19:25:23 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 16 Nov 2020 19:25:24 GMT
EXPOSE 9092
# Mon, 16 Nov 2020 19:25:24 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 16 Nov 2020 19:25:24 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Mon, 16 Nov 2020 19:25:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Nov 2020 19:25:24 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea603847a3b82b32a20eba9b8d97e8d5da78d7491d9412b148947a123d8c4ffd`  
		Last Modified: Thu, 22 Oct 2020 02:56:04 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a223a353c442a39f3d33072e3083a566649afc7172097634f2b9a318605c8b68`  
		Last Modified: Mon, 16 Nov 2020 19:25:54 GMT  
		Size: 20.1 MB (20100603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbebfafb26eb6ba627a30a9616b7d1a6412546b4f216e401a638d15cf0c155d`  
		Last Modified: Mon, 16 Nov 2020 19:25:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742d9a2c4f0636602533e1feb0dfd8bbf1140a0d6f62bcb1b92c2b50fcd5969b`  
		Last Modified: Mon, 16 Nov 2020 19:25:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:62c81e890355680a75d8625e3c576f28a8c0ea65c0c5c6882075ed92782f939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:46edc2279d0db43ad60d0e90505709a2b7bbcafb70ff947a9aa0d4a778edcbdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23178880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3734e75b088f1912286da510906557a9407b318575e2ee8bc7b4752c3eeda058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:54:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:55:00 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 16 Nov 2020 19:25:20 GMT
ENV KAPACITOR_VERSION=1.5.7
# Mon, 16 Nov 2020 19:25:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 16 Nov 2020 19:25:23 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 16 Nov 2020 19:25:24 GMT
EXPOSE 9092
# Mon, 16 Nov 2020 19:25:24 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 16 Nov 2020 19:25:24 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Mon, 16 Nov 2020 19:25:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Nov 2020 19:25:24 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab57a7256718fa42bedfa2c660a5f0de9129121c4f27e021d960eea00eb85650`  
		Last Modified: Thu, 22 Oct 2020 02:56:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea603847a3b82b32a20eba9b8d97e8d5da78d7491d9412b148947a123d8c4ffd`  
		Last Modified: Thu, 22 Oct 2020 02:56:04 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a223a353c442a39f3d33072e3083a566649afc7172097634f2b9a318605c8b68`  
		Last Modified: Mon, 16 Nov 2020 19:25:54 GMT  
		Size: 20.1 MB (20100603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbebfafb26eb6ba627a30a9616b7d1a6412546b4f216e401a638d15cf0c155d`  
		Last Modified: Mon, 16 Nov 2020 19:25:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742d9a2c4f0636602533e1feb0dfd8bbf1140a0d6f62bcb1b92c2b50fcd5969b`  
		Last Modified: Mon, 16 Nov 2020 19:25:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:47232cec363506128b66e4d17410505ba9398a6cef5dbeca04f3e7b5e82031c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:9e0e736b570a93a7323df6f7e77e31714a1c747423b69a2677b030206e1f2e47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110089906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8633002ed21494f7233dcc93e74874bf6808978caa138675de4791e7962bf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 23:27:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 13 Oct 2020 23:28:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Mon, 16 Nov 2020 19:25:10 GMT
ENV KAPACITOR_VERSION=1.5.7
# Mon, 16 Nov 2020 19:25:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Mon, 16 Nov 2020 19:25:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Mon, 16 Nov 2020 19:25:14 GMT
EXPOSE 9092
# Mon, 16 Nov 2020 19:25:14 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 16 Nov 2020 19:25:14 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Mon, 16 Nov 2020 19:25:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Nov 2020 19:25:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8559aa5ebb59d52475c0142459015fb9be267e1a497d8664f3fc8a35445173`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 10.8 MB (10751068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32bfbbc3bad880f731e2f37903c9e359e180a5e74a703293a9441260cf3551`  
		Last Modified: Tue, 13 Oct 2020 02:31:24 GMT  
		Size: 4.3 MB (4340586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddcd7b1d32dba2ff27539e272b23ef5c09f4b3777b1fd6cdca8cca7ce6c0254`  
		Last Modified: Tue, 13 Oct 2020 23:28:40 GMT  
		Size: 13.2 MB (13173587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8620385d89b76a759c4d7ced3d2e60ab0f02b6e0014a283611307a6c53b413c7`  
		Last Modified: Tue, 13 Oct 2020 23:28:37 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef715b38d07da58ce4193c1355aed097e099f378fa90e648801c81cd853ffaf0`  
		Last Modified: Mon, 16 Nov 2020 19:25:43 GMT  
		Size: 36.5 MB (36454607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d308844fbb1ca81e41af5932cad72ee0ab598d58e94c841a1490b101a6540f2c`  
		Last Modified: Mon, 16 Nov 2020 19:25:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d0659a36907a18faa571a1ba169a1d4f397a3713b4e6eca5e373b6409f68af`  
		Last Modified: Mon, 16 Nov 2020 19:25:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:dbb5d180da09ac439451e3369f70c982ec0e10fcd75a7caf3aa8fbdf337fcafa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103073367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dc9158c2d49677fe79ba913d3232b5adcc4ef71510d07943f703226157278a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:47 GMT
ADD file:58b80132bbfb3cae1eb2a9345e362cce1e39de41055fdcef8e5a8a8a447f69b0 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:57:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:57:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 19:28:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 19:28:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 19:28:39 GMT
ENV KAPACITOR_VERSION=1.5.7
# Wed, 18 Nov 2020 19:28:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 19:28:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 19:28:48 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 19:28:49 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 19:28:50 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 19:28:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 19:28:52 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cfc77fa15d772230821249f78cfbb69a8fc6596f6867601b9dad16aedb424325`  
		Last Modified: Tue, 17 Nov 2020 20:35:24 GMT  
		Size: 42.1 MB (42117734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1d24dbd0f85452f20a934ea14ebc3dadfdd8493317dfe8f7f2aa1772937953`  
		Last Modified: Tue, 17 Nov 2020 22:12:47 GMT  
		Size: 9.4 MB (9444101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90255e5a0a934b36df89ac1c1842d07d8d7ed4b3531898af64fdab8372662e3e`  
		Last Modified: Tue, 17 Nov 2020 22:12:46 GMT  
		Size: 3.9 MB (3919908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2039951b2be730d749377ed10abb75898d5083ea38568d8cd4972e7a791e8a34`  
		Last Modified: Wed, 18 Nov 2020 19:29:07 GMT  
		Size: 13.4 MB (13416267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4f166820e128a7f6172218770b80b3de48fe84639f56364ba3200ca580822e`  
		Last Modified: Wed, 18 Nov 2020 19:29:05 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0142c470d43c630e19772a73a56985e7d1b5bc8d58598800e20b062778901ee6`  
		Last Modified: Wed, 18 Nov 2020 19:29:28 GMT  
		Size: 34.2 MB (34172045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21079ad338808a272865afc17d11c43928a709bc37e13236b7fae0eda714711c`  
		Last Modified: Wed, 18 Nov 2020 19:29:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cad50e60a834d8bdd7201d17c37a51f596df750b0b8d94b9e6cb2ccc27fa3`  
		Last Modified: Wed, 18 Nov 2020 19:29:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5b20fed30b4e8c9f89c0dad6d8d172e1d76fad60cf53706bf54fe8b031f81c56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103862482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430779a890d64071bec0487e68fc1ccc6a775930a8edd400d8d3d2c8d58dd693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:28:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 21:14:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Nov 2020 21:15:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 18 Nov 2020 21:15:19 GMT
ENV KAPACITOR_VERSION=1.5.7
# Wed, 18 Nov 2020 21:15:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Nov 2020 21:15:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Nov 2020 21:15:27 GMT
EXPOSE 9092
# Wed, 18 Nov 2020 21:15:27 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Nov 2020 21:15:28 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Nov 2020 21:15:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Nov 2020 21:15:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9b3adbe4ac4ca73818d8b79e94d2ff2b6ceafc1225d7c036ec4d384f0804a`  
		Last Modified: Tue, 17 Nov 2020 22:40:38 GMT  
		Size: 9.7 MB (9702292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052ba804da6ef34fd9dddf0ca298b1e0551ac8cf3ea14fc371fa1fa51cbd7f7c`  
		Last Modified: Tue, 17 Nov 2020 22:40:36 GMT  
		Size: 4.1 MB (4095219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d0115aaf8aea01788d62c5180c53c44f5b525f2a9dddfd2859576f55f219b`  
		Last Modified: Wed, 18 Nov 2020 21:15:45 GMT  
		Size: 12.9 MB (12912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f61bf00eecdaa1ba088593162e6892a588b4bdebc909c2cbf006fe9d2b0332a`  
		Last Modified: Wed, 18 Nov 2020 21:15:42 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8814f25006190778f6d5c4c287f922d620ed7720f89d70b0be24eb7f1db4f0`  
		Last Modified: Wed, 18 Nov 2020 21:16:05 GMT  
		Size: 34.0 MB (33972658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b1a95a3f1063ac127f86a44a5a9cd8a68d6de59df05c3d9455088ddbceab29`  
		Last Modified: Wed, 18 Nov 2020 21:15:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57e1ccfd78a9919f64e08d48f8712b319bf7c4e2058563501c2aa3e4bc640fb`  
		Last Modified: Wed, 18 Nov 2020 21:15:58 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
