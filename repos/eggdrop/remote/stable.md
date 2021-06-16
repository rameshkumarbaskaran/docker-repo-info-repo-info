## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:2171d68b192113c99e972169bed9474a7bad6d9a7d765ccce310bbb7d8c46f6f
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
$ docker pull eggdrop@sha256:7006981f543e82459e49c13f2c60aa6c22dae0ce2b3a190293ba68f995407265
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8312907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dea417035fc8ed78c2c8db5f84bc5d81fa115172538e1f4dba0c8c74d2f2211`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:03:08 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 16 Jun 2021 11:03:09 GMT
RUN adduser -S eggdrop
# Wed, 16 Jun 2021 11:03:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 16 Jun 2021 11:03:12 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 16 Jun 2021 11:04:16 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 16 Jun 2021 11:04:17 GMT
ENV NICK=
# Wed, 16 Jun 2021 11:04:17 GMT
ENV SERVER=
# Wed, 16 Jun 2021 11:04:17 GMT
ENV LISTEN=3333
# Wed, 16 Jun 2021 11:04:17 GMT
ENV OWNER=
# Wed, 16 Jun 2021 11:04:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 16 Jun 2021 11:04:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 16 Jun 2021 11:04:18 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 16 Jun 2021 11:04:18 GMT
EXPOSE 3333
# Wed, 16 Jun 2021 11:04:18 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 16 Jun 2021 11:04:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 16 Jun 2021 11:04:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 16 Jun 2021 11:04:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045acbccf8f1556b6bc86e54a0193de50610006c93687439d76115d0960e44b2`  
		Last Modified: Wed, 16 Jun 2021 11:05:09 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe0f19423f3457fe7d51415c2e2d576aed2661a3081bd62a8071adef2a7dd90`  
		Last Modified: Wed, 16 Jun 2021 11:05:07 GMT  
		Size: 9.8 KB (9831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7159bc0d004635dbf262043b159bad8974b269103c08f7c743c188a786af2b7`  
		Last Modified: Wed, 16 Jun 2021 11:05:07 GMT  
		Size: 2.7 MB (2652138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1defc93b1feb8f06469c24a0b78cd2905139e7afb7d5b5b98120572ed66b964a`  
		Last Modified: Wed, 16 Jun 2021 11:05:07 GMT  
		Size: 3.0 MB (3025002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d850c31234748ef59780e95825f776443aa07fc3084830e2d30c68b2df58d7ab`  
		Last Modified: Wed, 16 Jun 2021 11:05:06 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8414f2047277fa00a65111207f33833d865be5533bf2eca74b7bd2e18c20b850`  
		Last Modified: Wed, 16 Jun 2021 11:05:06 GMT  
		Size: 701.0 B  
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
