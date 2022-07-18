## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:1119f9826d82b78c5c45fe0378d6ad03482f1b7a3e768b7ae96dfe60f8ff5cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:fd04d974fd1c59c3b4b00aaebd1d423bbc8282e08f4fdd8511d1da02ee7e358b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41162459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b700906d1f334863ac63c56310df99794fa9b300cc8e2d62731f818b71cff6c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:12:25 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 11:12:25 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 11:12:26 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 20:04:56 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Mon, 18 Jul 2022 20:04:56 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Mon, 18 Jul 2022 20:04:57 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 18 Jul 2022 20:09:08 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 20:09:09 GMT
ENV NICK=
# Mon, 18 Jul 2022 20:09:09 GMT
ENV SERVER=
# Mon, 18 Jul 2022 20:09:09 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 20:09:09 GMT
ENV OWNER=
# Mon, 18 Jul 2022 20:09:09 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 20:09:09 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 20:09:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 20:09:09 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 20:09:09 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 20:09:10 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 20:09:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 20:09:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afb7ebc822c4005d25f15d49dada11e4a41876f643351d04feea9b2b22840cc`  
		Last Modified: Tue, 05 Apr 2022 11:17:40 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e7bd2972241b11e355dd2e732c2f4dbcbe0a9624d7b8c43e68e1b891810d4a`  
		Last Modified: Tue, 05 Apr 2022 11:17:38 GMT  
		Size: 10.9 KB (10946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d60371653cbbb6a799e42cb68c55b92664ae5911ef01810663a723143150e5`  
		Last Modified: Mon, 18 Jul 2022 20:10:40 GMT  
		Size: 1.1 MB (1089973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d24c077be4de74a52f909f02afcfc69d58682843febf251086770019f322`  
		Last Modified: Mon, 18 Jul 2022 20:10:46 GMT  
		Size: 37.2 MB (37243117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783f43bb535cfc33101e684d42ec7aa469226106f327c2b257dbd55c4b49876c`  
		Last Modified: Mon, 18 Jul 2022 20:10:40 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da194030311da981b6b28720ea05b81e3c14deea5af6f40ee0b6274ff0c839ee`  
		Last Modified: Mon, 18 Jul 2022 20:10:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c9e126616745f437a1316d309084832d58151fafeb28b07c662db54fad03cf70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40314778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545abc69ab2eef92b2edbf01cbdd08740e6842bd1e6b477d8e6047b6b96f7fe4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:31:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:31:46 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:31:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 18:49:45 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Mon, 18 Jul 2022 18:49:45 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Mon, 18 Jul 2022 18:49:48 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 18 Jul 2022 19:00:28 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 19:00:29 GMT
ENV NICK=
# Mon, 18 Jul 2022 19:00:29 GMT
ENV SERVER=
# Mon, 18 Jul 2022 19:00:29 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 19:00:30 GMT
ENV OWNER=
# Mon, 18 Jul 2022 19:00:30 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 19:00:31 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 19:00:31 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 19:00:31 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 19:00:32 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 19:00:32 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 19:00:33 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 19:00:33 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f46acd206d1b9854dd7a69f3dd94d51ffb03228b347337d6755524e938f848d`  
		Last Modified: Tue, 05 Apr 2022 03:45:57 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ab9123d31326e4f773e35061abb57883ec6b6221e6df8719354fc8598c9123`  
		Last Modified: Tue, 05 Apr 2022 03:45:55 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f36aa237eb1d5a61f87401541fbc3b6b7c9fa196207eeb0fa78f126ff9145e`  
		Last Modified: Mon, 18 Jul 2022 19:04:34 GMT  
		Size: 1.0 MB (1032591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad3257c3ec35772168580fe6515ac2a515576ab7e6ea173ee9db5868c50f2c8`  
		Last Modified: Mon, 18 Jul 2022 19:04:58 GMT  
		Size: 36.6 MB (36645704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bd986b36f8bae82826097ae809bd11ee15f40d48ba1753fc9a8309e4bc9772`  
		Last Modified: Mon, 18 Jul 2022 19:04:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac6a5f8fc7f345fdc59052ce1153c7fc0f3c4e559a2ec14f6baaf732376285`  
		Last Modified: Mon, 18 Jul 2022 19:04:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:d83678d2eb7f05433e3077b917f5ae5d9bb3e0d04bcd2d3d50f0cdf65f59b77e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41105869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed5f47239adf5ad860a32263105693ed8520f07de6df888326210c8a4ce267e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:03:36 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 04:03:37 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 04:03:38 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 19:04:00 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Mon, 18 Jul 2022 19:04:01 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Mon, 18 Jul 2022 19:04:03 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 18 Jul 2022 19:08:41 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 19:08:41 GMT
ENV NICK=
# Mon, 18 Jul 2022 19:08:42 GMT
ENV SERVER=
# Mon, 18 Jul 2022 19:08:43 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 19:08:44 GMT
ENV OWNER=
# Mon, 18 Jul 2022 19:08:45 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 19:08:46 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 19:08:47 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 19:08:48 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 19:08:50 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 19:08:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 19:08:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 19:08:52 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687fbd14cec7fbb8ee2d3dfd1bedd832165c780a579635649359ea5d966007c3`  
		Last Modified: Tue, 05 Apr 2022 04:10:33 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778e0ebd563495b9fbda0eb57ed55b539e2a45c085cbb1dc1866b09b01007cb8`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 10.7 KB (10674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52078216c257b43f5ec723592db0ef148d021477c2a3ae869e13b3c1b17540b7`  
		Last Modified: Mon, 18 Jul 2022 19:10:59 GMT  
		Size: 1.1 MB (1087601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b594dd26f8aef28728f4732d32d9b40b251de22d12f1aaae6fac53ec8c919954`  
		Last Modified: Mon, 18 Jul 2022 19:11:04 GMT  
		Size: 37.3 MB (37287276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d475a701cf7af470e6f914a72b4eecca7163c657883e7574156a121155d2486e`  
		Last Modified: Mon, 18 Jul 2022 19:10:58 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2599fbdb93451279b9f84ff9e86c8a93f494ef785aa457560446d3e9763fb3`  
		Last Modified: Mon, 18 Jul 2022 19:10:58 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
