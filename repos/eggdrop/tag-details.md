<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.8`](#eggdrop18)
-	[`eggdrop:1.8.4`](#eggdrop184)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.8`

```console
$ docker pull eggdrop@sha256:bf954c76a6b22bafa5a1152045e8320cec873b0adf46bfb885db6bd81d6a4ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:1.8` - linux; amd64

```console
$ docker pull eggdrop@sha256:dc3eb82740c517c499ab8a0e0e6029d31a1355132e054984cd9c9da42631d8c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8786443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52c01e299f093296afc165d5f00b03e59207ddae8c434f7496b67c1292dce6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 23 Mar 2020 22:01:52 GMT
RUN adduser -S eggdrop
# Mon, 23 Mar 2020 22:01:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 23 Mar 2020 22:03:53 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 23 Mar 2020 22:05:14 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 23 Mar 2020 22:05:15 GMT
ENV NICK=
# Mon, 23 Mar 2020 22:05:15 GMT
ENV SERVER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV LISTEN=3333
# Mon, 23 Mar 2020 22:05:16 GMT
ENV OWNER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV USERFILE=eggdrop.user
# Mon, 23 Mar 2020 22:05:17 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 23 Mar 2020 22:05:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 23 Mar 2020 22:05:18 GMT
EXPOSE 3333
# Mon, 23 Mar 2020 22:05:18 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Mon, 23 Mar 2020 22:05:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 23 Mar 2020 22:05:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de90ac254f3b2092e08d0d1a27fade104236143c7429ad4bfd7a17858c302031`  
		Last Modified: Mon, 23 Mar 2020 22:05:43 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7989bd96822c15f6ae1d0789c29950de5717ef922d3f3f8e284011e9e169c4`  
		Last Modified: Mon, 23 Mar 2020 22:05:41 GMT  
		Size: 9.6 KB (9581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7689126dd51138dc04d8f316f2219b9bb5588d4f9a6b7fb9d19fe9917cfa76e`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 2.7 MB (2684248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c63278b54642d69450022162c6395d8b02367c5b0cc0745d295e8e4165b196c`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 3.3 MB (3285542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef178bab7af5fea90f56fd61a8ee49c76fb93729d8d4deb48bf776213dc02c1e`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb097a7c2750f9c97142d213394ada805c5e33cba328e781699e8303c560664`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.8.4`

```console
$ docker pull eggdrop@sha256:bf954c76a6b22bafa5a1152045e8320cec873b0adf46bfb885db6bd81d6a4ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:1.8.4` - linux; amd64

```console
$ docker pull eggdrop@sha256:dc3eb82740c517c499ab8a0e0e6029d31a1355132e054984cd9c9da42631d8c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8786443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52c01e299f093296afc165d5f00b03e59207ddae8c434f7496b67c1292dce6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 23 Mar 2020 22:01:52 GMT
RUN adduser -S eggdrop
# Mon, 23 Mar 2020 22:01:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 23 Mar 2020 22:03:53 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 23 Mar 2020 22:05:14 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 23 Mar 2020 22:05:15 GMT
ENV NICK=
# Mon, 23 Mar 2020 22:05:15 GMT
ENV SERVER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV LISTEN=3333
# Mon, 23 Mar 2020 22:05:16 GMT
ENV OWNER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV USERFILE=eggdrop.user
# Mon, 23 Mar 2020 22:05:17 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 23 Mar 2020 22:05:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 23 Mar 2020 22:05:18 GMT
EXPOSE 3333
# Mon, 23 Mar 2020 22:05:18 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Mon, 23 Mar 2020 22:05:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 23 Mar 2020 22:05:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de90ac254f3b2092e08d0d1a27fade104236143c7429ad4bfd7a17858c302031`  
		Last Modified: Mon, 23 Mar 2020 22:05:43 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7989bd96822c15f6ae1d0789c29950de5717ef922d3f3f8e284011e9e169c4`  
		Last Modified: Mon, 23 Mar 2020 22:05:41 GMT  
		Size: 9.6 KB (9581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7689126dd51138dc04d8f316f2219b9bb5588d4f9a6b7fb9d19fe9917cfa76e`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 2.7 MB (2684248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c63278b54642d69450022162c6395d8b02367c5b0cc0745d295e8e4165b196c`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 3.3 MB (3285542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef178bab7af5fea90f56fd61a8ee49c76fb93729d8d4deb48bf776213dc02c1e`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb097a7c2750f9c97142d213394ada805c5e33cba328e781699e8303c560664`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:c664b3158ea877b9ad52d593f26575d6660fb5d460a136d7fe1e40356e4c3467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:7fc7146740ac23e356324f06c9d6002e06de60bf22cc4224a1d473b1e382faf5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13161878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a4ededa2642b05e7e4f04aefbab25030c5a3d703400cbfb15e11ea0ef12f9f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 23 Mar 2020 22:01:52 GMT
RUN adduser -S eggdrop
# Mon, 23 Mar 2020 22:01:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 23 Mar 2020 22:01:55 GMT
ENV EGGDROP_SHA256=12f560ad31e27f1ad631964f6d4ca43e97de6b11c35d4b733a44d21216d83bb4
# Mon, 23 Mar 2020 22:01:55 GMT
ENV EGGDROP_COMMIT=7a490c534fd53af99cbf33a85d907785e9156629
# Mon, 23 Mar 2020 22:01:58 GMT
RUN apk --update add --no-cache tcl bash openssl
# Mon, 23 Mar 2020 22:03:40 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 23 Mar 2020 22:03:41 GMT
ENV NICK=
# Mon, 23 Mar 2020 22:03:41 GMT
ENV SERVER=
# Mon, 23 Mar 2020 22:03:41 GMT
ENV LISTEN=3333
# Mon, 23 Mar 2020 22:03:42 GMT
ENV OWNER=
# Mon, 23 Mar 2020 22:03:42 GMT
ENV USERFILE=eggdrop.user
# Mon, 23 Mar 2020 22:03:42 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 23 Mar 2020 22:03:43 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 23 Mar 2020 22:03:43 GMT
EXPOSE 3333
# Mon, 23 Mar 2020 22:03:44 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Mon, 23 Mar 2020 22:03:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 23 Mar 2020 22:03:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 23 Mar 2020 22:03:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de90ac254f3b2092e08d0d1a27fade104236143c7429ad4bfd7a17858c302031`  
		Last Modified: Mon, 23 Mar 2020 22:05:43 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7989bd96822c15f6ae1d0789c29950de5717ef922d3f3f8e284011e9e169c4`  
		Last Modified: Mon, 23 Mar 2020 22:05:41 GMT  
		Size: 9.6 KB (9581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c6f695262d96126f5d8ace179315acdee7e373a1758730524daad3dc571e81`  
		Last Modified: Mon, 23 Mar 2020 22:05:42 GMT  
		Size: 2.7 MB (2684257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660b0b8f894961a00dd343f973f8e3e029cf6cf07e6008a1ab3b99939369b623`  
		Last Modified: Mon, 23 Mar 2020 22:05:43 GMT  
		Size: 7.7 MB (7660959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaeb4a05350a979e38a4258d792a75fbf628d49449be1c3786a6839c4a647f91`  
		Last Modified: Mon, 23 Mar 2020 22:05:41 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbdfc077c3e48e443051bfe7f83a6d15187d16766b62278f09cdb63b71a8dac`  
		Last Modified: Mon, 23 Mar 2020 22:05:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:a8ca4e529cd12273b739fd66fe223154f5b4b9479425707abba4a8e5140236b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12842436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb859028b4c8757c32f6e959c94a388c3f47b8bca7eb08062d0041de0591cac`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:00:09 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 23 Mar 2020 23:00:11 GMT
RUN adduser -S eggdrop
# Mon, 23 Mar 2020 23:00:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 23 Mar 2020 23:00:15 GMT
ENV EGGDROP_SHA256=12f560ad31e27f1ad631964f6d4ca43e97de6b11c35d4b733a44d21216d83bb4
# Mon, 23 Mar 2020 23:00:17 GMT
ENV EGGDROP_COMMIT=7a490c534fd53af99cbf33a85d907785e9156629
# Mon, 23 Mar 2020 23:00:22 GMT
RUN apk --update add --no-cache tcl bash openssl
# Mon, 23 Mar 2020 23:02:16 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 23 Mar 2020 23:02:17 GMT
ENV NICK=
# Mon, 23 Mar 2020 23:02:18 GMT
ENV SERVER=
# Mon, 23 Mar 2020 23:02:18 GMT
ENV LISTEN=3333
# Mon, 23 Mar 2020 23:02:19 GMT
ENV OWNER=
# Mon, 23 Mar 2020 23:02:19 GMT
ENV USERFILE=eggdrop.user
# Mon, 23 Mar 2020 23:02:20 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 23 Mar 2020 23:02:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 23 Mar 2020 23:02:21 GMT
EXPOSE 3333
# Mon, 23 Mar 2020 23:02:22 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Mon, 23 Mar 2020 23:02:22 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 23 Mar 2020 23:02:23 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 23 Mar 2020 23:02:24 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1106d08950ae0dc54430d634a5f91e273a802f297b14564d84145faa304711a1`  
		Last Modified: Mon, 23 Mar 2020 23:02:45 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4fdb42becd6ce7dcfd0115a182367882945cd2e4c53d2cacab0a1310aea597`  
		Last Modified: Mon, 23 Mar 2020 23:02:43 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0399b8cd3af5be7f1bfd26f0e206f3eb2599161b48415a17f4d3718e3c6ee81e`  
		Last Modified: Mon, 23 Mar 2020 23:02:43 GMT  
		Size: 2.6 MB (2608551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577372496e8ba28a79dc43b6f13cd637f9515bbebeea69e875da5964a9daef68`  
		Last Modified: Mon, 23 Mar 2020 23:02:44 GMT  
		Size: 7.6 MB (7602076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988dff542446736ff4e66308f12bf91effff584e72f76309e0875f7230fbe9a0`  
		Last Modified: Mon, 23 Mar 2020 23:02:43 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4dbb60523e80a8d7d675f80fd16da54771debdc016d14b7a73171e875e7071`  
		Last Modified: Mon, 23 Mar 2020 23:02:43 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:a7303960fe0cbc56bad1453aeede82f0eb45d110346f51fcc0bcac0383ced13f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13141692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3713e34c0e691a1f9d079aa4e12d1f1c8fd3ba6454881205cb40219abd179e2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:21:10 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 23 Mar 2020 23:21:12 GMT
RUN adduser -S eggdrop
# Mon, 23 Mar 2020 23:21:14 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 23 Mar 2020 23:21:15 GMT
ENV EGGDROP_SHA256=12f560ad31e27f1ad631964f6d4ca43e97de6b11c35d4b733a44d21216d83bb4
# Mon, 23 Mar 2020 23:21:15 GMT
ENV EGGDROP_COMMIT=7a490c534fd53af99cbf33a85d907785e9156629
# Mon, 23 Mar 2020 23:21:18 GMT
RUN apk --update add --no-cache tcl bash openssl
# Mon, 23 Mar 2020 23:23:11 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 23 Mar 2020 23:23:12 GMT
ENV NICK=
# Mon, 23 Mar 2020 23:23:13 GMT
ENV SERVER=
# Mon, 23 Mar 2020 23:23:15 GMT
ENV LISTEN=3333
# Mon, 23 Mar 2020 23:23:16 GMT
ENV OWNER=
# Mon, 23 Mar 2020 23:23:17 GMT
ENV USERFILE=eggdrop.user
# Mon, 23 Mar 2020 23:23:18 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 23 Mar 2020 23:23:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 23 Mar 2020 23:23:21 GMT
EXPOSE 3333
# Mon, 23 Mar 2020 23:23:22 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Mon, 23 Mar 2020 23:23:23 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 23 Mar 2020 23:23:24 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 23 Mar 2020 23:23:26 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b63c1a6e13b1a71398150ac595bcf7f9da6e35406fb414527335ac85fa4a5b`  
		Last Modified: Mon, 23 Mar 2020 23:23:47 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585c313e804e3c02c867edec0ce1532cc51d93d8e0cd199e5e872ffdc3299b14`  
		Last Modified: Mon, 23 Mar 2020 23:23:46 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c895227bac8b1f2f8bf3356f31965f1c810cbb69e6068ec3b7b29d395051b59`  
		Last Modified: Mon, 23 Mar 2020 23:23:46 GMT  
		Size: 2.7 MB (2722233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a5225693f9d1dfb74d4c6dbf7473413861f2ce45081fb5b92ca9ff8a0dca1`  
		Last Modified: Mon, 23 Mar 2020 23:23:47 GMT  
		Size: 7.7 MB (7682965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f90977b178413a0ea4f9490ad81aba20c3e84537be9ae22e6940ea0d9eef07`  
		Last Modified: Mon, 23 Mar 2020 23:23:45 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df0e30f597c3c6f85ba179f950cbc78c89fb0fbc5267564132b4d3769c4fa22`  
		Last Modified: Mon, 23 Mar 2020 23:23:46 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:bf954c76a6b22bafa5a1152045e8320cec873b0adf46bfb885db6bd81d6a4ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:dc3eb82740c517c499ab8a0e0e6029d31a1355132e054984cd9c9da42631d8c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8786443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52c01e299f093296afc165d5f00b03e59207ddae8c434f7496b67c1292dce6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 23 Mar 2020 22:01:52 GMT
RUN adduser -S eggdrop
# Mon, 23 Mar 2020 22:01:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 23 Mar 2020 22:03:53 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 23 Mar 2020 22:05:14 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 23 Mar 2020 22:05:15 GMT
ENV NICK=
# Mon, 23 Mar 2020 22:05:15 GMT
ENV SERVER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV LISTEN=3333
# Mon, 23 Mar 2020 22:05:16 GMT
ENV OWNER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV USERFILE=eggdrop.user
# Mon, 23 Mar 2020 22:05:17 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 23 Mar 2020 22:05:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 23 Mar 2020 22:05:18 GMT
EXPOSE 3333
# Mon, 23 Mar 2020 22:05:18 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Mon, 23 Mar 2020 22:05:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 23 Mar 2020 22:05:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de90ac254f3b2092e08d0d1a27fade104236143c7429ad4bfd7a17858c302031`  
		Last Modified: Mon, 23 Mar 2020 22:05:43 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7989bd96822c15f6ae1d0789c29950de5717ef922d3f3f8e284011e9e169c4`  
		Last Modified: Mon, 23 Mar 2020 22:05:41 GMT  
		Size: 9.6 KB (9581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7689126dd51138dc04d8f316f2219b9bb5588d4f9a6b7fb9d19fe9917cfa76e`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 2.7 MB (2684248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c63278b54642d69450022162c6395d8b02367c5b0cc0745d295e8e4165b196c`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 3.3 MB (3285542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef178bab7af5fea90f56fd61a8ee49c76fb93729d8d4deb48bf776213dc02c1e`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb097a7c2750f9c97142d213394ada805c5e33cba328e781699e8303c560664`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:bf954c76a6b22bafa5a1152045e8320cec873b0adf46bfb885db6bd81d6a4ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:dc3eb82740c517c499ab8a0e0e6029d31a1355132e054984cd9c9da42631d8c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8786443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52c01e299f093296afc165d5f00b03e59207ddae8c434f7496b67c1292dce6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 23 Mar 2020 22:01:52 GMT
RUN adduser -S eggdrop
# Mon, 23 Mar 2020 22:01:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 23 Mar 2020 22:03:53 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 23 Mar 2020 22:05:14 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 23 Mar 2020 22:05:15 GMT
ENV NICK=
# Mon, 23 Mar 2020 22:05:15 GMT
ENV SERVER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV LISTEN=3333
# Mon, 23 Mar 2020 22:05:16 GMT
ENV OWNER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV USERFILE=eggdrop.user
# Mon, 23 Mar 2020 22:05:17 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 23 Mar 2020 22:05:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 23 Mar 2020 22:05:18 GMT
EXPOSE 3333
# Mon, 23 Mar 2020 22:05:18 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Mon, 23 Mar 2020 22:05:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 23 Mar 2020 22:05:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de90ac254f3b2092e08d0d1a27fade104236143c7429ad4bfd7a17858c302031`  
		Last Modified: Mon, 23 Mar 2020 22:05:43 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7989bd96822c15f6ae1d0789c29950de5717ef922d3f3f8e284011e9e169c4`  
		Last Modified: Mon, 23 Mar 2020 22:05:41 GMT  
		Size: 9.6 KB (9581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7689126dd51138dc04d8f316f2219b9bb5588d4f9a6b7fb9d19fe9917cfa76e`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 2.7 MB (2684248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c63278b54642d69450022162c6395d8b02367c5b0cc0745d295e8e4165b196c`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 3.3 MB (3285542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef178bab7af5fea90f56fd61a8ee49c76fb93729d8d4deb48bf776213dc02c1e`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb097a7c2750f9c97142d213394ada805c5e33cba328e781699e8303c560664`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
