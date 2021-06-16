<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.8`](#eggdrop18)
-	[`eggdrop:1.8.4`](#eggdrop184)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.0`](#eggdrop190)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.8`

```console
$ docker pull eggdrop@sha256:9cd4a0b8fee593cecf08c504fdda01e5c5059bac191ae3d93d000300c743b98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:1.8` - linux; amd64

```console
$ docker pull eggdrop@sha256:22fd38405c2ac3cdf8a68bd99b6373b4ca3ef22326dc55a9040d27cdb6759c30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8800819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3205dc38d4bd88d8222c7146b241df75126c7c0e31c216683e9c3997b88d99b8`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:26:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:26:39 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:26:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:27:40 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:28:41 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:28:42 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:28:42 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:28:43 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:28:43 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:28:43 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:28:44 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:28:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:28:45 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:28:45 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:28:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:28:46 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:28:46 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9b60f543dd32d2ac2d7575d5ad495a35a0796146dbf47fd6c76f083f30d599`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714e89337f555b15f73058aa485a830db0f4a0bd40a36eccd6e66bf949c0259`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644dcb11463fdb7414f818b0e825bcf15eaa953f86758ed75844357ebc346a2`  
		Last Modified: Wed, 14 Apr 2021 20:31:10 GMT  
		Size: 2.7 MB (2685300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7baaf014b27977624d9dd6472d3430a5910795933ad31bd1af3b311726094f6`  
		Last Modified: Wed, 14 Apr 2021 20:31:10 GMT  
		Size: 3.3 MB (3285828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558533a61e7e9393619d8477302e7a4ceff2107098c41d808f7ed16746c16d25`  
		Last Modified: Wed, 14 Apr 2021 20:31:09 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7459735fb3d77e7827bdbc52771965f821916df4851f7e0295c2717958bac34`  
		Last Modified: Wed, 14 Apr 2021 20:31:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.8.4`

```console
$ docker pull eggdrop@sha256:9cd4a0b8fee593cecf08c504fdda01e5c5059bac191ae3d93d000300c743b98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:1.8.4` - linux; amd64

```console
$ docker pull eggdrop@sha256:22fd38405c2ac3cdf8a68bd99b6373b4ca3ef22326dc55a9040d27cdb6759c30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8800819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3205dc38d4bd88d8222c7146b241df75126c7c0e31c216683e9c3997b88d99b8`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:26:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:26:39 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:26:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:27:40 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:28:41 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:28:42 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:28:42 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:28:43 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:28:43 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:28:43 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:28:44 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:28:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:28:45 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:28:45 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:28:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:28:46 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:28:46 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9b60f543dd32d2ac2d7575d5ad495a35a0796146dbf47fd6c76f083f30d599`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714e89337f555b15f73058aa485a830db0f4a0bd40a36eccd6e66bf949c0259`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644dcb11463fdb7414f818b0e825bcf15eaa953f86758ed75844357ebc346a2`  
		Last Modified: Wed, 14 Apr 2021 20:31:10 GMT  
		Size: 2.7 MB (2685300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7baaf014b27977624d9dd6472d3430a5910795933ad31bd1af3b311726094f6`  
		Last Modified: Wed, 14 Apr 2021 20:31:10 GMT  
		Size: 3.3 MB (3285828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558533a61e7e9393619d8477302e7a4ceff2107098c41d808f7ed16746c16d25`  
		Last Modified: Wed, 14 Apr 2021 20:31:09 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7459735fb3d77e7827bdbc52771965f821916df4851f7e0295c2717958bac34`  
		Last Modified: Wed, 14 Apr 2021 20:31:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:4b967a6417260ba3cfdac1cc0ab5df7e84df69cad98aba730ccfc434f0bdab6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:e8c3fe57ff5964dd97a8d2a2a506f6a40031e625afb25bdb5b1ec22988823d56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8224211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b387e204eb1200e349577df42c08c9953800908b336091be2e20c92a264a611`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:28:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:28:54 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:28:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:29:00 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:30:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:30:28 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:30:28 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:30:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:30:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:30:29 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:30:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:30:30 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1d9ab058af7106893a1ba77f9ca0b3a58052b9ae5066905c6f7ae26c94434`  
		Last Modified: Wed, 14 Apr 2021 20:31:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76394ca5ad9f94b4ac3d2cb72f4bcd6e7eb23df13adb36a6b732b4e11bf4e9a3`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 10.1 KB (10113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb74bc16f4c16d3b897fd84478f8df97a60b755eee63f8202139c5e4937537d`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2724472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee19a14cecf7a9a8b0e86b924d4aa1db06886f93b75039bac7d4d5eaa83bdbc`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2673860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5976395ecd64a6b14179cdbc52fceecb422cac42f1f9ed9cb4880fe7b563ed58`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa43e66c459b027e8b1e3088b3b265682a436283838f3687b2f71c18be678e8`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:78d4ef27cb29911685f18cdb92cfa41270f510f6e8d3592cb6be006bb87fd2b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52238f34cb3a55328a8ec63d83fbf69536f22afc05543942adae191aa86b4d4f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:56:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:57:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:57:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:57:16 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:59:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:59:13 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:59:14 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:59:15 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:59:16 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:59:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:59:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:59:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:59:25 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:59:30 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:59:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:59:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:59:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231f03afe8c29e8696ea3a9a12fa671d754a62a9c635382104d12dec2757072`  
		Last Modified: Wed, 14 Apr 2021 20:00:13 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf18f1d89826a83b49120673b77422238266894b80701441d516f79823588`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 9.8 KB (9830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e9e82dddc9b362ff5bb8a7f2a880e794e14e3d8e734ef0d6614f14bf56ffb`  
		Last Modified: Wed, 14 Apr 2021 20:00:14 GMT  
		Size: 2.7 MB (2652131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef3b98fe7b74dd2000c22edd32faf39f1067b9fa39efb1e59eb3ab209205275`  
		Last Modified: Wed, 14 Apr 2021 20:00:12 GMT  
		Size: 2.6 MB (2633547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b6a123b9dd6f23ecf8478d53dddf1407060d2f980725386ca54df4afca2c9`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a75460f30a5e4255854c4a9f16faf02f30eee88b4615b3fba025dbc0b2852`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2bbe127552ec58191550d7af38e5e2a838fa635f56809e3e1db2dd36d4c67b84
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8545444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c083b0cc317aeae61bb347db85d1822ff0e19726d88c403267ccf53d69acc3f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:30:50 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:30:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:30:53 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 15 Jun 2021 23:31:58 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 15 Jun 2021 23:31:58 GMT
ENV NICK=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV SERVER=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV LISTEN=3333
# Tue, 15 Jun 2021 23:31:59 GMT
ENV OWNER=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV USERFILE=eggdrop.user
# Tue, 15 Jun 2021 23:31:59 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 15 Jun 2021 23:32:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 15 Jun 2021 23:32:00 GMT
EXPOSE 3333
# Tue, 15 Jun 2021 23:32:00 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 15 Jun 2021 23:32:00 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 15 Jun 2021 23:32:00 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 15 Jun 2021 23:32:01 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3db2720b6273728863ce64bb67670c4aae649525cf85a5bc0834bd557c60028`  
		Last Modified: Tue, 15 Jun 2021 23:32:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960848fa3748666f162fe523f04c331adba985f24d63933d5aaf1e2a0e75c5b`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ebe6949c44b5c5569f8ee4c4dfe8132fc69db2ae59ed92a76bdcbbc5e5784`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 2.8 MB (2752462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d22cbebba2d9d664edeb72f9753d029f7909f033180536e04e09e7bccb03f5`  
		Last Modified: Tue, 15 Jun 2021 23:32:41 GMT  
		Size: 3.1 MB (3067159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e77d1989915493443764c02f12bfcecfcf3dece3248728da041a83a0c5d891`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5c799a3dc8fd10c393bea631747cb9e9888405244a3e7bdb38e294584a0e35`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.0`

```console
$ docker pull eggdrop@sha256:4b967a6417260ba3cfdac1cc0ab5df7e84df69cad98aba730ccfc434f0bdab6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.0` - linux; amd64

```console
$ docker pull eggdrop@sha256:e8c3fe57ff5964dd97a8d2a2a506f6a40031e625afb25bdb5b1ec22988823d56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8224211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b387e204eb1200e349577df42c08c9953800908b336091be2e20c92a264a611`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:28:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:28:54 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:28:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:29:00 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:30:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:30:28 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:30:28 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:30:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:30:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:30:29 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:30:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:30:30 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1d9ab058af7106893a1ba77f9ca0b3a58052b9ae5066905c6f7ae26c94434`  
		Last Modified: Wed, 14 Apr 2021 20:31:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76394ca5ad9f94b4ac3d2cb72f4bcd6e7eb23df13adb36a6b732b4e11bf4e9a3`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 10.1 KB (10113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb74bc16f4c16d3b897fd84478f8df97a60b755eee63f8202139c5e4937537d`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2724472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee19a14cecf7a9a8b0e86b924d4aa1db06886f93b75039bac7d4d5eaa83bdbc`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2673860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5976395ecd64a6b14179cdbc52fceecb422cac42f1f9ed9cb4880fe7b563ed58`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa43e66c459b027e8b1e3088b3b265682a436283838f3687b2f71c18be678e8`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.0` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:78d4ef27cb29911685f18cdb92cfa41270f510f6e8d3592cb6be006bb87fd2b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52238f34cb3a55328a8ec63d83fbf69536f22afc05543942adae191aa86b4d4f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:56:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:57:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:57:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:57:16 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:59:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:59:13 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:59:14 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:59:15 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:59:16 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:59:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:59:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:59:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:59:25 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:59:30 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:59:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:59:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:59:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231f03afe8c29e8696ea3a9a12fa671d754a62a9c635382104d12dec2757072`  
		Last Modified: Wed, 14 Apr 2021 20:00:13 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf18f1d89826a83b49120673b77422238266894b80701441d516f79823588`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 9.8 KB (9830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e9e82dddc9b362ff5bb8a7f2a880e794e14e3d8e734ef0d6614f14bf56ffb`  
		Last Modified: Wed, 14 Apr 2021 20:00:14 GMT  
		Size: 2.7 MB (2652131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef3b98fe7b74dd2000c22edd32faf39f1067b9fa39efb1e59eb3ab209205275`  
		Last Modified: Wed, 14 Apr 2021 20:00:12 GMT  
		Size: 2.6 MB (2633547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b6a123b9dd6f23ecf8478d53dddf1407060d2f980725386ca54df4afca2c9`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a75460f30a5e4255854c4a9f16faf02f30eee88b4615b3fba025dbc0b2852`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.0` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2bbe127552ec58191550d7af38e5e2a838fa635f56809e3e1db2dd36d4c67b84
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8545444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c083b0cc317aeae61bb347db85d1822ff0e19726d88c403267ccf53d69acc3f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:30:50 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:30:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:30:53 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 15 Jun 2021 23:31:58 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 15 Jun 2021 23:31:58 GMT
ENV NICK=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV SERVER=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV LISTEN=3333
# Tue, 15 Jun 2021 23:31:59 GMT
ENV OWNER=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV USERFILE=eggdrop.user
# Tue, 15 Jun 2021 23:31:59 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 15 Jun 2021 23:32:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 15 Jun 2021 23:32:00 GMT
EXPOSE 3333
# Tue, 15 Jun 2021 23:32:00 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 15 Jun 2021 23:32:00 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 15 Jun 2021 23:32:00 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 15 Jun 2021 23:32:01 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3db2720b6273728863ce64bb67670c4aae649525cf85a5bc0834bd557c60028`  
		Last Modified: Tue, 15 Jun 2021 23:32:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960848fa3748666f162fe523f04c331adba985f24d63933d5aaf1e2a0e75c5b`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ebe6949c44b5c5569f8ee4c4dfe8132fc69db2ae59ed92a76bdcbbc5e5784`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 2.8 MB (2752462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d22cbebba2d9d664edeb72f9753d029f7909f033180536e04e09e7bccb03f5`  
		Last Modified: Tue, 15 Jun 2021 23:32:41 GMT  
		Size: 3.1 MB (3067159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e77d1989915493443764c02f12bfcecfcf3dece3248728da041a83a0c5d891`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5c799a3dc8fd10c393bea631747cb9e9888405244a3e7bdb38e294584a0e35`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:78506c59d37a6e1113285c2774fd1793ebedcd774def601256c1eb228a497551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:863a1dca7315a511d83332073aacfa18fac03397358b5fe5ba2e7b8a75a276e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13903044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576dc66e6ec6201c1e65dcb5da0e0c2fa11511e7a1501fbe397e97153707e91c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:26:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:26:39 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:26:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:26:41 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Wed, 14 Apr 2021 20:26:41 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Wed, 14 Apr 2021 20:26:42 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:27:33 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:27:33 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:27:34 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:27:34 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:27:34 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:27:34 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:27:34 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:27:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:27:35 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:27:35 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:27:35 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:27:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:27:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9b60f543dd32d2ac2d7575d5ad495a35a0796146dbf47fd6c76f083f30d599`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714e89337f555b15f73058aa485a830db0f4a0bd40a36eccd6e66bf949c0259`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e603a0c1dc60f9e4445917bed7c38bd060a3e336da983bab83ed39e1d071ec3`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 2.7 MB (2685312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43656001cc97fbe42d47f6244dd22e9dc0d4091492bd2a44536fcb0aa27a7f4`  
		Last Modified: Wed, 14 Apr 2021 20:30:59 GMT  
		Size: 8.4 MB (8388045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6b5e043a85370cf7210f1f8531dbc218be306517c005b8eae5be566056b7f6`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914a952f41a10e7c83dd041fa5773f3c6328b582d6ea304077875cb445d9d06`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c3bf9c2cdda221f8f156f3057dd408719ef78bff09878a6c82205fd7b26d7d76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13560543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08412b7b45976542614516e11642429bae78a720cfd2198019236710aa3dc69`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:58 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Wed, 14 Apr 2021 18:49:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:53:23 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:53:38 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:53:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:53:49 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Wed, 14 Apr 2021 19:53:52 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Wed, 14 Apr 2021 19:54:07 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:56:19 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:56:21 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:56:24 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:56:26 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:56:27 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:56:29 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:56:31 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:56:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:56:34 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:56:36 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:56:39 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:56:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:56:41 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d78ffb0e230408fd608629b875c877407afeedd0a45af9c9ed2169117984a`  
		Last Modified: Wed, 14 Apr 2021 20:00:04 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c9123ad8d661005614f22f8c8a3d8e82e151f2596a6b93ce83809a14465b9b`  
		Last Modified: Wed, 14 Apr 2021 20:00:02 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d2497d083ecbb0cc42823a3ca7c0f6ad3b17b85d126e8bd66a9fdac142d9a3`  
		Last Modified: Wed, 14 Apr 2021 20:00:04 GMT  
		Size: 2.6 MB (2608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca996bb7fde0998b70d0a1136b7178cce6ed3fe68b18596b71e73446dc5aa649`  
		Last Modified: Wed, 14 Apr 2021 20:00:05 GMT  
		Size: 8.3 MB (8316642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd72ae776e770eebcfd03df0c40615a2bdcc024cfe43b8e8e08c4ed405c121`  
		Last Modified: Wed, 14 Apr 2021 20:00:02 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dc612d9cb44bd8c9252e2c38ca1cc514123fa1a8af2c91306702bd2b6e3680`  
		Last Modified: Wed, 14 Apr 2021 20:00:02 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:e87dd640cc119ad6cc91c7dbe703dfcbffb44c99d5d58b9fdede0e2e6fddc128
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13869663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5cb57e2536eb4bfbac350e408633eab9e087280e4aef220187c4f603668c9e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:29:36 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:29:37 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:29:38 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:29:38 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Tue, 15 Jun 2021 23:29:39 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Tue, 15 Jun 2021 23:29:40 GMT
RUN apk --update add --no-cache tcl bash openssl
# Tue, 15 Jun 2021 23:30:41 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 15 Jun 2021 23:30:41 GMT
ENV NICK=
# Tue, 15 Jun 2021 23:30:41 GMT
ENV SERVER=
# Tue, 15 Jun 2021 23:30:41 GMT
ENV LISTEN=3333
# Tue, 15 Jun 2021 23:30:42 GMT
ENV OWNER=
# Tue, 15 Jun 2021 23:30:42 GMT
ENV USERFILE=eggdrop.user
# Tue, 15 Jun 2021 23:30:42 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 15 Jun 2021 23:30:42 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 15 Jun 2021 23:30:42 GMT
EXPOSE 3333
# Tue, 15 Jun 2021 23:30:43 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Tue, 15 Jun 2021 23:30:43 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 15 Jun 2021 23:30:43 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 15 Jun 2021 23:30:43 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c7539bf8879d1a52593f00c732dcc06de9183953717c4b4951f6b8d29cbbc1`  
		Last Modified: Tue, 15 Jun 2021 23:32:32 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7414aa2d3258c5ce8af602a09967cff2107fdb7e678a330b48e092a0cfca4a44`  
		Last Modified: Tue, 15 Jun 2021 23:32:29 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b401d7da2a0200684ac1edaf8b1cb70f8c7ddb0d17c029472fab8b4d4752741`  
		Last Modified: Tue, 15 Jun 2021 23:32:30 GMT  
		Size: 2.7 MB (2722562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae76c318549e2ba522e8be38f6995a9c1b0e24b4865a15d1273f6798f38047f`  
		Last Modified: Tue, 15 Jun 2021 23:32:31 GMT  
		Size: 8.4 MB (8406803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507f778e1558b2a7b849665e241d34d0b68775046d20328f4880170fc58a6e72`  
		Last Modified: Tue, 15 Jun 2021 23:32:29 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1de162c38f13e372ca3021007a34709f5f55d2398c025635b6e1f68b54f7da`  
		Last Modified: Tue, 15 Jun 2021 23:32:29 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:4b967a6417260ba3cfdac1cc0ab5df7e84df69cad98aba730ccfc434f0bdab6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:e8c3fe57ff5964dd97a8d2a2a506f6a40031e625afb25bdb5b1ec22988823d56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8224211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b387e204eb1200e349577df42c08c9953800908b336091be2e20c92a264a611`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:28:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:28:54 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:28:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:29:00 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:30:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:30:28 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:30:28 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:30:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:30:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:30:29 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:30:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:30:30 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1d9ab058af7106893a1ba77f9ca0b3a58052b9ae5066905c6f7ae26c94434`  
		Last Modified: Wed, 14 Apr 2021 20:31:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76394ca5ad9f94b4ac3d2cb72f4bcd6e7eb23df13adb36a6b732b4e11bf4e9a3`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 10.1 KB (10113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb74bc16f4c16d3b897fd84478f8df97a60b755eee63f8202139c5e4937537d`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2724472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee19a14cecf7a9a8b0e86b924d4aa1db06886f93b75039bac7d4d5eaa83bdbc`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2673860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5976395ecd64a6b14179cdbc52fceecb422cac42f1f9ed9cb4880fe7b563ed58`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa43e66c459b027e8b1e3088b3b265682a436283838f3687b2f71c18be678e8`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:78d4ef27cb29911685f18cdb92cfa41270f510f6e8d3592cb6be006bb87fd2b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52238f34cb3a55328a8ec63d83fbf69536f22afc05543942adae191aa86b4d4f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:56:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:57:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:57:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:57:16 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:59:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:59:13 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:59:14 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:59:15 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:59:16 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:59:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:59:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:59:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:59:25 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:59:30 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:59:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:59:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:59:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231f03afe8c29e8696ea3a9a12fa671d754a62a9c635382104d12dec2757072`  
		Last Modified: Wed, 14 Apr 2021 20:00:13 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf18f1d89826a83b49120673b77422238266894b80701441d516f79823588`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 9.8 KB (9830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e9e82dddc9b362ff5bb8a7f2a880e794e14e3d8e734ef0d6614f14bf56ffb`  
		Last Modified: Wed, 14 Apr 2021 20:00:14 GMT  
		Size: 2.7 MB (2652131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef3b98fe7b74dd2000c22edd32faf39f1067b9fa39efb1e59eb3ab209205275`  
		Last Modified: Wed, 14 Apr 2021 20:00:12 GMT  
		Size: 2.6 MB (2633547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b6a123b9dd6f23ecf8478d53dddf1407060d2f980725386ca54df4afca2c9`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a75460f30a5e4255854c4a9f16faf02f30eee88b4615b3fba025dbc0b2852`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2bbe127552ec58191550d7af38e5e2a838fa635f56809e3e1db2dd36d4c67b84
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8545444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c083b0cc317aeae61bb347db85d1822ff0e19726d88c403267ccf53d69acc3f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:30:50 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:30:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:30:53 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 15 Jun 2021 23:31:58 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 15 Jun 2021 23:31:58 GMT
ENV NICK=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV SERVER=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV LISTEN=3333
# Tue, 15 Jun 2021 23:31:59 GMT
ENV OWNER=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV USERFILE=eggdrop.user
# Tue, 15 Jun 2021 23:31:59 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 15 Jun 2021 23:32:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 15 Jun 2021 23:32:00 GMT
EXPOSE 3333
# Tue, 15 Jun 2021 23:32:00 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 15 Jun 2021 23:32:00 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 15 Jun 2021 23:32:00 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 15 Jun 2021 23:32:01 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3db2720b6273728863ce64bb67670c4aae649525cf85a5bc0834bd557c60028`  
		Last Modified: Tue, 15 Jun 2021 23:32:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960848fa3748666f162fe523f04c331adba985f24d63933d5aaf1e2a0e75c5b`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ebe6949c44b5c5569f8ee4c4dfe8132fc69db2ae59ed92a76bdcbbc5e5784`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 2.8 MB (2752462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d22cbebba2d9d664edeb72f9753d029f7909f033180536e04e09e7bccb03f5`  
		Last Modified: Tue, 15 Jun 2021 23:32:41 GMT  
		Size: 3.1 MB (3067159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e77d1989915493443764c02f12bfcecfcf3dece3248728da041a83a0c5d891`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5c799a3dc8fd10c393bea631747cb9e9888405244a3e7bdb38e294584a0e35`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:4b967a6417260ba3cfdac1cc0ab5df7e84df69cad98aba730ccfc434f0bdab6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:e8c3fe57ff5964dd97a8d2a2a506f6a40031e625afb25bdb5b1ec22988823d56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8224211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b387e204eb1200e349577df42c08c9953800908b336091be2e20c92a264a611`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:28:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:28:54 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:28:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:29:00 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:30:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:30:28 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:30:28 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:30:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:30:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:30:29 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:30:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:30:30 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1d9ab058af7106893a1ba77f9ca0b3a58052b9ae5066905c6f7ae26c94434`  
		Last Modified: Wed, 14 Apr 2021 20:31:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76394ca5ad9f94b4ac3d2cb72f4bcd6e7eb23df13adb36a6b732b4e11bf4e9a3`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 10.1 KB (10113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb74bc16f4c16d3b897fd84478f8df97a60b755eee63f8202139c5e4937537d`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2724472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee19a14cecf7a9a8b0e86b924d4aa1db06886f93b75039bac7d4d5eaa83bdbc`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2673860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5976395ecd64a6b14179cdbc52fceecb422cac42f1f9ed9cb4880fe7b563ed58`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa43e66c459b027e8b1e3088b3b265682a436283838f3687b2f71c18be678e8`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:78d4ef27cb29911685f18cdb92cfa41270f510f6e8d3592cb6be006bb87fd2b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52238f34cb3a55328a8ec63d83fbf69536f22afc05543942adae191aa86b4d4f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:56:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:57:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:57:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:57:16 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:59:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:59:13 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:59:14 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:59:15 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:59:16 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:59:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:59:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:59:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:59:25 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:59:30 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:59:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:59:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:59:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231f03afe8c29e8696ea3a9a12fa671d754a62a9c635382104d12dec2757072`  
		Last Modified: Wed, 14 Apr 2021 20:00:13 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf18f1d89826a83b49120673b77422238266894b80701441d516f79823588`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 9.8 KB (9830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e9e82dddc9b362ff5bb8a7f2a880e794e14e3d8e734ef0d6614f14bf56ffb`  
		Last Modified: Wed, 14 Apr 2021 20:00:14 GMT  
		Size: 2.7 MB (2652131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef3b98fe7b74dd2000c22edd32faf39f1067b9fa39efb1e59eb3ab209205275`  
		Last Modified: Wed, 14 Apr 2021 20:00:12 GMT  
		Size: 2.6 MB (2633547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b6a123b9dd6f23ecf8478d53dddf1407060d2f980725386ca54df4afca2c9`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a75460f30a5e4255854c4a9f16faf02f30eee88b4615b3fba025dbc0b2852`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2bbe127552ec58191550d7af38e5e2a838fa635f56809e3e1db2dd36d4c67b84
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8545444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c083b0cc317aeae61bb347db85d1822ff0e19726d88c403267ccf53d69acc3f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:30:50 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:30:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:30:53 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 15 Jun 2021 23:31:58 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 15 Jun 2021 23:31:58 GMT
ENV NICK=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV SERVER=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV LISTEN=3333
# Tue, 15 Jun 2021 23:31:59 GMT
ENV OWNER=
# Tue, 15 Jun 2021 23:31:59 GMT
ENV USERFILE=eggdrop.user
# Tue, 15 Jun 2021 23:31:59 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 15 Jun 2021 23:32:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 15 Jun 2021 23:32:00 GMT
EXPOSE 3333
# Tue, 15 Jun 2021 23:32:00 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 15 Jun 2021 23:32:00 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 15 Jun 2021 23:32:00 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 15 Jun 2021 23:32:01 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3db2720b6273728863ce64bb67670c4aae649525cf85a5bc0834bd557c60028`  
		Last Modified: Tue, 15 Jun 2021 23:32:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960848fa3748666f162fe523f04c331adba985f24d63933d5aaf1e2a0e75c5b`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ebe6949c44b5c5569f8ee4c4dfe8132fc69db2ae59ed92a76bdcbbc5e5784`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 2.8 MB (2752462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d22cbebba2d9d664edeb72f9753d029f7909f033180536e04e09e7bccb03f5`  
		Last Modified: Tue, 15 Jun 2021 23:32:41 GMT  
		Size: 3.1 MB (3067159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e77d1989915493443764c02f12bfcecfcf3dece3248728da041a83a0c5d891`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5c799a3dc8fd10c393bea631747cb9e9888405244a3e7bdb38e294584a0e35`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
