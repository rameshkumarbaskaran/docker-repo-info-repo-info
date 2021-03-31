## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:a54c296d77920b11e1b39f5baf9574613c22b8e5a2dae4db22ea4f0a62c50de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:13010b6a4f764c6e5425d27686195f872847ec5921a7db5a8bfc4b41168c852b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8223857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e1b66b36045836215599980d50ddb3fd2bb467e8c4f7d66f0d70e4d82b2168`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Mon, 29 Mar 2021 18:25:37 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 29 Mar 2021 18:25:38 GMT
RUN adduser -S eggdrop
# Mon, 29 Mar 2021 18:25:39 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 29 Mar 2021 18:25:41 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 29 Mar 2021 18:26:46 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 29 Mar 2021 18:26:46 GMT
ENV NICK=
# Mon, 29 Mar 2021 18:26:46 GMT
ENV SERVER=
# Mon, 29 Mar 2021 18:26:46 GMT
ENV LISTEN=3333
# Mon, 29 Mar 2021 18:26:46 GMT
ENV OWNER=
# Mon, 29 Mar 2021 18:26:47 GMT
ENV USERFILE=eggdrop.user
# Mon, 29 Mar 2021 18:26:47 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 29 Mar 2021 18:26:47 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 29 Mar 2021 18:26:47 GMT
EXPOSE 3333
# Mon, 29 Mar 2021 18:26:47 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 29 Mar 2021 18:26:48 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 29 Mar 2021 18:26:48 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 29 Mar 2021 18:26:48 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eb87d40a5d04bb2f3cddc6c0113a1f4a738519880cff4f1e07f650afc6dbf3`  
		Last Modified: Mon, 29 Mar 2021 18:27:30 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0b1ed597373f415721344f92df02c7699e1e113ec744bacb5ddfe5bd3173d9`  
		Last Modified: Mon, 29 Mar 2021 18:27:28 GMT  
		Size: 10.1 KB (10109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e835b8b19e774c697d1793e108cd750e6c1892afb1297e469ba25dc9d2ba12`  
		Last Modified: Mon, 29 Mar 2021 18:27:29 GMT  
		Size: 2.7 MB (2724405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f89e026f3f26d697df684d26a88f117e9883d99d06ebeba67c6e6cfafa9e19`  
		Last Modified: Mon, 29 Mar 2021 18:27:28 GMT  
		Size: 2.7 MB (2673861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da9cf0048a0a220ae0bf1a6d07c39a67c3a4c8d8799d669b4388228680e393f`  
		Last Modified: Mon, 29 Mar 2021 18:27:28 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024f150310092d715076476be109a494ac27069acdddd796376344da55c6d533`  
		Last Modified: Mon, 29 Mar 2021 18:27:28 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:aec1e8d64ab1e7287f6b9c1c7991a1562b4b794d77931d75542a5fda37471472
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc484287ff1b50155f08697db75e244702a5c27467145a8c40ca8002b485a0b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 19:29:11 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 31 Mar 2021 19:29:17 GMT
RUN adduser -S eggdrop
# Wed, 31 Mar 2021 19:29:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 31 Mar 2021 19:29:31 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 31 Mar 2021 19:32:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 31 Mar 2021 19:32:13 GMT
ENV NICK=
# Wed, 31 Mar 2021 19:32:15 GMT
ENV SERVER=
# Wed, 31 Mar 2021 19:32:15 GMT
ENV LISTEN=3333
# Wed, 31 Mar 2021 19:32:16 GMT
ENV OWNER=
# Wed, 31 Mar 2021 19:32:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 31 Mar 2021 19:32:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 31 Mar 2021 19:32:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 31 Mar 2021 19:32:19 GMT
EXPOSE 3333
# Wed, 31 Mar 2021 19:32:20 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 31 Mar 2021 19:32:21 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 31 Mar 2021 19:32:22 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 31 Mar 2021 19:32:22 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8e825d0673b1409e4dbdb8d11420d3548926c7ec06471892c81459e7e0d09c`  
		Last Modified: Wed, 31 Mar 2021 19:33:03 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0da49ceef750484d93aa4007ce4f01a1666c837942ef9d945a16c9b2632dc8e`  
		Last Modified: Wed, 31 Mar 2021 19:33:01 GMT  
		Size: 9.8 KB (9827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134921cf54ec8713f3a15bc2d9394074aa568ae849eae467885486a2d67d0667`  
		Last Modified: Wed, 31 Mar 2021 19:33:04 GMT  
		Size: 2.7 MB (2652129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3215ac4092c427e26144436537fd2a9885bc701488ce2bb8f39c335622c3f3a7`  
		Last Modified: Wed, 31 Mar 2021 19:33:04 GMT  
		Size: 2.6 MB (2633508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0fae382c9caaf85d714725025dc973e4c111a01e3073fb71e0af12ff339d87`  
		Last Modified: Wed, 31 Mar 2021 19:33:02 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8af98c83bd092d0263be90d1ffd87110f1ec9bb32f8e33a54dfeb6ae76a5ac`  
		Last Modified: Wed, 31 Mar 2021 19:33:04 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:aa869560547dc520f7327b8123c108ec394137a93befa2ec96742f6c3f4e7cec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8146606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d0f5e17e38fc11cecbc4aae1054fca1d1b46831a637640bced609cd9e10661`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Mon, 29 Mar 2021 18:41:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 29 Mar 2021 18:41:59 GMT
RUN adduser -S eggdrop
# Mon, 29 Mar 2021 18:42:04 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 29 Mar 2021 18:42:08 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 29 Mar 2021 18:44:06 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 29 Mar 2021 18:44:07 GMT
ENV NICK=
# Mon, 29 Mar 2021 18:44:08 GMT
ENV SERVER=
# Mon, 29 Mar 2021 18:44:09 GMT
ENV LISTEN=3333
# Mon, 29 Mar 2021 18:44:10 GMT
ENV OWNER=
# Mon, 29 Mar 2021 18:44:10 GMT
ENV USERFILE=eggdrop.user
# Mon, 29 Mar 2021 18:44:11 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 29 Mar 2021 18:44:12 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 29 Mar 2021 18:44:13 GMT
EXPOSE 3333
# Mon, 29 Mar 2021 18:44:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 29 Mar 2021 18:44:15 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 29 Mar 2021 18:44:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 29 Mar 2021 18:44:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7908687cab4e2e8036d3a15a7b35c59c0fb94a48df7adc80fecbf7f62b1e37f`  
		Last Modified: Mon, 29 Mar 2021 18:44:43 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed4b45bb3f885133e6216b64ea7b52fd184ceaff01b3f065710c2d4a5a75e6f`  
		Last Modified: Mon, 29 Mar 2021 18:44:42 GMT  
		Size: 10.0 KB (9994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5efde971466056a68596f83fa25c975d505e70d57c8ab24c47c16808aaeed4`  
		Last Modified: Mon, 29 Mar 2021 18:44:42 GMT  
		Size: 2.8 MB (2752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d1479a7f297db755dad66c514bc3a85053294cb58f8ae47793a7efaf496b9e`  
		Last Modified: Mon, 29 Mar 2021 18:44:42 GMT  
		Size: 2.7 MB (2668400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808a387447375f7ffae93dc4ee79e97f9fede109c952002b5b01d1b79b7abc1e`  
		Last Modified: Mon, 29 Mar 2021 18:44:41 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eeef541bea0e9378eff40154ba040f95a9ac50d2c4b7f4e2b0ced63f3e1b1c`  
		Last Modified: Mon, 29 Mar 2021 18:44:41 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
