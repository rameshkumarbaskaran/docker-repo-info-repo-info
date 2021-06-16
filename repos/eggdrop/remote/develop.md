## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:1d95b8fea1753598982ea16011ae539d8626e029fbeb9efa049f070bb7296998
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
$ docker pull eggdrop@sha256:b9c68cb036eaca600104945c1c96208c9f4e86145f707b9b3818054e30c8ca33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13560476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19771f728103cf8e6508928e727c623edb6952e83ed99fc195882d7d28c7f257`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:47 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Tue, 15 Jun 2021 22:57:47 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:01:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 16 Jun 2021 11:01:41 GMT
RUN adduser -S eggdrop
# Wed, 16 Jun 2021 11:01:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 16 Jun 2021 11:01:43 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Wed, 16 Jun 2021 11:01:43 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Wed, 16 Jun 2021 11:01:45 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 16 Jun 2021 11:02:53 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 16 Jun 2021 11:02:53 GMT
ENV NICK=
# Wed, 16 Jun 2021 11:02:53 GMT
ENV SERVER=
# Wed, 16 Jun 2021 11:02:54 GMT
ENV LISTEN=3333
# Wed, 16 Jun 2021 11:02:54 GMT
ENV OWNER=
# Wed, 16 Jun 2021 11:02:54 GMT
ENV USERFILE=eggdrop.user
# Wed, 16 Jun 2021 11:02:54 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 16 Jun 2021 11:02:54 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 16 Jun 2021 11:02:55 GMT
EXPOSE 3333
# Wed, 16 Jun 2021 11:02:55 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Wed, 16 Jun 2021 11:02:55 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 16 Jun 2021 11:02:55 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 16 Jun 2021 11:02:55 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd9e94c2fc071f8031671416fd3978d5e15df32f85606293c7808302e2a1281`  
		Last Modified: Wed, 16 Jun 2021 11:04:57 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0618f856dc73d30dff3c2d4ffa5c5695e1f32cf733706780bd828e71ef8d58`  
		Last Modified: Wed, 16 Jun 2021 11:04:55 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024c911a2c2aea1c44236d3f8532674186153bb61e3acf533e805e0a878aab0`  
		Last Modified: Wed, 16 Jun 2021 11:04:56 GMT  
		Size: 2.6 MB (2608726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c393c0da043953c5ff88616e25d27a75493b1c82c1044fab95192fcf68e11383`  
		Last Modified: Wed, 16 Jun 2021 11:04:57 GMT  
		Size: 8.3 MB (8316596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc237cbdbc8e29b6309f34c6f11c4ff348088ab839d4520d681ff4ebcb17963`  
		Last Modified: Wed, 16 Jun 2021 11:04:55 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77ad91a22ff90d04c86e62022462824d2cc2b2318cd8cddcb2bf2671da027b8`  
		Last Modified: Wed, 16 Jun 2021 11:04:55 GMT  
		Size: 699.0 B  
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
