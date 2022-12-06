## `chronograf:latest`

```console
$ docker pull chronograf@sha256:a9d048c0161612c8e99a6a0022bb3d897cf6f2d0bd22b865f01d8f7b3292002d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:29ab1b9d91d0c5493c5a5da0a6d8d81098d48a4217cdfe1452dcefa8b5e4a720
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81254093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc3e83e2be670ef62324a08070a2c4836172d7f37b0b841a50fcc5705ea594c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:46:27 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 01:46:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:46:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:46:35 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:46:35 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:46:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:46:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:46:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ff5a347561490589cdaddbb9c1d1fd79814edac3ddf8bc928b34dddfd7c5bb`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 5.2 MB (5228712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86e4af0a7ab80153783e9829b83a062eb28cb99ba473fdb07e876952c8354b1`  
		Last Modified: Tue, 06 Dec 2022 01:47:47 GMT  
		Size: 44.6 MB (44588133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2df382812100ec1f9eee6ae9216b67d9d9ae41984fab817ddf26ef056701d`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb68818fcfd812eb6559bb580d3b5be78474c1a0bda9b702987437c87c66309`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1a18d308edf2a5a71cfaffc3459b9585962a4b199e557cc2c662df81a27165`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:73faecaca432c3dba55288fb2f4bce07cdf8d16188a7fe8f07e6b06f4f639763
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73560455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21db32e9f8ab2a11ad052adbaeb03e3f031aa69ef241e4f6958c3b08cb41c80c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:12:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 15 Nov 2022 12:13:04 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 15 Nov 2022 12:13:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 15 Nov 2022 12:13:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 15 Nov 2022 12:13:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 15 Nov 2022 12:13:14 GMT
EXPOSE 8888
# Tue, 15 Nov 2022 12:13:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 15 Nov 2022 12:13:15 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 15 Nov 2022 12:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Nov 2022 12:13:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118439706100e2536364e0a7909c17a0e97502d09e6cef1f5fcf85371e6d767c`  
		Last Modified: Tue, 15 Nov 2022 12:14:07 GMT  
		Size: 4.5 MB (4494978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d881550c0f258caec8cb2e72bccef84e085b776435200a059d49847dff4783`  
		Last Modified: Tue, 15 Nov 2022 12:14:44 GMT  
		Size: 42.5 MB (42464891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cac2e60b326d356648abb3d6bfe415011f8bd66147b2d3ec1b3236f3055684f`  
		Last Modified: Tue, 15 Nov 2022 12:14:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344219e1493f8d5d359b71e27b1ea1de083ab0ea6b505d3a8c03669762cc671a`  
		Last Modified: Tue, 15 Nov 2022 12:14:36 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbb6a1869ce0007c21319ca79ce86193e1235cd80341ab1a4f207269de6ed61`  
		Last Modified: Tue, 15 Nov 2022 12:14:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b9a923a7f9577ea18562ca96d20f9092d3564d8b7fdbab907678a2125762c73d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77914187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b562de4f793f8bfe522fb78778dadf5df254c69bff24023d08eda93fbfe602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:36 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 02:15:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:42 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcfd47e4f0331c64dfb2af5573bf99a4b88b4d972387850c61ff6ef0d11a9`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 5.2 MB (5211566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63cfceb30c24c808b43865619c58241102c036bd153c354e2f2f1457954400`  
		Last Modified: Tue, 06 Dec 2022 02:16:37 GMT  
		Size: 42.6 MB (42617907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb34459112efb5b29d1c5cbe97dad350e283c8259b45e077aa3104ff0a7c432b`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21072e41358457fcdb1399f31b7dd73322af50a96fc66fe37b8841d39bb92579`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca77523a925a0d9872b733837dba904a8a82c95de486d5f95f5bf8678deb165`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
