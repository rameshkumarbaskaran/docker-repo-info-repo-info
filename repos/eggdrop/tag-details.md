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
$ docker pull eggdrop@sha256:00bafe9755bf4566cd934efc8331b4808c791ba58ab48562fa5706a8f1aab2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:60ceef04f82725229f4142a1718825787afef319fc561ac5e5fbf5b891ab74c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8285159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c226dc9ecbca7ff9f87c364811300bea754c9dae86a46350d068d6d6945e076`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:26 GMT
ADD file:e15461ac94648d9599df6304a53587fc8bfceaf6e111ee5917860e95ed9e751c in / 
# Tue, 19 Jul 2022 22:20:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:27:02 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:27:02 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:27:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:27:05 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 19 Jul 2022 23:27:57 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:27:57 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:27:58 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:27:58 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:27:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:27:58 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:27:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:27:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:27:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:27:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:627fad6f28f79c3907ad18a4399be4d810c0e1bb503fe3712217145c555b9d2f`  
		Last Modified: Tue, 19 Jul 2022 22:21:04 GMT  
		Size: 2.8 MB (2819330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f770a632361cf9cea49989f949de73ee9e48ea317060abb35b17bee6b01513f`  
		Last Modified: Tue, 19 Jul 2022 23:28:37 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a30e7236e85450cc17ec8a60c0c319c1f8b2add38c7813beb4bfad61352f5b3`  
		Last Modified: Tue, 19 Jul 2022 23:28:34 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38ee08ca5821f33d5f20cc67b74b01f9cb58c7a4284d180a07407040a6f0034`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 2.7 MB (2726723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde00d776b2c5bd316ea70b4fdf9ccd98b164d2ae1945aff1fdef55f3b4e6dec`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 2.7 MB (2724626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c7d8b6fe54697388caf64d137daf0de89bb3fd52a745d43c8bca33fd3ee098`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0effa4b67fa5f1ff7ebb646bd5601ee0df7971dc4d1ddc9e017dd33505e424c`  
		Last Modified: Tue, 19 Jul 2022 23:28:34 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5f612a73564453d842b4d792dc9ae6e4242412b5b7a032b475c5be472d28e6d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5abfb1dcefa42801e88040dbbcf28f1a958831415925b1b8f6be8fffc8808`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:42:42 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:42:43 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:42:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 03:42:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 03:45:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 03:45:10 GMT
ENV NICK=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV SERVER=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 03:45:12 GMT
ENV OWNER=
# Tue, 05 Apr 2022 03:45:12 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 03:45:12 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 03:45:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 03:45:13 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 03:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 03:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d0875ece6437b7759f658b19a743c65d8a0209dd6959b89006f06a7d4632d`  
		Last Modified: Tue, 05 Apr 2022 03:46:25 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2483aeba1bc6bf4edfd57deb0a196f319c5338bf1032faa780a5f7d392477`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 10.4 KB (10403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883dd4bb4066fb7e7baa70d4271a40c7d91977982d50cc6b30892462da59f8b`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2653002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c32b092000a7f5deeebdd19f48bf387342a0106dd81e475ba6110f073171679`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2683288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45089181a50f12a8dcd62efc9ad43f63605aece6c118eddafefa51dfb361fc4`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43385cdd604f9bac361f23a6a138a6e0e979410600f0c9a4d4fc9f564b16e1a`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 703.0 B  
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
$ docker pull eggdrop@sha256:00bafe9755bf4566cd934efc8331b4808c791ba58ab48562fa5706a8f1aab2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.2` - linux; amd64

```console
$ docker pull eggdrop@sha256:60ceef04f82725229f4142a1718825787afef319fc561ac5e5fbf5b891ab74c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8285159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c226dc9ecbca7ff9f87c364811300bea754c9dae86a46350d068d6d6945e076`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:26 GMT
ADD file:e15461ac94648d9599df6304a53587fc8bfceaf6e111ee5917860e95ed9e751c in / 
# Tue, 19 Jul 2022 22:20:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:27:02 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:27:02 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:27:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:27:05 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 19 Jul 2022 23:27:57 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:27:57 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:27:58 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:27:58 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:27:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:27:58 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:27:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:27:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:27:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:27:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:627fad6f28f79c3907ad18a4399be4d810c0e1bb503fe3712217145c555b9d2f`  
		Last Modified: Tue, 19 Jul 2022 22:21:04 GMT  
		Size: 2.8 MB (2819330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f770a632361cf9cea49989f949de73ee9e48ea317060abb35b17bee6b01513f`  
		Last Modified: Tue, 19 Jul 2022 23:28:37 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a30e7236e85450cc17ec8a60c0c319c1f8b2add38c7813beb4bfad61352f5b3`  
		Last Modified: Tue, 19 Jul 2022 23:28:34 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38ee08ca5821f33d5f20cc67b74b01f9cb58c7a4284d180a07407040a6f0034`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 2.7 MB (2726723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde00d776b2c5bd316ea70b4fdf9ccd98b164d2ae1945aff1fdef55f3b4e6dec`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 2.7 MB (2724626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c7d8b6fe54697388caf64d137daf0de89bb3fd52a745d43c8bca33fd3ee098`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0effa4b67fa5f1ff7ebb646bd5601ee0df7971dc4d1ddc9e017dd33505e424c`  
		Last Modified: Tue, 19 Jul 2022 23:28:34 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.2` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5f612a73564453d842b4d792dc9ae6e4242412b5b7a032b475c5be472d28e6d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5abfb1dcefa42801e88040dbbcf28f1a958831415925b1b8f6be8fffc8808`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:42:42 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:42:43 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:42:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 03:42:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 03:45:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 03:45:10 GMT
ENV NICK=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV SERVER=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 03:45:12 GMT
ENV OWNER=
# Tue, 05 Apr 2022 03:45:12 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 03:45:12 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 03:45:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 03:45:13 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 03:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 03:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d0875ece6437b7759f658b19a743c65d8a0209dd6959b89006f06a7d4632d`  
		Last Modified: Tue, 05 Apr 2022 03:46:25 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2483aeba1bc6bf4edfd57deb0a196f319c5338bf1032faa780a5f7d392477`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 10.4 KB (10403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883dd4bb4066fb7e7baa70d4271a40c7d91977982d50cc6b30892462da59f8b`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2653002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c32b092000a7f5deeebdd19f48bf387342a0106dd81e475ba6110f073171679`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2683288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45089181a50f12a8dcd62efc9ad43f63605aece6c118eddafefa51dfb361fc4`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43385cdd604f9bac361f23a6a138a6e0e979410600f0c9a4d4fc9f564b16e1a`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 703.0 B  
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
$ docker pull eggdrop@sha256:a14e00f626e02d8ad1b95c3e5ca5c383ebae367345516904956dae38425df81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.3rc1` - linux; amd64

```console
$ docker pull eggdrop@sha256:dad3de2ceae1edc30c94a020e51b8f117fe88687a4b90a5b0fae73a1dc062c87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8171743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02efe040da836aa57f0fc9d953b58dc8d4e971cf1cf9aea1fc6d513dacf57619`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:01:24 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 18 Jul 2022 21:01:24 GMT
RUN adduser -S eggdrop
# Mon, 18 Jul 2022 21:01:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 21:01:27 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 18 Jul 2022 21:02:24 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3rc1.tar.gz.asc eggdrop-1.9.3rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3rc1.tar.gz.asc   && tar -zxvf eggdrop-1.9.3rc1.tar.gz   && rm eggdrop-1.9.3rc1.tar.gz   && ( cd eggdrop-1.9.3rc1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 21:02:24 GMT
ENV NICK=
# Mon, 18 Jul 2022 21:02:24 GMT
ENV SERVER=
# Mon, 18 Jul 2022 21:02:25 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 21:02:25 GMT
ENV OWNER=
# Mon, 18 Jul 2022 21:02:25 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 21:02:25 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 21:02:25 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 21:02:25 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 21:02:25 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 21:02:25 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 21:02:25 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 21:02:26 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dc67a7e62653d3846f08f84471b9d69a994cbb65f61425bbb86789475917dd`  
		Last Modified: Mon, 18 Jul 2022 21:02:47 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44665cacec565984be192fed4481df67032270ff87621de84494750202fe6c2b`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 10.9 KB (10908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8ac8c6454f50c944d90e0d8d14c98a98f9a1fe4809a9b1ec66b8e17d566baf`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 2.8 MB (2757814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43094664a37e2581a99fc1d530a8ad5568f27fe1f27d3093190647d2a762d648`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 2.6 MB (2600417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abda0d4645ea0f771a0113ecd80da64e140385c5eb2b174a4a55e4e85b1fec6`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3611e0f5adbbc773b05f65982e3c0ac7412efabeb0553de5dbe6f6af2e0f163`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.3rc1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:3fdfbb48bef53ae668389c730f5c3374d7bfa5f21df8f0d537ae937e9fbc3888
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ff1592841c57427e2cc36617955b8692957eb7dd6426138ee2af26166ce1ec`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 20:20:26 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 18 Jul 2022 20:20:27 GMT
RUN adduser -S eggdrop
# Mon, 18 Jul 2022 20:20:29 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 20:20:33 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 18 Jul 2022 20:23:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3rc1.tar.gz.asc eggdrop-1.9.3rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3rc1.tar.gz.asc   && tar -zxvf eggdrop-1.9.3rc1.tar.gz   && rm eggdrop-1.9.3rc1.tar.gz   && ( cd eggdrop-1.9.3rc1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 20:23:11 GMT
ENV NICK=
# Mon, 18 Jul 2022 20:23:11 GMT
ENV SERVER=
# Mon, 18 Jul 2022 20:23:12 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 20:23:12 GMT
ENV OWNER=
# Mon, 18 Jul 2022 20:23:12 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 20:23:13 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 20:23:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 20:23:14 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 20:23:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 20:23:15 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 20:23:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 20:23:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bf358da359bc34c989093c8a871f385d0b108bcf3fce18cdac4d543bd07da0`  
		Last Modified: Mon, 18 Jul 2022 20:24:12 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655d344c5652d10ea25461fe0aac12fa4820915b1dad8c306d3d481a01e8ba84`  
		Last Modified: Mon, 18 Jul 2022 20:24:10 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be3cf31cfdee484cf0e9f19889179f59587f5820afc365d5c921112ccbcad75`  
		Last Modified: Mon, 18 Jul 2022 20:24:12 GMT  
		Size: 2.7 MB (2679937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8741adee0ec9c7ad2d0f393d15a09cdb10d3771bb7dc910291696770356442f3`  
		Last Modified: Mon, 18 Jul 2022 20:24:12 GMT  
		Size: 2.6 MB (2614606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7150238cd34be8f321787abb7669f6b2de34281b317ea63d6ac52bdd333a77d`  
		Last Modified: Mon, 18 Jul 2022 20:24:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f06965c294b5f1246fb6700d2fac17ddc7b58475ced817eee9bf8c7358e84f`  
		Last Modified: Mon, 18 Jul 2022 20:24:10 GMT  
		Size: 703.0 B  
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
$ docker pull eggdrop@sha256:0b7c2c3e25a3a20af54a60ce2c5b529901de52e169d6f8d1e3cd2e7c25ce6636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:167357057c64dbf146d6be251a103b299f818ee33114b1b8aa9ec38e4ba373df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39683291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dfc58496b5a1cf0c69dbe6533fbce4c0538431eb735fca60b4682a68bc1f53`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:22:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:22:54 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:22:55 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:22:56 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 19 Jul 2022 23:22:56 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 19 Jul 2022 23:22:57 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 19 Jul 2022 23:26:55 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:26:56 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:26:56 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:26:56 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:26:56 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:26:56 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:26:56 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:26:56 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:26:56 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:26:57 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:26:57 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:26:57 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:26:57 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce3ee76f2e28d4dd47d43d3605eb1c6af0e96fcafc28de6ec5379c5172ebb55`  
		Last Modified: Tue, 19 Jul 2022 23:28:25 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ac4a1d51bd2cc5020a4d0d0e2169d5cedbe911ba463dea6ad06a6a6ff0596d`  
		Last Modified: Tue, 19 Jul 2022 23:28:23 GMT  
		Size: 10.9 KB (10940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1db5a3780dd3366d59813dc8b37cd5cb8f7af399f04e32d57c1928fd9d4d9b2`  
		Last Modified: Tue, 19 Jul 2022 23:28:23 GMT  
		Size: 1.1 MB (1089912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d536323f2786afb7faba1bacc8dd118128b0aa364ef3b02502548c995c77e6a`  
		Last Modified: Tue, 19 Jul 2022 23:28:28 GMT  
		Size: 35.8 MB (35763938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191c01706265110ab1e69ea5fb73fa571136f6bf45e57291a2257228da38f09e`  
		Last Modified: Tue, 19 Jul 2022 23:28:23 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db96b5e1af04782658496a1aec79cbf4703fb50cbe4647b25442b945f4e9f4b3`  
		Last Modified: Tue, 19 Jul 2022 23:28:23 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c9e126616745f437a1316d309084832d58151fafeb28b07c662db54fad03cf70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40314778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545abc69ab2eef92b2edbf01cbdd08740e6842bd1e6b477d8e6047b6b96f7fe4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:31:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:31:46 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:31:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 18:49:45 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Mon, 18 Jul 2022 18:49:45 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Mon, 18 Jul 2022 18:49:48 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 18 Jul 2022 19:00:28 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 19:00:29 GMT
ENV NICK=
# Mon, 18 Jul 2022 19:00:29 GMT
ENV SERVER=
# Mon, 18 Jul 2022 19:00:29 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 19:00:30 GMT
ENV OWNER=
# Mon, 18 Jul 2022 19:00:30 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 19:00:31 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 19:00:31 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 19:00:31 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 19:00:32 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 19:00:32 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 19:00:33 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 19:00:33 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f46acd206d1b9854dd7a69f3dd94d51ffb03228b347337d6755524e938f848d`  
		Last Modified: Tue, 05 Apr 2022 03:45:57 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ab9123d31326e4f773e35061abb57883ec6b6221e6df8719354fc8598c9123`  
		Last Modified: Tue, 05 Apr 2022 03:45:55 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f36aa237eb1d5a61f87401541fbc3b6b7c9fa196207eeb0fa78f126ff9145e`  
		Last Modified: Mon, 18 Jul 2022 19:04:34 GMT  
		Size: 1.0 MB (1032591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad3257c3ec35772168580fe6515ac2a515576ab7e6ea173ee9db5868c50f2c8`  
		Last Modified: Mon, 18 Jul 2022 19:04:58 GMT  
		Size: 36.6 MB (36645704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bd986b36f8bae82826097ae809bd11ee15f40d48ba1753fc9a8309e4bc9772`  
		Last Modified: Mon, 18 Jul 2022 19:04:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac6a5f8fc7f345fdc59052ce1153c7fc0f3c4e559a2ec14f6baaf732376285`  
		Last Modified: Mon, 18 Jul 2022 19:04:33 GMT  
		Size: 707.0 B  
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
$ docker pull eggdrop@sha256:00bafe9755bf4566cd934efc8331b4808c791ba58ab48562fa5706a8f1aab2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:60ceef04f82725229f4142a1718825787afef319fc561ac5e5fbf5b891ab74c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8285159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c226dc9ecbca7ff9f87c364811300bea754c9dae86a46350d068d6d6945e076`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:26 GMT
ADD file:e15461ac94648d9599df6304a53587fc8bfceaf6e111ee5917860e95ed9e751c in / 
# Tue, 19 Jul 2022 22:20:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:27:02 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:27:02 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:27:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:27:05 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 19 Jul 2022 23:27:57 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:27:57 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:27:58 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:27:58 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:27:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:27:58 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:27:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:27:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:27:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:27:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:627fad6f28f79c3907ad18a4399be4d810c0e1bb503fe3712217145c555b9d2f`  
		Last Modified: Tue, 19 Jul 2022 22:21:04 GMT  
		Size: 2.8 MB (2819330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f770a632361cf9cea49989f949de73ee9e48ea317060abb35b17bee6b01513f`  
		Last Modified: Tue, 19 Jul 2022 23:28:37 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a30e7236e85450cc17ec8a60c0c319c1f8b2add38c7813beb4bfad61352f5b3`  
		Last Modified: Tue, 19 Jul 2022 23:28:34 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38ee08ca5821f33d5f20cc67b74b01f9cb58c7a4284d180a07407040a6f0034`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 2.7 MB (2726723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde00d776b2c5bd316ea70b4fdf9ccd98b164d2ae1945aff1fdef55f3b4e6dec`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 2.7 MB (2724626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c7d8b6fe54697388caf64d137daf0de89bb3fd52a745d43c8bca33fd3ee098`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0effa4b67fa5f1ff7ebb646bd5601ee0df7971dc4d1ddc9e017dd33505e424c`  
		Last Modified: Tue, 19 Jul 2022 23:28:34 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5f612a73564453d842b4d792dc9ae6e4242412b5b7a032b475c5be472d28e6d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5abfb1dcefa42801e88040dbbcf28f1a958831415925b1b8f6be8fffc8808`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:42:42 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:42:43 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:42:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 03:42:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 03:45:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 03:45:10 GMT
ENV NICK=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV SERVER=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 03:45:12 GMT
ENV OWNER=
# Tue, 05 Apr 2022 03:45:12 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 03:45:12 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 03:45:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 03:45:13 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 03:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 03:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d0875ece6437b7759f658b19a743c65d8a0209dd6959b89006f06a7d4632d`  
		Last Modified: Tue, 05 Apr 2022 03:46:25 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2483aeba1bc6bf4edfd57deb0a196f319c5338bf1032faa780a5f7d392477`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 10.4 KB (10403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883dd4bb4066fb7e7baa70d4271a40c7d91977982d50cc6b30892462da59f8b`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2653002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c32b092000a7f5deeebdd19f48bf387342a0106dd81e475ba6110f073171679`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2683288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45089181a50f12a8dcd62efc9ad43f63605aece6c118eddafefa51dfb361fc4`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43385cdd604f9bac361f23a6a138a6e0e979410600f0c9a4d4fc9f564b16e1a`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 703.0 B  
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
$ docker pull eggdrop@sha256:00bafe9755bf4566cd934efc8331b4808c791ba58ab48562fa5706a8f1aab2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:60ceef04f82725229f4142a1718825787afef319fc561ac5e5fbf5b891ab74c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8285159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c226dc9ecbca7ff9f87c364811300bea754c9dae86a46350d068d6d6945e076`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:26 GMT
ADD file:e15461ac94648d9599df6304a53587fc8bfceaf6e111ee5917860e95ed9e751c in / 
# Tue, 19 Jul 2022 22:20:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:27:02 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:27:02 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:27:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:27:05 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 19 Jul 2022 23:27:57 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:27:57 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:27:58 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:27:58 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:27:58 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:27:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:27:58 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:27:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:27:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:27:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:27:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:627fad6f28f79c3907ad18a4399be4d810c0e1bb503fe3712217145c555b9d2f`  
		Last Modified: Tue, 19 Jul 2022 22:21:04 GMT  
		Size: 2.8 MB (2819330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f770a632361cf9cea49989f949de73ee9e48ea317060abb35b17bee6b01513f`  
		Last Modified: Tue, 19 Jul 2022 23:28:37 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a30e7236e85450cc17ec8a60c0c319c1f8b2add38c7813beb4bfad61352f5b3`  
		Last Modified: Tue, 19 Jul 2022 23:28:34 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38ee08ca5821f33d5f20cc67b74b01f9cb58c7a4284d180a07407040a6f0034`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 2.7 MB (2726723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde00d776b2c5bd316ea70b4fdf9ccd98b164d2ae1945aff1fdef55f3b4e6dec`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 2.7 MB (2724626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c7d8b6fe54697388caf64d137daf0de89bb3fd52a745d43c8bca33fd3ee098`  
		Last Modified: Tue, 19 Jul 2022 23:28:35 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0effa4b67fa5f1ff7ebb646bd5601ee0df7971dc4d1ddc9e017dd33505e424c`  
		Last Modified: Tue, 19 Jul 2022 23:28:34 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5f612a73564453d842b4d792dc9ae6e4242412b5b7a032b475c5be472d28e6d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5abfb1dcefa42801e88040dbbcf28f1a958831415925b1b8f6be8fffc8808`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:42:42 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:42:43 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:42:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 03:42:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 03:45:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 03:45:10 GMT
ENV NICK=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV SERVER=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 03:45:12 GMT
ENV OWNER=
# Tue, 05 Apr 2022 03:45:12 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 03:45:12 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 03:45:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 03:45:13 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 03:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 03:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d0875ece6437b7759f658b19a743c65d8a0209dd6959b89006f06a7d4632d`  
		Last Modified: Tue, 05 Apr 2022 03:46:25 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2483aeba1bc6bf4edfd57deb0a196f319c5338bf1032faa780a5f7d392477`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 10.4 KB (10403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883dd4bb4066fb7e7baa70d4271a40c7d91977982d50cc6b30892462da59f8b`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2653002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c32b092000a7f5deeebdd19f48bf387342a0106dd81e475ba6110f073171679`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2683288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45089181a50f12a8dcd62efc9ad43f63605aece6c118eddafefa51dfb361fc4`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43385cdd604f9bac361f23a6a138a6e0e979410600f0c9a4d4fc9f564b16e1a`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 703.0 B  
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
