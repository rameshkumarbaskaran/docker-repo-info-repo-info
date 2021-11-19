## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:5f9ad2ec6a71c235942439776527277761b340efc3a8b72bef35a628330d6c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:6e892a67931479b599c272a667e2938484206e52d7264ff14d7b7db016f37b30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8289929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15447097e0374d1ea165db47231adde6fb63ff6480b16f30134b7a313a3b43e9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:49:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 00:49:05 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 00:49:07 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 00:49:10 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 00:50:26 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 00:50:26 GMT
ENV NICK=
# Wed, 01 Sep 2021 00:50:27 GMT
ENV SERVER=
# Wed, 01 Sep 2021 00:50:27 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 00:50:27 GMT
ENV OWNER=
# Wed, 01 Sep 2021 00:50:27 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 00:50:27 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 00:50:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 00:50:28 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 00:50:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 00:50:28 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 00:50:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 00:50:29 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2739640d4bb626124033590fe2bf187a76c1f09fc23aa7686e7c3fab1ea81d84`  
		Last Modified: Wed, 01 Sep 2021 00:51:19 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738ab5f4a6a9c53e0f6ed425003f94b60df8ec4e166993682419cfe0a94a62f5`  
		Last Modified: Wed, 01 Sep 2021 00:51:16 GMT  
		Size: 10.1 KB (10118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0880ee1cbcc03493b50e3d163c452ce2bbb7b3de40bf0f955c9744388500b821`  
		Last Modified: Wed, 01 Sep 2021 00:51:17 GMT  
		Size: 2.7 MB (2724823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734b1d2617820fb511e667242f74784e1a91e810da7643c518373cea683dc9f5`  
		Last Modified: Wed, 01 Sep 2021 00:51:17 GMT  
		Size: 2.7 MB (2737114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2384c732a6a65e03999103c3cb481f0e361b99732133b52e23f57be3a24759`  
		Last Modified: Wed, 01 Sep 2021 00:51:16 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4ab1d804e5474fe3998c40986e14f69650bea83115a3f78da3e35a49da8219`  
		Last Modified: Wed, 01 Sep 2021 00:51:16 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:256bf1e8371ae1436bd7b27b318801ba886744ed2a1225293f5d586fac79f541
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7984703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c777347de3a39dff1a465be9c70eeda9ba5de814025ba8d418620d17956a5a7b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:40:18 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 01:40:20 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 01:40:22 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 01:40:25 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 01:42:54 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 01:42:54 GMT
ENV NICK=
# Wed, 01 Sep 2021 01:42:55 GMT
ENV SERVER=
# Wed, 01 Sep 2021 01:42:55 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 01:42:56 GMT
ENV OWNER=
# Wed, 01 Sep 2021 01:42:56 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 01:42:56 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 01:42:57 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 01:42:57 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 01:42:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 01:42:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 01:42:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 01:42:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f046c2415fb1127f8d46523c533c6d2cce3bd492e0d68c48c260d220336ca952`  
		Last Modified: Wed, 01 Sep 2021 01:43:59 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf336ff3aa2db3f62c40723c1adc70b28e83510d2314cff15dcb5e218e1c2af`  
		Last Modified: Wed, 01 Sep 2021 01:43:57 GMT  
		Size: 9.8 KB (9833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87713f793a04367c6610fc1476e6a6f31d2e474ebb4598fde28a9728dbd06ae`  
		Last Modified: Wed, 01 Sep 2021 01:43:59 GMT  
		Size: 2.7 MB (2652189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7192b1f59b63dc171f423af626fa69dc717358b1645dd0db5b1ed1fb3cbbb2bc`  
		Last Modified: Wed, 01 Sep 2021 01:43:59 GMT  
		Size: 2.7 MB (2695121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c74d83e6f19d90b93b685a87dd4c0c1b522bc2338d4fe8c56b9806a195ca45`  
		Last Modified: Wed, 01 Sep 2021 01:43:57 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402fc12bd28bda7948b0b77e3a48bd0ebb3f7d2ce610b45949fcfc92e8e478a`  
		Last Modified: Wed, 01 Sep 2021 01:43:57 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cce2af596f43a71f3de7c879b8e8cebc3fd854ef89894ee49b673988036c5147
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d52838b63670883cfec07a7586170da2288a4506bef5bf0c02fa411731b2e97`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 08:52:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 13 Nov 2021 08:52:45 GMT
RUN adduser -S eggdrop
# Sat, 13 Nov 2021 08:52:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Nov 2021 08:52:49 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 01:37:42 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 01:37:42 GMT
ENV NICK=
# Fri, 19 Nov 2021 01:37:43 GMT
ENV SERVER=
# Fri, 19 Nov 2021 01:37:44 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 01:37:45 GMT
ENV OWNER=
# Fri, 19 Nov 2021 01:37:46 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 01:37:47 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 01:37:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 01:37:52 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 01:37:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 01:37:56 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 01:37:57 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 01:37:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbc128b98804468eb07fa0b1f7b4085c18d55cce6ed2ee8f3b56142609072e2`  
		Last Modified: Fri, 19 Nov 2021 01:38:47 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74808eaa2e85c2f4828d5df25cdcc933b83b31a54fbe0a8f56b6aa7e44ddb722`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 10.5 KB (10488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317e568dff660152611634a3956770f05f9e989c2b4510e6c43999867205c556`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.8 MB (2752158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c739270eb14b17b8b35df6c081e3781bae52f8d48a5e6c70787b4cde16ae80e`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.7 MB (2731563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fcc42b9556809184e4b06fc5dd03a84ca43734db824db1b99538be54debdc6`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27268c13af41e5b69d74afc62083d6832c3dc5f7f2dd4debc9b8abd32de1040`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
