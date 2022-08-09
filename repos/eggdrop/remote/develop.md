## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:0e2b70a7b8a83bbadecb59cb2a1c8e942944148320dbba020f0a834fec1a303a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:c782c9d94bb89c734c3277fb534f9e1aada70acfd368de7b8ad2ac3ccab46d5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39697640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc2a3ddd459b82cc505383ba6f2229104d60e5b5807640dc36903f373930dbb`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:29:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:29:50 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:29:51 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:29:51 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 09 Aug 2022 18:29:51 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 09 Aug 2022 18:29:52 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 09 Aug 2022 18:33:47 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:33:48 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:33:48 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:33:48 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:33:48 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:33:48 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:33:48 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:33:49 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:33:49 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:33:49 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:33:49 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:33:49 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:33:49 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c168c83c5b7cbf66a9e59b6eeb2681bba349bbfcfb2210a9e498fbd081911b8`  
		Last Modified: Tue, 09 Aug 2022 18:36:28 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ada8ef30839b781a7752202bb0508c0b31289da9d6c8e2c579b714517f21ca`  
		Last Modified: Tue, 09 Aug 2022 18:36:26 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5a6827106d9ac255c1074ade8a834fad1c2c24c59abbaa036c30ea7e50bc68`  
		Last Modified: Tue, 09 Aug 2022 18:36:26 GMT  
		Size: 1.1 MB (1089939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd6758e0fde641f96ae3752b918e7005398fc332b5ba08b3fa03ab91e77df9a`  
		Last Modified: Tue, 09 Aug 2022 18:36:31 GMT  
		Size: 35.8 MB (35769404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34e9bb594cf5cb810d65d664e8bd68f3a0c975d4d4b00154b7d9f40f8439680`  
		Last Modified: Tue, 09 Aug 2022 18:36:26 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3664d2d4b6b34c02f920ac62c60d8a02b7f86ad43518170e9f6669027382bb85`  
		Last Modified: Tue, 09 Aug 2022 18:36:25 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5708b3cdfd986537b8e3ea8d34cda88cd993f5bfb5cc6785c14136c4698e3e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39089261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ee4e6c23206e9a11d221ab76fb1562f8ca76c71216c6363694cbc051e50f89`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:46:24 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:46:24 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:46:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:46:26 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 09 Aug 2022 18:46:26 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 09 Aug 2022 18:46:27 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 09 Aug 2022 18:50:43 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:50:44 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:50:44 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:50:44 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:50:44 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:50:44 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:50:45 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:50:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:50:45 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:50:45 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:50:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:50:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:50:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b0548d2e71c5e0d69a7d82b4707fa752adad30ef06fb8d34592c20144b1904`  
		Last Modified: Tue, 09 Aug 2022 18:54:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efa052f331402356a00e0435bf34e783a18b22cb899d2daf4ec7ed61bea0727`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e349162c85bd03d527832a51a9da69584af33d92d8edf9a2207c4ddbc958d10`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 1.0 MB (1032556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c61638079e5b7979624aeb3f087b465bbffad1dfb59d11b92390d10a9dc478`  
		Last Modified: Tue, 09 Aug 2022 18:54:18 GMT  
		Size: 35.4 MB (35411073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2eb13384450fae5712b634f4008cea093f07ea7f518bac5a47507283fe8a9e8`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf747ffa38af6270fefdb2f9235b0c6e9e21c8f7f51ad1c2c9047c14c55acb8a`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 702.0 B  
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
