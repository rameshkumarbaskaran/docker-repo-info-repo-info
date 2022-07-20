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
