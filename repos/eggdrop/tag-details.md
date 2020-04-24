<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.8`](#eggdrop18)
-	[`eggdrop:1.8.4`](#eggdrop184)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.8`

```console
$ docker pull eggdrop@sha256:8185e8efd2afb5ae74f15257a1ab17b0750fcd888c77592e7da7365fa36aa8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:1.8` - linux; amd64

```console
$ docker pull eggdrop@sha256:164a2020bbfdcebc48b736220f286b6d6cc867935869287e4f05afe928690cd1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8797283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474a16bc962201f303d7bc6d26bce9ddbb4ee2ee498e2cfbe88798b422deee8b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:21:14 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 24 Apr 2020 14:21:15 GMT
RUN adduser -S eggdrop
# Fri, 24 Apr 2020 14:21:16 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 24 Apr 2020 14:22:32 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 24 Apr 2020 14:23:22 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 24 Apr 2020 14:23:23 GMT
ENV NICK=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV SERVER=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV LISTEN=3333
# Fri, 24 Apr 2020 14:23:23 GMT
ENV OWNER=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV USERFILE=eggdrop.user
# Fri, 24 Apr 2020 14:23:23 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 24 Apr 2020 14:23:24 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 24 Apr 2020 14:23:24 GMT
EXPOSE 3333
# Fri, 24 Apr 2020 14:23:24 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Fri, 24 Apr 2020 14:23:24 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 24 Apr 2020 14:23:24 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 24 Apr 2020 14:23:25 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0cdf0ff845235e19454000f632a4d9bf6d978c7948da54b51bf3962d766f4c`  
		Last Modified: Fri, 24 Apr 2020 14:23:40 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05e553ff44d8d1344fff59fed8897d80984977807b655be3d15128815d5bcf0`  
		Last Modified: Fri, 24 Apr 2020 14:23:38 GMT  
		Size: 9.6 KB (9573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2ea2690f263ee9e3bbad72e3d426631672412762a5dbb0a9c3de374a77d17e`  
		Last Modified: Fri, 24 Apr 2020 14:23:44 GMT  
		Size: 2.7 MB (2684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d60d22e2e991596f29d84aef5ad465a365c8aea921b7f9f540b9e496259452d`  
		Last Modified: Fri, 24 Apr 2020 14:23:44 GMT  
		Size: 3.3 MB (3285724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ea18db1513b38e9605e34eb798b83fad2a20707470b30e4381e2eec2ec6db`  
		Last Modified: Fri, 24 Apr 2020 14:23:43 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b873e8173e8be5007fc16ef578eba2b973b90b418159527089ad5b4958e0502`  
		Last Modified: Fri, 24 Apr 2020 14:23:43 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.8.4`

```console
$ docker pull eggdrop@sha256:8185e8efd2afb5ae74f15257a1ab17b0750fcd888c77592e7da7365fa36aa8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:1.8.4` - linux; amd64

```console
$ docker pull eggdrop@sha256:164a2020bbfdcebc48b736220f286b6d6cc867935869287e4f05afe928690cd1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8797283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474a16bc962201f303d7bc6d26bce9ddbb4ee2ee498e2cfbe88798b422deee8b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:21:14 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 24 Apr 2020 14:21:15 GMT
RUN adduser -S eggdrop
# Fri, 24 Apr 2020 14:21:16 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 24 Apr 2020 14:22:32 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 24 Apr 2020 14:23:22 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 24 Apr 2020 14:23:23 GMT
ENV NICK=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV SERVER=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV LISTEN=3333
# Fri, 24 Apr 2020 14:23:23 GMT
ENV OWNER=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV USERFILE=eggdrop.user
# Fri, 24 Apr 2020 14:23:23 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 24 Apr 2020 14:23:24 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 24 Apr 2020 14:23:24 GMT
EXPOSE 3333
# Fri, 24 Apr 2020 14:23:24 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Fri, 24 Apr 2020 14:23:24 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 24 Apr 2020 14:23:24 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 24 Apr 2020 14:23:25 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0cdf0ff845235e19454000f632a4d9bf6d978c7948da54b51bf3962d766f4c`  
		Last Modified: Fri, 24 Apr 2020 14:23:40 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05e553ff44d8d1344fff59fed8897d80984977807b655be3d15128815d5bcf0`  
		Last Modified: Fri, 24 Apr 2020 14:23:38 GMT  
		Size: 9.6 KB (9573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2ea2690f263ee9e3bbad72e3d426631672412762a5dbb0a9c3de374a77d17e`  
		Last Modified: Fri, 24 Apr 2020 14:23:44 GMT  
		Size: 2.7 MB (2684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d60d22e2e991596f29d84aef5ad465a365c8aea921b7f9f540b9e496259452d`  
		Last Modified: Fri, 24 Apr 2020 14:23:44 GMT  
		Size: 3.3 MB (3285724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ea18db1513b38e9605e34eb798b83fad2a20707470b30e4381e2eec2ec6db`  
		Last Modified: Fri, 24 Apr 2020 14:23:43 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b873e8173e8be5007fc16ef578eba2b973b90b418159527089ad5b4958e0502`  
		Last Modified: Fri, 24 Apr 2020 14:23:43 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:a7fe994fcd72db58fc8b54c858dc86016123c17f62d575a7f8f97b72ed843b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:4c1c6fbee47b97be296e81420020210677aecab975fd4598643b1b73c2ce925b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13173351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636d3c943c1330caad94d9edba187b5e3f7873d77290846f3ec59f6c2e75b794`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:21:14 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 24 Apr 2020 14:21:15 GMT
RUN adduser -S eggdrop
# Fri, 24 Apr 2020 14:21:16 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 24 Apr 2020 14:21:16 GMT
ENV EGGDROP_SHA256=12f560ad31e27f1ad631964f6d4ca43e97de6b11c35d4b733a44d21216d83bb4
# Fri, 24 Apr 2020 14:21:16 GMT
ENV EGGDROP_COMMIT=7a490c534fd53af99cbf33a85d907785e9156629
# Fri, 24 Apr 2020 14:21:18 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 24 Apr 2020 14:22:15 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 24 Apr 2020 14:22:15 GMT
ENV NICK=
# Fri, 24 Apr 2020 14:22:15 GMT
ENV SERVER=
# Fri, 24 Apr 2020 14:22:15 GMT
ENV LISTEN=3333
# Fri, 24 Apr 2020 14:22:15 GMT
ENV OWNER=
# Fri, 24 Apr 2020 14:22:15 GMT
ENV USERFILE=eggdrop.user
# Fri, 24 Apr 2020 14:22:16 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 24 Apr 2020 14:22:16 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 24 Apr 2020 14:22:16 GMT
EXPOSE 3333
# Fri, 24 Apr 2020 14:22:16 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Fri, 24 Apr 2020 14:22:16 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 24 Apr 2020 14:22:17 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 24 Apr 2020 14:22:17 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0cdf0ff845235e19454000f632a4d9bf6d978c7948da54b51bf3962d766f4c`  
		Last Modified: Fri, 24 Apr 2020 14:23:40 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05e553ff44d8d1344fff59fed8897d80984977807b655be3d15128815d5bcf0`  
		Last Modified: Fri, 24 Apr 2020 14:23:38 GMT  
		Size: 9.6 KB (9573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85560cef49ffd473105321ca906412af7324d5f8524efc8876d16021669b5017`  
		Last Modified: Fri, 24 Apr 2020 14:23:39 GMT  
		Size: 2.7 MB (2684832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de777f70fce826540793fc917ccb3bf888e1ff24bd901f77768a07fde84c4bde`  
		Last Modified: Fri, 24 Apr 2020 14:23:40 GMT  
		Size: 7.7 MB (7661812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06401b363336b9fe4503328d7f8d8eecc680421f9d8444a3058761496e4fd98`  
		Last Modified: Fri, 24 Apr 2020 14:23:39 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1c6ac3049d2bce1dd29ecc03e6fc78278ca705a6a20f915f56d015218ef586`  
		Last Modified: Fri, 24 Apr 2020 14:23:38 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:66b70820b405a82c2be740969af6e10e6acda0dcd663f53d38189df4fdbba93c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12845127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb459cffc9df6a6ffa5858548420eccbb14b254d2b8bc988e69d57244d7d0796`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:36:48 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 23 Apr 2020 17:36:52 GMT
RUN adduser -S eggdrop
# Thu, 23 Apr 2020 17:36:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 23 Apr 2020 17:36:55 GMT
ENV EGGDROP_SHA256=12f560ad31e27f1ad631964f6d4ca43e97de6b11c35d4b733a44d21216d83bb4
# Thu, 23 Apr 2020 17:36:56 GMT
ENV EGGDROP_COMMIT=7a490c534fd53af99cbf33a85d907785e9156629
# Thu, 23 Apr 2020 17:37:03 GMT
RUN apk --update add --no-cache tcl bash openssl
# Thu, 23 Apr 2020 17:39:04 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 23 Apr 2020 17:39:05 GMT
ENV NICK=
# Thu, 23 Apr 2020 17:39:06 GMT
ENV SERVER=
# Thu, 23 Apr 2020 17:39:07 GMT
ENV LISTEN=3333
# Thu, 23 Apr 2020 17:39:08 GMT
ENV OWNER=
# Thu, 23 Apr 2020 17:39:08 GMT
ENV USERFILE=eggdrop.user
# Thu, 23 Apr 2020 17:39:09 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 23 Apr 2020 17:39:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 23 Apr 2020 17:39:10 GMT
EXPOSE 3333
# Thu, 23 Apr 2020 17:39:11 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Thu, 23 Apr 2020 17:39:12 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 23 Apr 2020 17:39:12 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 23 Apr 2020 17:39:13 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f412a5980f526ade995939566f7c342b9adb4c13754922fed8d1798066f9eed`  
		Last Modified: Thu, 23 Apr 2020 17:39:27 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f404049eca1aec0b894cf78c6e968dd2065753284309b55be17f3291c31ad065`  
		Last Modified: Thu, 23 Apr 2020 17:39:24 GMT  
		Size: 9.4 KB (9390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59742158857b1dd535ac41399f7d4394181e53384e9d232920dbd3ea76141c65`  
		Last Modified: Thu, 23 Apr 2020 17:39:25 GMT  
		Size: 2.6 MB (2608162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b568885b56ef30dc69ec15ad3d84230b828a17b49595a616e12d97f400426`  
		Last Modified: Thu, 23 Apr 2020 17:39:26 GMT  
		Size: 7.6 MB (7603793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0bec210903ad7e7f55610ab22068f322a6c530668ca880b62d975730bbb974`  
		Last Modified: Thu, 23 Apr 2020 17:39:24 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7c734405bebe7061ba5895931c94d0119a538922bfbcc62024ee7abbf21d18`  
		Last Modified: Thu, 23 Apr 2020 17:39:25 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:19a062e171c430e18c2a7da18883cf282d3e108eae061846151d45a97cfd3dd3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13146560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8ac75e27f10a19f9bff9cb474c66e5a4805b942e266343c5788130edef9a42`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:28 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 24 Apr 2020 09:02:31 GMT
RUN adduser -S eggdrop
# Fri, 24 Apr 2020 09:02:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 24 Apr 2020 09:02:35 GMT
ENV EGGDROP_SHA256=12f560ad31e27f1ad631964f6d4ca43e97de6b11c35d4b733a44d21216d83bb4
# Fri, 24 Apr 2020 09:02:35 GMT
ENV EGGDROP_COMMIT=7a490c534fd53af99cbf33a85d907785e9156629
# Fri, 24 Apr 2020 09:02:38 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 24 Apr 2020 09:04:30 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 24 Apr 2020 09:04:31 GMT
ENV NICK=
# Fri, 24 Apr 2020 09:04:32 GMT
ENV SERVER=
# Fri, 24 Apr 2020 09:04:32 GMT
ENV LISTEN=3333
# Fri, 24 Apr 2020 09:04:33 GMT
ENV OWNER=
# Fri, 24 Apr 2020 09:04:33 GMT
ENV USERFILE=eggdrop.user
# Fri, 24 Apr 2020 09:04:34 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 24 Apr 2020 09:04:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 24 Apr 2020 09:04:36 GMT
EXPOSE 3333
# Fri, 24 Apr 2020 09:04:37 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Fri, 24 Apr 2020 09:04:38 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 24 Apr 2020 09:04:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 24 Apr 2020 09:04:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a8db5818fe5b735a8e3706dd1ae7043eb3b468306058c8c416fb4770df991`  
		Last Modified: Fri, 24 Apr 2020 09:04:52 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdba78ca0222af81b132121091d817259b1a4e7a7e98379b4dcaec6e64d10a2c`  
		Last Modified: Fri, 24 Apr 2020 09:04:50 GMT  
		Size: 9.5 KB (9514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d804560281d0dbf23c7bd23fa98458db91bbb6c693869808003103582b786277`  
		Last Modified: Fri, 24 Apr 2020 09:04:50 GMT  
		Size: 2.7 MB (2724583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0d48b96a09a7cc968ef409bcf0fe7df290dacce554c7adeca8970a6fb2d11e`  
		Last Modified: Fri, 24 Apr 2020 09:04:52 GMT  
		Size: 7.7 MB (7684186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ea6bfe9c0fbe7c00d411793600eb08805f9f1d89cb82641264cfaded8e6019`  
		Last Modified: Fri, 24 Apr 2020 09:04:50 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d84b56e50f3ffabf6814288073063d35609fe6535cd83947fa39d9456727f2d`  
		Last Modified: Fri, 24 Apr 2020 09:04:50 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:8185e8efd2afb5ae74f15257a1ab17b0750fcd888c77592e7da7365fa36aa8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:164a2020bbfdcebc48b736220f286b6d6cc867935869287e4f05afe928690cd1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8797283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474a16bc962201f303d7bc6d26bce9ddbb4ee2ee498e2cfbe88798b422deee8b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:21:14 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 24 Apr 2020 14:21:15 GMT
RUN adduser -S eggdrop
# Fri, 24 Apr 2020 14:21:16 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 24 Apr 2020 14:22:32 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 24 Apr 2020 14:23:22 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 24 Apr 2020 14:23:23 GMT
ENV NICK=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV SERVER=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV LISTEN=3333
# Fri, 24 Apr 2020 14:23:23 GMT
ENV OWNER=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV USERFILE=eggdrop.user
# Fri, 24 Apr 2020 14:23:23 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 24 Apr 2020 14:23:24 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 24 Apr 2020 14:23:24 GMT
EXPOSE 3333
# Fri, 24 Apr 2020 14:23:24 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Fri, 24 Apr 2020 14:23:24 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 24 Apr 2020 14:23:24 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 24 Apr 2020 14:23:25 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0cdf0ff845235e19454000f632a4d9bf6d978c7948da54b51bf3962d766f4c`  
		Last Modified: Fri, 24 Apr 2020 14:23:40 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05e553ff44d8d1344fff59fed8897d80984977807b655be3d15128815d5bcf0`  
		Last Modified: Fri, 24 Apr 2020 14:23:38 GMT  
		Size: 9.6 KB (9573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2ea2690f263ee9e3bbad72e3d426631672412762a5dbb0a9c3de374a77d17e`  
		Last Modified: Fri, 24 Apr 2020 14:23:44 GMT  
		Size: 2.7 MB (2684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d60d22e2e991596f29d84aef5ad465a365c8aea921b7f9f540b9e496259452d`  
		Last Modified: Fri, 24 Apr 2020 14:23:44 GMT  
		Size: 3.3 MB (3285724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ea18db1513b38e9605e34eb798b83fad2a20707470b30e4381e2eec2ec6db`  
		Last Modified: Fri, 24 Apr 2020 14:23:43 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b873e8173e8be5007fc16ef578eba2b973b90b418159527089ad5b4958e0502`  
		Last Modified: Fri, 24 Apr 2020 14:23:43 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:8185e8efd2afb5ae74f15257a1ab17b0750fcd888c77592e7da7365fa36aa8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:164a2020bbfdcebc48b736220f286b6d6cc867935869287e4f05afe928690cd1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8797283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474a16bc962201f303d7bc6d26bce9ddbb4ee2ee498e2cfbe88798b422deee8b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:21:14 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 24 Apr 2020 14:21:15 GMT
RUN adduser -S eggdrop
# Fri, 24 Apr 2020 14:21:16 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 24 Apr 2020 14:22:32 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 24 Apr 2020 14:23:22 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 24 Apr 2020 14:23:23 GMT
ENV NICK=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV SERVER=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV LISTEN=3333
# Fri, 24 Apr 2020 14:23:23 GMT
ENV OWNER=
# Fri, 24 Apr 2020 14:23:23 GMT
ENV USERFILE=eggdrop.user
# Fri, 24 Apr 2020 14:23:23 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 24 Apr 2020 14:23:24 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 24 Apr 2020 14:23:24 GMT
EXPOSE 3333
# Fri, 24 Apr 2020 14:23:24 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Fri, 24 Apr 2020 14:23:24 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 24 Apr 2020 14:23:24 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 24 Apr 2020 14:23:25 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0cdf0ff845235e19454000f632a4d9bf6d978c7948da54b51bf3962d766f4c`  
		Last Modified: Fri, 24 Apr 2020 14:23:40 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05e553ff44d8d1344fff59fed8897d80984977807b655be3d15128815d5bcf0`  
		Last Modified: Fri, 24 Apr 2020 14:23:38 GMT  
		Size: 9.6 KB (9573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2ea2690f263ee9e3bbad72e3d426631672412762a5dbb0a9c3de374a77d17e`  
		Last Modified: Fri, 24 Apr 2020 14:23:44 GMT  
		Size: 2.7 MB (2684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d60d22e2e991596f29d84aef5ad465a365c8aea921b7f9f540b9e496259452d`  
		Last Modified: Fri, 24 Apr 2020 14:23:44 GMT  
		Size: 3.3 MB (3285724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ea18db1513b38e9605e34eb798b83fad2a20707470b30e4381e2eec2ec6db`  
		Last Modified: Fri, 24 Apr 2020 14:23:43 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b873e8173e8be5007fc16ef578eba2b973b90b418159527089ad5b4958e0502`  
		Last Modified: Fri, 24 Apr 2020 14:23:43 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
