## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:5b446f03a7d657202a528eeb3d5c82e09a3429c37ee89f8b47c9cceed9c48a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:e49f298cb2e9e2f2e802edaa9a19cc482bcf74029faa98843994fe7aa98e6a9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9767476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02576e601c28f1892b42557b2f916fcb832f175dd8b3cf2a85e582cd541c7a3b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 02:14:10 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 19 Nov 2021 02:14:11 GMT
RUN adduser -S eggdrop
# Fri, 19 Nov 2021 02:14:12 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 19 Nov 2021 02:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 16 Mar 2022 17:25:25 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 16 Mar 2022 17:25:25 GMT
ENV NICK=
# Wed, 16 Mar 2022 17:25:25 GMT
ENV SERVER=
# Wed, 16 Mar 2022 17:25:25 GMT
ENV LISTEN=3333
# Wed, 16 Mar 2022 17:25:25 GMT
ENV OWNER=
# Wed, 16 Mar 2022 17:25:25 GMT
ENV USERFILE=eggdrop.user
# Wed, 16 Mar 2022 17:25:25 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 16 Mar 2022 17:25:25 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 16 Mar 2022 17:25:25 GMT
EXPOSE 3333
# Wed, 16 Mar 2022 17:25:26 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 16 Mar 2022 17:25:26 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 16 Mar 2022 17:25:26 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 16 Mar 2022 17:25:26 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3241c16fd16e3a139d141166ed22612842968854446255731cfe12791acfc269`  
		Last Modified: Fri, 19 Nov 2021 02:16:18 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a017ba637452218499fca2a22d724cdc72571a4475255c1ab054b41b12a67`  
		Last Modified: Fri, 19 Nov 2021 02:16:15 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb699dbe31b3a2a61d0a1d77320a2b8498026a801e89a6120867ce22e17fcbfa`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 2.7 MB (2725635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e042219553e908abc1c2cbb88b2deaf6800a593a292741d76f13002fc8d42776`  
		Last Modified: Wed, 16 Mar 2022 17:25:51 GMT  
		Size: 4.2 MB (4204907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e81597d040b7cdd032802ee42ff737f6d1fd6843ba0b21631dfec2df44ef80`  
		Last Modified: Wed, 16 Mar 2022 17:25:50 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4c2f9192430888a96251b7100c3ac53911e57ab2dd596520cd88e6aa955f`  
		Last Modified: Wed, 16 Mar 2022 17:25:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:122bb0227f48ef8fe35ba5812cb8958afb24465ccfd5c7ac68be28f5a63b204d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7978193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a651c413330366ccced3e0f0ef84e38f1bbfa847251f4d46b94f11379d9dad`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:45 GMT
ADD file:85dfb53147cadaa6ec9595f75c71284523f862af4b9edb32c7f8ccebb0ef50a8 in / 
# Thu, 17 Mar 2022 14:32:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:15:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 17 Mar 2022 15:15:45 GMT
RUN adduser -S eggdrop
# Thu, 17 Mar 2022 15:15:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 17 Mar 2022 15:15:50 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 17 Mar 2022 15:18:23 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 17 Mar 2022 15:18:24 GMT
ENV NICK=
# Thu, 17 Mar 2022 15:18:24 GMT
ENV SERVER=
# Thu, 17 Mar 2022 15:18:24 GMT
ENV LISTEN=3333
# Thu, 17 Mar 2022 15:18:25 GMT
ENV OWNER=
# Thu, 17 Mar 2022 15:18:25 GMT
ENV USERFILE=eggdrop.user
# Thu, 17 Mar 2022 15:18:26 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 17 Mar 2022 15:18:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 17 Mar 2022 15:18:26 GMT
EXPOSE 3333
# Thu, 17 Mar 2022 15:18:27 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 17 Mar 2022 15:18:27 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 17 Mar 2022 15:18:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 17 Mar 2022 15:18:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:84104bbf59c688eb09fa3dfa49f67ee18a001947cd8e75d4c8d09e92926d6b31`  
		Last Modified: Thu, 17 Mar 2022 14:34:22 GMT  
		Size: 2.6 MB (2627924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd1e510cf840340b9c34cfa14cc3fc7a832572443f28af0d2c63cf30dec078`  
		Last Modified: Thu, 17 Mar 2022 15:19:16 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cb7fa74ab74933c3d0f5a43b2b2e0f5cb4332ad9e0f3d558b3bc296e438dad`  
		Last Modified: Thu, 17 Mar 2022 15:19:14 GMT  
		Size: 10.4 KB (10402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce325b134d392e303241c318e8f3927c9fff71180df7ab82013df55879374047`  
		Last Modified: Thu, 17 Mar 2022 15:19:16 GMT  
		Size: 2.7 MB (2652778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db12377e78aa28c481d5f31d50a704199e7a8ece0d814e51692670d1dfcdf210`  
		Last Modified: Thu, 17 Mar 2022 15:19:16 GMT  
		Size: 2.7 MB (2683288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0311035445d15202ed8f1d5d853071ea99fcd4919d47c93ffe8b3dd72cf901`  
		Last Modified: Thu, 17 Mar 2022 15:19:14 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df94df2aefc0ab73ed8cdc9d8e440c91a76a178bc7a7e93c2564e770d5a22bb`  
		Last Modified: Thu, 17 Mar 2022 15:19:14 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:c238c47c3943e2433b9b4b521d1216015d5382efcfd6b2f205b2b3811e578b57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8205326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3360c1069756788284a40b6b4d98d5c5524e0831045b8c9f7fc6c4390ca8c7d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:19 GMT
ADD file:0bbbf3ca52651bbef2547689474beafcef779899da63743efd8166a01d9f3f7a in / 
# Thu, 17 Mar 2022 18:43:20 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 14:45:12 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 18 Mar 2022 14:45:13 GMT
RUN adduser -S eggdrop
# Fri, 18 Mar 2022 14:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 18 Mar 2022 14:45:16 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 18 Mar 2022 14:46:52 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 18 Mar 2022 14:46:53 GMT
ENV NICK=
# Fri, 18 Mar 2022 14:46:54 GMT
ENV SERVER=
# Fri, 18 Mar 2022 14:46:55 GMT
ENV LISTEN=3333
# Fri, 18 Mar 2022 14:46:56 GMT
ENV OWNER=
# Fri, 18 Mar 2022 14:46:57 GMT
ENV USERFILE=eggdrop.user
# Fri, 18 Mar 2022 14:46:58 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 18 Mar 2022 14:46:59 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 18 Mar 2022 14:47:00 GMT
EXPOSE 3333
# Fri, 18 Mar 2022 14:47:02 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 18 Mar 2022 14:47:03 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 18 Mar 2022 14:47:03 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 18 Mar 2022 14:47:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6b5c040bf1f18956758f68628afdc8e179044ac75bcd411134da39a661a772e0`  
		Last Modified: Thu, 17 Mar 2022 18:44:11 GMT  
		Size: 2.7 MB (2719134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7d5a2ca34099ee59f1fe9cf95cdebe5333240fc3fcc85b1f87385f2009182`  
		Last Modified: Fri, 18 Mar 2022 14:47:27 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f63adfc43a1a5c75fc2ae2f1ef9a21be6ea3cd3f23e49b1f5b848538d4d65a1`  
		Last Modified: Fri, 18 Mar 2022 14:47:24 GMT  
		Size: 10.5 KB (10479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a4fe92bba72599e1e2ff73684c341d4588bde58f8ac95df4d2ca47f0edb58c`  
		Last Modified: Fri, 18 Mar 2022 14:47:25 GMT  
		Size: 2.8 MB (2752210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d7283084533cfc36469ab71ac7cbdf4d43225dc13dcdd05f00c69c6a28ebb7`  
		Last Modified: Fri, 18 Mar 2022 14:47:25 GMT  
		Size: 2.7 MB (2719723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea66aaf353f32b17778bb9aa25dc17273e21a3b37ddf4315552269025569cee`  
		Last Modified: Fri, 18 Mar 2022 14:47:24 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fba34823c5a1a78d76f8ddcd7a709dc0f6c55f23cab8203d64ea6c3a79b51d3`  
		Last Modified: Fri, 18 Mar 2022 14:47:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
