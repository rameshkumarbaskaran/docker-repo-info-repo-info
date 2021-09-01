## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:5cc3fa7b2537f9546c73c9f145e5eecc676e5c70878c2238334e7c278f06395c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:ac313d620f14ba79aaf04ea37893c884eecda0ab74bc1c8504392949f06e265e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13971057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c678c6c2ef4c384635313ea7010639ae5bcd84ff82a4c0232e4d03872319f2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:45:26 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 00:45:27 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 00:45:29 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 00:45:29 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Wed, 01 Sep 2021 00:45:30 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Wed, 01 Sep 2021 00:45:32 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 00:47:07 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 00:47:07 GMT
ENV NICK=
# Wed, 01 Sep 2021 00:47:08 GMT
ENV SERVER=
# Wed, 01 Sep 2021 00:47:08 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 00:47:08 GMT
ENV OWNER=
# Wed, 01 Sep 2021 00:47:09 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 00:47:09 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 00:47:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 00:47:09 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 00:47:10 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 00:47:10 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 00:47:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 00:47:11 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f20f9fdd96b050b7674a3c80fab08aa90a03ade7cdb1605902daa948fda52a2`  
		Last Modified: Wed, 01 Sep 2021 00:50:59 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd70c5c8eea46f41315a10333d6c4180d7330668d5d9a03a677e69f00dc72e`  
		Last Modified: Wed, 01 Sep 2021 00:50:56 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06195f163e0e173103bdbd7895dad3e16cd83d0bea4b387e8ba0a279675c6c7f`  
		Last Modified: Wed, 01 Sep 2021 00:50:57 GMT  
		Size: 2.7 MB (2685319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b39ea5b87e596e6b07a2ad6917fe4dc53c15e522b7284f084d1594f143d80e`  
		Last Modified: Wed, 01 Sep 2021 00:50:58 GMT  
		Size: 8.5 MB (8454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c5a2dde7490e58c609dc03eec26f76472c035e792e785fabde507ec82220f3`  
		Last Modified: Wed, 01 Sep 2021 00:50:56 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe69b5152010e5eee368deff14a0392844761ff7f0dde5eb3d4004a7fb1c2c0`  
		Last Modified: Wed, 01 Sep 2021 00:50:56 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:80d8796e48b3d3949de691838f905fcb69e73b391334049e68d0f0b3796ddff5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13628662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf786dc53d037fdd74a82d889b18bb506c5930153260e490c66497d4efdc424`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:57 GMT
ADD file:3e83d6b5df3a951968e475c7326baf5ef90a22f04163693db34f3b4fc5812434 in / 
# Tue, 31 Aug 2021 22:30:57 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:37:30 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 01:37:32 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 01:37:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 01:37:34 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Wed, 01 Sep 2021 01:37:35 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Wed, 01 Sep 2021 01:37:38 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 01:39:57 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 01:39:57 GMT
ENV NICK=
# Wed, 01 Sep 2021 01:39:58 GMT
ENV SERVER=
# Wed, 01 Sep 2021 01:39:58 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 01:39:58 GMT
ENV OWNER=
# Wed, 01 Sep 2021 01:39:59 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 01:39:59 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 01:40:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 01:40:00 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 01:40:01 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 01:40:01 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 01:40:02 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 01:40:02 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:7fe987b00bcb1f14c5b65f89813475143c021e2f5c156705ac3525abe1b397a1`  
		Last Modified: Tue, 31 Aug 2021 22:32:38 GMT  
		Size: 2.6 MB (2623044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6dd069ebad3ad600a5cca2d74c3ad787846847f6632100ebec5c84edd0f2ef`  
		Last Modified: Wed, 01 Sep 2021 01:43:46 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41231715f4355826a61f9bd9185a0aea868443b6ad7204af06dd8d51a0862274`  
		Last Modified: Wed, 01 Sep 2021 01:43:43 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e663e4511cb4deee82fdc4628d95ac09cdb02f325c1aae273d2640de7e0e6f2`  
		Last Modified: Wed, 01 Sep 2021 01:43:46 GMT  
		Size: 2.6 MB (2608714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d64f077b97874c7ea3af332b7ca1ccdce3972fe69f0742049a2b9ecfbdf2728`  
		Last Modified: Wed, 01 Sep 2021 01:43:49 GMT  
		Size: 8.4 MB (8383658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae48121573bcf358e0189bd7e6fcdebedbe09d8f3526866509e52e047603c5b0`  
		Last Modified: Wed, 01 Sep 2021 01:43:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fe2b0c418f3c99112e873b436447c754f54ee32091888b467586f070eb8cb9`  
		Last Modified: Wed, 01 Sep 2021 01:43:44 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:e505c5f85c44687ef35b02910322074b8c65d61a82f04aeae22ebfc9b3e1f01e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13934190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68182d0dd58f674d6ac3c36dcf19e644a13c6cb64f62d1c5e3fc310dc44cf840`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:59 GMT
ADD file:da6c0ac7cb9f819998546d88fb489b746004eb2ad6da64a39210696ef0e66e54 in / 
# Wed, 01 Sep 2021 02:50:59 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 15:14:23 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 15:14:24 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 15:14:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 15:14:25 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Wed, 01 Sep 2021 15:14:25 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Wed, 01 Sep 2021 15:14:27 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 15:15:27 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 15:15:27 GMT
ENV NICK=
# Wed, 01 Sep 2021 15:15:27 GMT
ENV SERVER=
# Wed, 01 Sep 2021 15:15:27 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 15:15:28 GMT
ENV OWNER=
# Wed, 01 Sep 2021 15:15:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 15:15:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 15:15:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 15:15:28 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 15:15:29 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 15:15:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 15:15:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 15:15:29 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:07d756952c5cd45726cf9e8a292a3e05ca67eee5da176df7d632be8c5bb0ad04`  
		Last Modified: Wed, 01 Sep 2021 02:52:00 GMT  
		Size: 2.7 MB (2728407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77992e9a0ea5be6e3c6bbfa4fa595266bfdf5c5cef3e6840258c42dc9bdd24a8`  
		Last Modified: Wed, 01 Sep 2021 15:17:20 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7ddce6f5c878efe0df3e540ebeaf6a5a4765fff701d369356f318e54f6195`  
		Last Modified: Wed, 01 Sep 2021 15:17:18 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a45924b16715996a6631dfe560eba72540f8931745dbd27a8369c07da408c`  
		Last Modified: Wed, 01 Sep 2021 15:17:18 GMT  
		Size: 2.7 MB (2722569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751cd66fcc38103b489118ba1351d649d3b6df2f725220e230124f9863c2609b`  
		Last Modified: Wed, 01 Sep 2021 15:17:19 GMT  
		Size: 8.5 MB (8469835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3348c9013c05531db307f682233367518ce245cb2856edf89ba2ff0abcdb9ad2`  
		Last Modified: Wed, 01 Sep 2021 15:17:17 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6d655d3c74b3761cd764d92a63f137fcfa4d4fa388acc830322f434d4abe3`  
		Last Modified: Wed, 01 Sep 2021 15:17:18 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
