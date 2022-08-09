<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.2`](#eggdrop192)
-	[`eggdrop:1.9.3rc1`](#eggdrop193rc1)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:76989e1e251b26b0882e49c32311dfccf3566389cf8702c1d8469760539c2d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:7c1f07fb2993db2d23c2e3a8e823129712498b74c5e45e56f55b7404c92e592f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce82528bfca421aca6084f8346db146a3916779e591d66c47ae07885ca8e46d6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:33:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:33:58 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:33:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:34:00 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:34:52 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:34:53 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:34:53 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:34:53 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:34:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:34:53 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:34:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:34:54 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:34:54 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:34:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c64dbfdb30e6f2bd91f9d7ba689f3dd89f62125a424c3c17fcee5620b2020a3`  
		Last Modified: Tue, 09 Aug 2022 18:36:41 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d40371db7868456b4ab64cfe248665bd0667efb13b1d7f88c53d2c2b119809`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6657ec397289e21433c76381c67362a8917b0a8a27d3fed327a468a29c51d1c`  
		Last Modified: Tue, 09 Aug 2022 18:36:39 GMT  
		Size: 2.7 MB (2726758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a22238d642dd432a127e2b9748eca1a5c7257af11d7e79d3ab7fcff4d7ae94d`  
		Last Modified: Tue, 09 Aug 2022 18:36:40 GMT  
		Size: 2.7 MB (2731661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23a4112d585d674763eebdc058f2e3c60c68d8ae5d07c49b0b2c83965298a4`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38d0f5cf90ae3f376a3e1abb98ea29aed2da199c6fd97b39df16deb70fc968`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:e37161cd4b8b5bed14a49cfdad3e2a9c48b7313e94c982463c045ad10aca8c31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc95519b4a1c840f914d74fc894264484613be3a619f55381b34c446cafd39c0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:40 GMT
ADD file:541b767b21b9e0c4dab118d5e000990da3dbb81b547c1ee9941e2cf7edc5edd6 in / 
# Tue, 09 Aug 2022 17:49:40 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:51:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:51:03 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:51:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:51:06 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:52:08 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:52:08 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:52:09 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:52:09 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:52:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:52:09 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:52:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:52:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b423ab447fbb66b194458908339addbb5dd52e4aa7d04a42b387cdc07bbd92a1`  
		Last Modified: Tue, 09 Aug 2022 17:51:16 GMT  
		Size: 2.6 MB (2633535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ab43c4ab8ce3acf894fb689d3fab3e352715d608c94c7ee0ee865b529cec6d`  
		Last Modified: Tue, 09 Aug 2022 18:54:29 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511cfb58f000c475f12763f9367d55beb8423621bb6a35bf8a7f715cd1fb1a30`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 10.4 KB (10408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfec0ee07b8315970755477fe547e30ce338e99e7c00565c182a9ca59b5c8a8`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2653209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfdb869195492c054c5600ff7528f0f9520281927b6ca195486d47254674c16`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2686830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2676ad94b7d2ef8b194fb1d5a76635d4965833ee34cd876da2d48abdd5bcaa`  
		Last Modified: Tue, 09 Aug 2022 18:54:26 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f913ef8822c4a99179c9d88e1dfe63f9c4eeac5c6295fbaff2d605b4524077c0`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:8742e15342a7bbb16cc67080eccdad43c562b9247eed84b3f3d15597539aaf64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8207176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b4ec7917ffc45ea7312ef4cf881e890014f297d9e004c853ba3dede9415098`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:31:50 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:31:51 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:31:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:31:54 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 19 Jul 2022 23:32:58 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:32:59 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:33:00 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:33:01 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:33:02 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:33:03 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:33:04 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:33:05 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:33:06 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:33:08 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:33:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:33:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:33:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dbac81bec09c0716eeeccdb6afbe623c4b8ad08f044642623c18f6af531b54`  
		Last Modified: Tue, 19 Jul 2022 23:33:49 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facbeba827e8fea73efa4f1f728fc01d423230fae7e1342b0f9a67574897107f`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 10.5 KB (10477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b1b679b927f7031cc1fe1185ced237ba184e9a5e7dbf5ba545723f62724180`  
		Last Modified: Tue, 19 Jul 2022 23:33:48 GMT  
		Size: 2.8 MB (2752055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3002264c65c5b51440a2a94ca4a4c51c9528612157a97ff0cdf707e1336bd59`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 2.7 MB (2719681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6f183367dbe30deb5c145276f489d7096d50a04afa5b1965dae7070e047c01`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d6ce2389c0c1a1906fc6ce831a96187e0f16e312754a5450604ce448173579`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.2`

```console
$ docker pull eggdrop@sha256:76989e1e251b26b0882e49c32311dfccf3566389cf8702c1d8469760539c2d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.2` - linux; amd64

```console
$ docker pull eggdrop@sha256:7c1f07fb2993db2d23c2e3a8e823129712498b74c5e45e56f55b7404c92e592f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce82528bfca421aca6084f8346db146a3916779e591d66c47ae07885ca8e46d6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:33:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:33:58 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:33:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:34:00 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:34:52 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:34:53 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:34:53 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:34:53 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:34:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:34:53 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:34:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:34:54 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:34:54 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:34:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c64dbfdb30e6f2bd91f9d7ba689f3dd89f62125a424c3c17fcee5620b2020a3`  
		Last Modified: Tue, 09 Aug 2022 18:36:41 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d40371db7868456b4ab64cfe248665bd0667efb13b1d7f88c53d2c2b119809`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6657ec397289e21433c76381c67362a8917b0a8a27d3fed327a468a29c51d1c`  
		Last Modified: Tue, 09 Aug 2022 18:36:39 GMT  
		Size: 2.7 MB (2726758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a22238d642dd432a127e2b9748eca1a5c7257af11d7e79d3ab7fcff4d7ae94d`  
		Last Modified: Tue, 09 Aug 2022 18:36:40 GMT  
		Size: 2.7 MB (2731661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23a4112d585d674763eebdc058f2e3c60c68d8ae5d07c49b0b2c83965298a4`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38d0f5cf90ae3f376a3e1abb98ea29aed2da199c6fd97b39df16deb70fc968`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.2` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:e37161cd4b8b5bed14a49cfdad3e2a9c48b7313e94c982463c045ad10aca8c31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc95519b4a1c840f914d74fc894264484613be3a619f55381b34c446cafd39c0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:40 GMT
ADD file:541b767b21b9e0c4dab118d5e000990da3dbb81b547c1ee9941e2cf7edc5edd6 in / 
# Tue, 09 Aug 2022 17:49:40 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:51:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:51:03 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:51:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:51:06 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:52:08 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:52:08 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:52:09 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:52:09 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:52:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:52:09 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:52:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:52:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b423ab447fbb66b194458908339addbb5dd52e4aa7d04a42b387cdc07bbd92a1`  
		Last Modified: Tue, 09 Aug 2022 17:51:16 GMT  
		Size: 2.6 MB (2633535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ab43c4ab8ce3acf894fb689d3fab3e352715d608c94c7ee0ee865b529cec6d`  
		Last Modified: Tue, 09 Aug 2022 18:54:29 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511cfb58f000c475f12763f9367d55beb8423621bb6a35bf8a7f715cd1fb1a30`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 10.4 KB (10408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfec0ee07b8315970755477fe547e30ce338e99e7c00565c182a9ca59b5c8a8`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2653209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfdb869195492c054c5600ff7528f0f9520281927b6ca195486d47254674c16`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2686830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2676ad94b7d2ef8b194fb1d5a76635d4965833ee34cd876da2d48abdd5bcaa`  
		Last Modified: Tue, 09 Aug 2022 18:54:26 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f913ef8822c4a99179c9d88e1dfe63f9c4eeac5c6295fbaff2d605b4524077c0`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.2` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:8742e15342a7bbb16cc67080eccdad43c562b9247eed84b3f3d15597539aaf64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8207176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b4ec7917ffc45ea7312ef4cf881e890014f297d9e004c853ba3dede9415098`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:31:50 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:31:51 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:31:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:31:54 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 19 Jul 2022 23:32:58 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:32:59 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:33:00 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:33:01 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:33:02 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:33:03 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:33:04 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:33:05 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:33:06 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:33:08 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:33:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:33:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:33:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dbac81bec09c0716eeeccdb6afbe623c4b8ad08f044642623c18f6af531b54`  
		Last Modified: Tue, 19 Jul 2022 23:33:49 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facbeba827e8fea73efa4f1f728fc01d423230fae7e1342b0f9a67574897107f`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 10.5 KB (10477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b1b679b927f7031cc1fe1185ced237ba184e9a5e7dbf5ba545723f62724180`  
		Last Modified: Tue, 19 Jul 2022 23:33:48 GMT  
		Size: 2.8 MB (2752055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3002264c65c5b51440a2a94ca4a4c51c9528612157a97ff0cdf707e1336bd59`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 2.7 MB (2719681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6f183367dbe30deb5c145276f489d7096d50a04afa5b1965dae7070e047c01`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d6ce2389c0c1a1906fc6ce831a96187e0f16e312754a5450604ce448173579`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.3rc1`

```console
$ docker pull eggdrop@sha256:9d30dd45c7ac02716b9137caddb304c645d75bd53f1884d1744aa9d457a361f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.3rc1` - linux; amd64

```console
$ docker pull eggdrop@sha256:84103aa45a8a586765646627c7d5cf473cf5cd77c53a188613d22a8ccf492038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8185513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c67fa84ee6fc79c9607178ba44a9549147ff921179c303e98d3f0bfa46e555`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:35:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:35:07 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:35:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:35:09 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:36:04 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3rc1.tar.gz.asc eggdrop-1.9.3rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3rc1.tar.gz.asc   && tar -zxvf eggdrop-1.9.3rc1.tar.gz   && rm eggdrop-1.9.3rc1.tar.gz   && ( cd eggdrop-1.9.3rc1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:36:04 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:36:04 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:36:04 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:36:05 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:36:05 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:36:05 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:36:05 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:36:05 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:36:05 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:36:05 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:36:05 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:36:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d156f1e73a5c09ea7d595552f2886c32e46f8b9da1f7aa8637bedabca35b3c`  
		Last Modified: Tue, 09 Aug 2022 18:36:58 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57ccd21dcf7fc4a0b414bb17cdea42bfce6902ff9a7a98d94e67738bec46e0`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf7f0646fedf1539fbc291c21fd990c5d286f406bd9340846de181384ab68a2`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 2.8 MB (2757888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8805a4ea2959974f1f37beae2f3abd718b9e00eab651d86b43889e5da4bdbd`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 2.6 MB (2606846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f563a36c4d067614739e94002eba0669f19b3520d914fac4b295d90a5c68e0`  
		Last Modified: Tue, 09 Aug 2022 18:36:55 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbb3c172b037a12e1516ba2e55d60a8954bf959de62dffdcd9ed9e314a8d1ff`  
		Last Modified: Tue, 09 Aug 2022 18:36:55 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.3rc1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:9635d09f07af95089bef1d110306b0d4525e3c935650ad127b769fb73343a05c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73800cd63956b665cd8aa70f0bf59611a22bf760be5cf522c70b6dbd01f4606`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:52:27 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:52:28 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:52:29 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:52:31 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:53:37 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3rc1.tar.gz.asc eggdrop-1.9.3rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3rc1.tar.gz.asc   && tar -zxvf eggdrop-1.9.3rc1.tar.gz   && rm eggdrop-1.9.3rc1.tar.gz   && ( cd eggdrop-1.9.3rc1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:53:37 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:53:38 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:53:38 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:53:38 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:53:38 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:53:38 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:53:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:53:39 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:53:39 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:53:39 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:53:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:53:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb866cf343f7b9b34dad5c926781cac38ea063839bb5b21e95034c4cdd4819c`  
		Last Modified: Tue, 09 Aug 2022 18:54:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be0cf078e0482d862fe98d285ba22f2f015c9042e4a8856570b4b1724798e8f`  
		Last Modified: Tue, 09 Aug 2022 18:54:49 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a85ef0c41d89851cd45b7c3f87491bf9c706f4f3160cee727ce12108c2a9f7`  
		Last Modified: Tue, 09 Aug 2022 18:54:49 GMT  
		Size: 2.7 MB (2679961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a351e4963a67d1eb11df1f49489725ec1d385504a16c691ec79a8e48e9b88b`  
		Last Modified: Tue, 09 Aug 2022 18:54:49 GMT  
		Size: 2.6 MB (2616177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe0bd47772e3cd510c7bd1f85ae187a4599903b01ab33667c7e6c4ae64b836`  
		Last Modified: Tue, 09 Aug 2022 18:54:48 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e38b65c09fb7298ad0b17b670d53be4368153bff0d99968a76c276568e37f3`  
		Last Modified: Tue, 09 Aug 2022 18:54:48 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.3rc1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:3a09be9a01283eabfec3a3ee6129f811aa47c01a73db654e31adc42cf4833b92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8113860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba42398ee12dfd494080142bd60add255772352b050ebd08b0ff8cce33faa9c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:21:35 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 18 Jul 2022 22:21:36 GMT
RUN adduser -S eggdrop
# Mon, 18 Jul 2022 22:21:38 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 22:21:39 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 18 Jul 2022 22:22:48 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3rc1.tar.gz.asc eggdrop-1.9.3rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3rc1.tar.gz.asc   && tar -zxvf eggdrop-1.9.3rc1.tar.gz   && rm eggdrop-1.9.3rc1.tar.gz   && ( cd eggdrop-1.9.3rc1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 22:22:48 GMT
ENV NICK=
# Mon, 18 Jul 2022 22:22:49 GMT
ENV SERVER=
# Mon, 18 Jul 2022 22:22:50 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 22:22:51 GMT
ENV OWNER=
# Mon, 18 Jul 2022 22:22:52 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 22:22:53 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 22:22:54 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 22:22:55 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 22:22:57 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 22:22:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 22:22:58 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 22:22:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3e23b41ab3fc3dca1cb2d468079d1db5b1f5cada8c2f8b3ca59819d5e9612`  
		Last Modified: Mon, 18 Jul 2022 22:23:36 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76b6939ad9887d656502dea966a0ed11974715248f71ca1be000c371ea071f6`  
		Last Modified: Mon, 18 Jul 2022 22:23:34 GMT  
		Size: 10.6 KB (10620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920dc62957d07396c43588001c1961c926312dacae64eeab8f460e12d18355e`  
		Last Modified: Mon, 18 Jul 2022 22:23:35 GMT  
		Size: 2.8 MB (2775880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65739305b2979792ce3e6a9463243866f2ef253e2827b670f428687c41dce69d`  
		Last Modified: Mon, 18 Jul 2022 22:23:34 GMT  
		Size: 2.6 MB (2628849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfd5bdea2aff49d85de6ec2f14c9b42ba50b070fbdd02ae2d792aabde064dd3`  
		Last Modified: Mon, 18 Jul 2022 22:23:34 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30136caea046c19e04d5fd29bc99c02e23cdcdc79c0f3376e5d34753c2252b`  
		Last Modified: Mon, 18 Jul 2022 22:23:34 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:0e2b70a7b8a83bbadecb59cb2a1c8e942944148320dbba020f0a834fec1a303a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:c782c9d94bb89c734c3277fb534f9e1aada70acfd368de7b8ad2ac3ccab46d5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39697640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc2a3ddd459b82cc505383ba6f2229104d60e5b5807640dc36903f373930dbb`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:29:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:29:50 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:29:51 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:29:51 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 09 Aug 2022 18:29:51 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 09 Aug 2022 18:29:52 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 09 Aug 2022 18:33:47 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:33:48 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:33:48 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:33:48 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:33:48 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:33:48 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:33:48 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:33:49 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:33:49 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:33:49 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:33:49 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:33:49 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:33:49 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c168c83c5b7cbf66a9e59b6eeb2681bba349bbfcfb2210a9e498fbd081911b8`  
		Last Modified: Tue, 09 Aug 2022 18:36:28 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ada8ef30839b781a7752202bb0508c0b31289da9d6c8e2c579b714517f21ca`  
		Last Modified: Tue, 09 Aug 2022 18:36:26 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5a6827106d9ac255c1074ade8a834fad1c2c24c59abbaa036c30ea7e50bc68`  
		Last Modified: Tue, 09 Aug 2022 18:36:26 GMT  
		Size: 1.1 MB (1089939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd6758e0fde641f96ae3752b918e7005398fc332b5ba08b3fa03ab91e77df9a`  
		Last Modified: Tue, 09 Aug 2022 18:36:31 GMT  
		Size: 35.8 MB (35769404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34e9bb594cf5cb810d65d664e8bd68f3a0c975d4d4b00154b7d9f40f8439680`  
		Last Modified: Tue, 09 Aug 2022 18:36:26 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3664d2d4b6b34c02f920ac62c60d8a02b7f86ad43518170e9f6669027382bb85`  
		Last Modified: Tue, 09 Aug 2022 18:36:25 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5708b3cdfd986537b8e3ea8d34cda88cd993f5bfb5cc6785c14136c4698e3e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39089261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ee4e6c23206e9a11d221ab76fb1562f8ca76c71216c6363694cbc051e50f89`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:46:24 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:46:24 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:46:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:46:26 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 09 Aug 2022 18:46:26 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 09 Aug 2022 18:46:27 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 09 Aug 2022 18:50:43 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:50:44 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:50:44 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:50:44 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:50:44 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:50:44 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:50:45 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:50:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:50:45 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:50:45 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:50:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:50:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:50:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b0548d2e71c5e0d69a7d82b4707fa752adad30ef06fb8d34592c20144b1904`  
		Last Modified: Tue, 09 Aug 2022 18:54:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efa052f331402356a00e0435bf34e783a18b22cb899d2daf4ec7ed61bea0727`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e349162c85bd03d527832a51a9da69584af33d92d8edf9a2207c4ddbc958d10`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 1.0 MB (1032556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c61638079e5b7979624aeb3f087b465bbffad1dfb59d11b92390d10a9dc478`  
		Last Modified: Tue, 09 Aug 2022 18:54:18 GMT  
		Size: 35.4 MB (35411073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2eb13384450fae5712b634f4008cea093f07ea7f518bac5a47507283fe8a9e8`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf747ffa38af6270fefdb2f9235b0c6e9e21c8f7f51ad1c2c9047c14c55acb8a`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:21d798f07747179773d3cc07f708ec442fe94b266cb0c940ceffc5c5de7cf8b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39756377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976062a942c1aba30c130d5dac5cc76b1b9cf30429ffa49c00d1ea830425164f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:26:37 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:26:38 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:26:39 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:26:40 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 19 Jul 2022 23:26:41 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 19 Jul 2022 23:26:42 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 19 Jul 2022 23:31:22 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:31:23 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:31:24 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:31:25 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:31:26 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:31:27 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:31:28 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:31:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:31:30 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:31:32 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:31:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:31:33 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:31:34 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f733119a90d66cc38b960cfd3a82f5ac1bf15b88c4210aa7d8daffbae880b8b`  
		Last Modified: Tue, 19 Jul 2022 23:33:36 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046d236c13e8c2c0071dd8655962c99baffb43bb2f6376c65f56bba0b40963af`  
		Last Modified: Tue, 19 Jul 2022 23:33:34 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468fce109fc975be6dbeac73ae066d0fad7aa1479d47d37e32d44ca79bd0567b`  
		Last Modified: Tue, 19 Jul 2022 23:33:34 GMT  
		Size: 1.1 MB (1087539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559fad7e7f02484465220157b063a741a67862e772ec7f0902431614e778e654`  
		Last Modified: Tue, 19 Jul 2022 23:33:39 GMT  
		Size: 35.9 MB (35937439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafc071d54893d348ab170bc20d3b4043025b9b5ba9f4ec960a6626f911e8864`  
		Last Modified: Tue, 19 Jul 2022 23:33:34 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65748c0b1d2f7521c9d2e446166aab0f2295eff54e6f05dad946b848e7e1d71`  
		Last Modified: Tue, 19 Jul 2022 23:33:34 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:76989e1e251b26b0882e49c32311dfccf3566389cf8702c1d8469760539c2d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:7c1f07fb2993db2d23c2e3a8e823129712498b74c5e45e56f55b7404c92e592f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce82528bfca421aca6084f8346db146a3916779e591d66c47ae07885ca8e46d6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:33:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:33:58 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:33:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:34:00 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:34:52 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:34:53 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:34:53 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:34:53 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:34:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:34:53 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:34:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:34:54 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:34:54 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:34:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c64dbfdb30e6f2bd91f9d7ba689f3dd89f62125a424c3c17fcee5620b2020a3`  
		Last Modified: Tue, 09 Aug 2022 18:36:41 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d40371db7868456b4ab64cfe248665bd0667efb13b1d7f88c53d2c2b119809`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6657ec397289e21433c76381c67362a8917b0a8a27d3fed327a468a29c51d1c`  
		Last Modified: Tue, 09 Aug 2022 18:36:39 GMT  
		Size: 2.7 MB (2726758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a22238d642dd432a127e2b9748eca1a5c7257af11d7e79d3ab7fcff4d7ae94d`  
		Last Modified: Tue, 09 Aug 2022 18:36:40 GMT  
		Size: 2.7 MB (2731661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23a4112d585d674763eebdc058f2e3c60c68d8ae5d07c49b0b2c83965298a4`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38d0f5cf90ae3f376a3e1abb98ea29aed2da199c6fd97b39df16deb70fc968`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:e37161cd4b8b5bed14a49cfdad3e2a9c48b7313e94c982463c045ad10aca8c31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc95519b4a1c840f914d74fc894264484613be3a619f55381b34c446cafd39c0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:40 GMT
ADD file:541b767b21b9e0c4dab118d5e000990da3dbb81b547c1ee9941e2cf7edc5edd6 in / 
# Tue, 09 Aug 2022 17:49:40 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:51:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:51:03 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:51:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:51:06 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:52:08 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:52:08 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:52:09 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:52:09 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:52:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:52:09 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:52:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:52:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b423ab447fbb66b194458908339addbb5dd52e4aa7d04a42b387cdc07bbd92a1`  
		Last Modified: Tue, 09 Aug 2022 17:51:16 GMT  
		Size: 2.6 MB (2633535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ab43c4ab8ce3acf894fb689d3fab3e352715d608c94c7ee0ee865b529cec6d`  
		Last Modified: Tue, 09 Aug 2022 18:54:29 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511cfb58f000c475f12763f9367d55beb8423621bb6a35bf8a7f715cd1fb1a30`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 10.4 KB (10408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfec0ee07b8315970755477fe547e30ce338e99e7c00565c182a9ca59b5c8a8`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2653209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfdb869195492c054c5600ff7528f0f9520281927b6ca195486d47254674c16`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2686830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2676ad94b7d2ef8b194fb1d5a76635d4965833ee34cd876da2d48abdd5bcaa`  
		Last Modified: Tue, 09 Aug 2022 18:54:26 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f913ef8822c4a99179c9d88e1dfe63f9c4eeac5c6295fbaff2d605b4524077c0`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:8742e15342a7bbb16cc67080eccdad43c562b9247eed84b3f3d15597539aaf64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8207176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b4ec7917ffc45ea7312ef4cf881e890014f297d9e004c853ba3dede9415098`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:31:50 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:31:51 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:31:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:31:54 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 19 Jul 2022 23:32:58 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:32:59 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:33:00 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:33:01 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:33:02 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:33:03 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:33:04 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:33:05 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:33:06 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:33:08 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:33:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:33:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:33:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dbac81bec09c0716eeeccdb6afbe623c4b8ad08f044642623c18f6af531b54`  
		Last Modified: Tue, 19 Jul 2022 23:33:49 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facbeba827e8fea73efa4f1f728fc01d423230fae7e1342b0f9a67574897107f`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 10.5 KB (10477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b1b679b927f7031cc1fe1185ced237ba184e9a5e7dbf5ba545723f62724180`  
		Last Modified: Tue, 19 Jul 2022 23:33:48 GMT  
		Size: 2.8 MB (2752055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3002264c65c5b51440a2a94ca4a4c51c9528612157a97ff0cdf707e1336bd59`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 2.7 MB (2719681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6f183367dbe30deb5c145276f489d7096d50a04afa5b1965dae7070e047c01`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d6ce2389c0c1a1906fc6ce831a96187e0f16e312754a5450604ce448173579`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:76989e1e251b26b0882e49c32311dfccf3566389cf8702c1d8469760539c2d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:7c1f07fb2993db2d23c2e3a8e823129712498b74c5e45e56f55b7404c92e592f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce82528bfca421aca6084f8346db146a3916779e591d66c47ae07885ca8e46d6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:33:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:33:58 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:33:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:34:00 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:34:52 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:34:53 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:34:53 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:34:53 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:34:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:34:53 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:34:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:34:54 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:34:54 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:34:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c64dbfdb30e6f2bd91f9d7ba689f3dd89f62125a424c3c17fcee5620b2020a3`  
		Last Modified: Tue, 09 Aug 2022 18:36:41 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d40371db7868456b4ab64cfe248665bd0667efb13b1d7f88c53d2c2b119809`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6657ec397289e21433c76381c67362a8917b0a8a27d3fed327a468a29c51d1c`  
		Last Modified: Tue, 09 Aug 2022 18:36:39 GMT  
		Size: 2.7 MB (2726758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a22238d642dd432a127e2b9748eca1a5c7257af11d7e79d3ab7fcff4d7ae94d`  
		Last Modified: Tue, 09 Aug 2022 18:36:40 GMT  
		Size: 2.7 MB (2731661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23a4112d585d674763eebdc058f2e3c60c68d8ae5d07c49b0b2c83965298a4`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38d0f5cf90ae3f376a3e1abb98ea29aed2da199c6fd97b39df16deb70fc968`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:e37161cd4b8b5bed14a49cfdad3e2a9c48b7313e94c982463c045ad10aca8c31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc95519b4a1c840f914d74fc894264484613be3a619f55381b34c446cafd39c0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:40 GMT
ADD file:541b767b21b9e0c4dab118d5e000990da3dbb81b547c1ee9941e2cf7edc5edd6 in / 
# Tue, 09 Aug 2022 17:49:40 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:51:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:51:03 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:51:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:51:06 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:52:08 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:52:08 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:52:09 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:52:09 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:52:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:52:09 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:52:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:52:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b423ab447fbb66b194458908339addbb5dd52e4aa7d04a42b387cdc07bbd92a1`  
		Last Modified: Tue, 09 Aug 2022 17:51:16 GMT  
		Size: 2.6 MB (2633535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ab43c4ab8ce3acf894fb689d3fab3e352715d608c94c7ee0ee865b529cec6d`  
		Last Modified: Tue, 09 Aug 2022 18:54:29 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511cfb58f000c475f12763f9367d55beb8423621bb6a35bf8a7f715cd1fb1a30`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 10.4 KB (10408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfec0ee07b8315970755477fe547e30ce338e99e7c00565c182a9ca59b5c8a8`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2653209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfdb869195492c054c5600ff7528f0f9520281927b6ca195486d47254674c16`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2686830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2676ad94b7d2ef8b194fb1d5a76635d4965833ee34cd876da2d48abdd5bcaa`  
		Last Modified: Tue, 09 Aug 2022 18:54:26 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f913ef8822c4a99179c9d88e1dfe63f9c4eeac5c6295fbaff2d605b4524077c0`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:8742e15342a7bbb16cc67080eccdad43c562b9247eed84b3f3d15597539aaf64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8207176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b4ec7917ffc45ea7312ef4cf881e890014f297d9e004c853ba3dede9415098`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:31:50 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:31:51 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:31:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:31:54 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 19 Jul 2022 23:32:58 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:32:59 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:33:00 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:33:01 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:33:02 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:33:03 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:33:04 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:33:05 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:33:06 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:33:08 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:33:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:33:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:33:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dbac81bec09c0716eeeccdb6afbe623c4b8ad08f044642623c18f6af531b54`  
		Last Modified: Tue, 19 Jul 2022 23:33:49 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facbeba827e8fea73efa4f1f728fc01d423230fae7e1342b0f9a67574897107f`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 10.5 KB (10477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b1b679b927f7031cc1fe1185ced237ba184e9a5e7dbf5ba545723f62724180`  
		Last Modified: Tue, 19 Jul 2022 23:33:48 GMT  
		Size: 2.8 MB (2752055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3002264c65c5b51440a2a94ca4a4c51c9528612157a97ff0cdf707e1336bd59`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 2.7 MB (2719681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6f183367dbe30deb5c145276f489d7096d50a04afa5b1965dae7070e047c01`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d6ce2389c0c1a1906fc6ce831a96187e0f16e312754a5450604ce448173579`  
		Last Modified: Tue, 19 Jul 2022 23:33:47 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
