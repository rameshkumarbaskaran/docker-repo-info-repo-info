## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:979dd0a571a6d884d6f4005d87e259b01d2eccf4a693b93a11467bd071f51274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:0dbae2bcb5c0afd85aeb02ecb33593d552ee8eade082997d60ee456b82360bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16146288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43a30c2649a2e91dcfd939f8d0c20f89f38b9c5ca0237b606bd16b87e1f78ff`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:38:43 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 01 Dec 2023 06:38:44 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Fri, 01 Dec 2023 06:38:45 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Fri, 01 Dec 2023 06:38:45 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Fri, 01 Dec 2023 06:38:45 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Fri, 01 Dec 2023 06:40:53 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Fri, 01 Dec 2023 06:40:53 GMT
ENV NICK=
# Fri, 01 Dec 2023 06:40:53 GMT
ENV SERVER=
# Fri, 01 Dec 2023 06:40:53 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 06:40:53 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 06:40:53 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 06:40:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 06:40:53 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 06:40:53 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Fri, 01 Dec 2023 06:40:54 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Fri, 01 Dec 2023 06:40:54 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 06:40:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8d4286230b4d5d95213c19d08015e2d35beb2cffa862992135f0c6a48ba37d`  
		Last Modified: Fri, 01 Dec 2023 06:45:22 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0abd1b087ea616c57c07d1fd242635b591f81b010064f6743f66f46eea39562`  
		Last Modified: Fri, 01 Dec 2023 06:45:22 GMT  
		Size: 1.2 MB (1208548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6afb6802bb96586ab96437c600cdb4a8b9bd5abc46c015bf0f65030badd2d71`  
		Last Modified: Fri, 01 Dec 2023 06:45:24 GMT  
		Size: 11.6 MB (11554131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751ec9b32617d65b3a17cbcd4ce853093b934cafd61065d9e45e88efa26f6918`  
		Last Modified: Fri, 01 Dec 2023 06:45:22 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7f8e4e30612777c2e9f1478c6164967167c7b009f21d33947e3f5c036dde95`  
		Last Modified: Fri, 01 Dec 2023 06:45:22 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:efadae87c1de5e32ec5ae3feaa94ad1036efb3c68fcc7d0ebe87048259ade9c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15746145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a40062f619d324347fe62da0cfa525c5ce5637d14878fcfe8a16530bdfcf0f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:21 GMT
ADD file:90d3bdc6a557ead63796de0110e2fda87e65aa091070cbae612dfb2126568253 in / 
# Thu, 30 Nov 2023 22:49:21 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:44:28 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 01 Dec 2023 00:44:29 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Fri, 01 Dec 2023 00:44:30 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Fri, 01 Dec 2023 00:44:30 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Fri, 01 Dec 2023 00:44:30 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Fri, 01 Dec 2023 00:46:45 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Fri, 01 Dec 2023 00:46:45 GMT
ENV NICK=
# Fri, 01 Dec 2023 00:46:45 GMT
ENV SERVER=
# Fri, 01 Dec 2023 00:46:45 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 00:46:45 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 00:46:46 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 00:46:46 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 00:46:46 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 00:46:46 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Fri, 01 Dec 2023 00:46:46 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Fri, 01 Dec 2023 00:46:46 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 00:46:46 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f0440ff44d712e5fc701b84856116589b428157893ac461b633b1ab30b627eed`  
		Last Modified: Thu, 30 Nov 2023 22:49:52 GMT  
		Size: 3.1 MB (3113003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2007141e1acfb13278961b1dd692cc8a98a7e1b62eeaff37f1adbb12e8430e42`  
		Last Modified: Fri, 01 Dec 2023 00:51:36 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468e6c2f98a7e7b040cfec6a1355ead740cfd1a1808df7dbd49a65179c31bf27`  
		Last Modified: Fri, 01 Dec 2023 00:51:35 GMT  
		Size: 1.2 MB (1190279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c6293eb2d227b278db01528877de24f462ee047e43c001dca3e2fb96b50088`  
		Last Modified: Fri, 01 Dec 2023 00:51:37 GMT  
		Size: 11.4 MB (11438578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cf3ee2be1b239ea78d66ba74bda662c437d4bc32f1e42dc04cc83c5076c289`  
		Last Modified: Fri, 01 Dec 2023 00:51:35 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382e1ecf17320063154e4d3958995df68ef0b8e7330a1d167d7ba6a06d44fde`  
		Last Modified: Fri, 01 Dec 2023 00:51:35 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:70c32e454aca8c3516627dcde5ed95984bd6101e20fa8af37bf0cc0e2f8f7e93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16114076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f0456d051e5a6a9382948a1fbc291bed7d971febf90183ba72e2096acf1870`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:53 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 01 Dec 2023 03:11:53 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Fri, 01 Dec 2023 03:11:55 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Fri, 01 Dec 2023 03:11:55 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Fri, 01 Dec 2023 03:11:55 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Fri, 01 Dec 2023 03:13:43 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Fri, 01 Dec 2023 03:13:44 GMT
ENV NICK=
# Fri, 01 Dec 2023 03:13:44 GMT
ENV SERVER=
# Fri, 01 Dec 2023 03:13:44 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 03:13:44 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 03:13:44 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 03:13:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 03:13:44 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 03:13:44 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Fri, 01 Dec 2023 03:13:44 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Fri, 01 Dec 2023 03:13:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 03:13:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bacdc4b43589aef43c1d2c353fd54809834e48f4c5df7638a530b51b9c6673`  
		Last Modified: Fri, 01 Dec 2023 03:17:59 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff546a7c3f3fd3c5b3d6deb4fd081a3d899c9c0e34e88598d3ea87de5945259`  
		Last Modified: Fri, 01 Dec 2023 03:18:00 GMT  
		Size: 1.2 MB (1235871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0eca6e881ad2d151b651e87f832ed570e938a42fd3458ff262c735ac05d924`  
		Last Modified: Fri, 01 Dec 2023 03:18:01 GMT  
		Size: 11.6 MB (11615569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317b5fc59491b349f7f90bdcbf66f6a91bcea032b81c0656612af288d30fb380`  
		Last Modified: Fri, 01 Dec 2023 03:17:59 GMT  
		Size: 2.0 KB (1953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39617066b3ff6192087a015914df6009055915d33a4311aff0536537a161d1ae`  
		Last Modified: Fri, 01 Dec 2023 03:17:59 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
