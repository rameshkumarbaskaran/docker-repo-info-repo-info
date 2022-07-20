## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:0b7c2c3e25a3a20af54a60ce2c5b529901de52e169d6f8d1e3cd2e7c25ce6636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:167357057c64dbf146d6be251a103b299f818ee33114b1b8aa9ec38e4ba373df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39683291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dfc58496b5a1cf0c69dbe6533fbce4c0538431eb735fca60b4682a68bc1f53`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:22:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:22:54 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:22:55 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:22:56 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 19 Jul 2022 23:22:56 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 19 Jul 2022 23:22:57 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 19 Jul 2022 23:26:55 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:26:56 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:26:56 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:26:56 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:26:56 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:26:56 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:26:56 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:26:56 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:26:56 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:26:57 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:26:57 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:26:57 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:26:57 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce3ee76f2e28d4dd47d43d3605eb1c6af0e96fcafc28de6ec5379c5172ebb55`  
		Last Modified: Tue, 19 Jul 2022 23:28:25 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ac4a1d51bd2cc5020a4d0d0e2169d5cedbe911ba463dea6ad06a6a6ff0596d`  
		Last Modified: Tue, 19 Jul 2022 23:28:23 GMT  
		Size: 10.9 KB (10940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1db5a3780dd3366d59813dc8b37cd5cb8f7af399f04e32d57c1928fd9d4d9b2`  
		Last Modified: Tue, 19 Jul 2022 23:28:23 GMT  
		Size: 1.1 MB (1089912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d536323f2786afb7faba1bacc8dd118128b0aa364ef3b02502548c995c77e6a`  
		Last Modified: Tue, 19 Jul 2022 23:28:28 GMT  
		Size: 35.8 MB (35763938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191c01706265110ab1e69ea5fb73fa571136f6bf45e57291a2257228da38f09e`  
		Last Modified: Tue, 19 Jul 2022 23:28:23 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db96b5e1af04782658496a1aec79cbf4703fb50cbe4647b25442b945f4e9f4b3`  
		Last Modified: Tue, 19 Jul 2022 23:28:23 GMT  
		Size: 702.0 B  
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
$ docker pull eggdrop@sha256:21d798f07747179773d3cc07f708ec442fe94b266cb0c940ceffc5c5de7cf8b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39756377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976062a942c1aba30c130d5dac5cc76b1b9cf30429ffa49c00d1ea830425164f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:26:37 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 19 Jul 2022 23:26:38 GMT
RUN adduser -S eggdrop
# Tue, 19 Jul 2022 23:26:39 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 19 Jul 2022 23:26:40 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 19 Jul 2022 23:26:41 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 19 Jul 2022 23:26:42 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 19 Jul 2022 23:31:22 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 19 Jul 2022 23:31:23 GMT
ENV NICK=
# Tue, 19 Jul 2022 23:31:24 GMT
ENV SERVER=
# Tue, 19 Jul 2022 23:31:25 GMT
ENV LISTEN=3333
# Tue, 19 Jul 2022 23:31:26 GMT
ENV OWNER=
# Tue, 19 Jul 2022 23:31:27 GMT
ENV USERFILE=eggdrop.user
# Tue, 19 Jul 2022 23:31:28 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 19 Jul 2022 23:31:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 19 Jul 2022 23:31:30 GMT
EXPOSE 3333
# Tue, 19 Jul 2022 23:31:32 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 19 Jul 2022 23:31:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 19 Jul 2022 23:31:33 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 19 Jul 2022 23:31:34 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f733119a90d66cc38b960cfd3a82f5ac1bf15b88c4210aa7d8daffbae880b8b`  
		Last Modified: Tue, 19 Jul 2022 23:33:36 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046d236c13e8c2c0071dd8655962c99baffb43bb2f6376c65f56bba0b40963af`  
		Last Modified: Tue, 19 Jul 2022 23:33:34 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468fce109fc975be6dbeac73ae066d0fad7aa1479d47d37e32d44ca79bd0567b`  
		Last Modified: Tue, 19 Jul 2022 23:33:34 GMT  
		Size: 1.1 MB (1087539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559fad7e7f02484465220157b063a741a67862e772ec7f0902431614e778e654`  
		Last Modified: Tue, 19 Jul 2022 23:33:39 GMT  
		Size: 35.9 MB (35937439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafc071d54893d348ab170bc20d3b4043025b9b5ba9f4ec960a6626f911e8864`  
		Last Modified: Tue, 19 Jul 2022 23:33:34 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65748c0b1d2f7521c9d2e446166aab0f2295eff54e6f05dad946b848e7e1d71`  
		Last Modified: Tue, 19 Jul 2022 23:33:34 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
