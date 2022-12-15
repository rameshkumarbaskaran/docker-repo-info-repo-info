## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:92abf8406dd6ddb745eb3c8b84503ac2fc6e9c517419af6ca70b15f3ecb4b863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:5f0243189a8b11739f20bf8a17fb1296d576cf812e3bfe6df177f90e40cf9841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41192505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b8df50611895b460125bdb521c1a558e5cc61721b96eea85af17354de1b18e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:37:01 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:37:02 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:37:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Dec 2022 18:19:31 GMT
ENV EGGDROP_SHA256=297c0dacb6c3ea03b260d863be9f0f34099f5ed6d4f4ba07b7493b0f66c2cbae
# Thu, 15 Dec 2022 18:19:31 GMT
ENV EGGDROP_COMMIT=6f4309cdfb82cf0763c27d30a3db75dc96e4a8ab
# Thu, 15 Dec 2022 18:19:32 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 15 Dec 2022 18:23:24 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 15 Dec 2022 18:23:25 GMT
ENV NICK=
# Thu, 15 Dec 2022 18:23:25 GMT
ENV SERVER=
# Thu, 15 Dec 2022 18:23:25 GMT
ENV LISTEN=3333
# Thu, 15 Dec 2022 18:23:25 GMT
ENV OWNER=
# Thu, 15 Dec 2022 18:23:25 GMT
ENV USERFILE=eggdrop.user
# Thu, 15 Dec 2022 18:23:25 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 15 Dec 2022 18:23:25 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 15 Dec 2022 18:23:25 GMT
EXPOSE 3333
# Thu, 15 Dec 2022 18:23:25 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 15 Dec 2022 18:23:26 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 15 Dec 2022 18:23:26 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 15 Dec 2022 18:23:26 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd629a2e1daaf15d9fdb2bd171b0a8c0622c4f982e7a6b1059c076fb9e1b42e5`  
		Last Modified: Thu, 06 Oct 2022 20:42:28 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfd741c22df00a71bc308727ead4698aa665f26cbf98ae6e3899b5c94acef40`  
		Last Modified: Thu, 06 Oct 2022 20:42:26 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea7c595cb72c9da2a102930c6ee04850cf54922c68591be678b3bd6454c9330`  
		Last Modified: Thu, 15 Dec 2022 18:24:58 GMT  
		Size: 1.1 MB (1090158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7643fad9a4a5befbeb08d5e178f86b544abe6ee4bb7b7fd72a9ee4caa61f3ce9`  
		Last Modified: Thu, 15 Dec 2022 18:25:04 GMT  
		Size: 37.3 MB (37264032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44da921ce5b7b6be6d9feb6c9286e335a3300f9bd0b702f279024f7a5d523fb0`  
		Last Modified: Thu, 15 Dec 2022 18:24:58 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d28f08e7cb51193d79d2bc117cbf7889a3d35a049259b878844f3ab4cc511c8`  
		Last Modified: Thu, 15 Dec 2022 18:24:58 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:61f67d749b7bab5d47956acb9a2512dc8107c11a0522489beb398ebca1cdbdf8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40344007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95a190e009ac355c298130ea5c9763b2e4246a023bdecb62dbaa34267f76640`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:36 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Thu, 10 Nov 2022 20:49:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 21:34:46 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 10 Nov 2022 21:34:47 GMT
RUN adduser -S eggdrop
# Thu, 10 Nov 2022 21:34:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Dec 2022 17:49:26 GMT
ENV EGGDROP_SHA256=297c0dacb6c3ea03b260d863be9f0f34099f5ed6d4f4ba07b7493b0f66c2cbae
# Thu, 15 Dec 2022 17:49:27 GMT
ENV EGGDROP_COMMIT=6f4309cdfb82cf0763c27d30a3db75dc96e4a8ab
# Thu, 15 Dec 2022 17:49:28 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 15 Dec 2022 17:53:56 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 15 Dec 2022 17:53:57 GMT
ENV NICK=
# Thu, 15 Dec 2022 17:53:57 GMT
ENV SERVER=
# Thu, 15 Dec 2022 17:53:57 GMT
ENV LISTEN=3333
# Thu, 15 Dec 2022 17:53:57 GMT
ENV OWNER=
# Thu, 15 Dec 2022 17:53:57 GMT
ENV USERFILE=eggdrop.user
# Thu, 15 Dec 2022 17:53:57 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 15 Dec 2022 17:53:57 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 15 Dec 2022 17:53:57 GMT
EXPOSE 3333
# Thu, 15 Dec 2022 17:53:57 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 15 Dec 2022 17:53:57 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 15 Dec 2022 17:53:58 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 15 Dec 2022 17:53:58 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b34cb66db1266899fb04b5d23484182b4fbaeb962888748f7cf45b5469e1cc`  
		Last Modified: Thu, 10 Nov 2022 21:43:03 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b411ce6f41f3486b16f301c44530bcdff2350b1a818209f912759aa06bded636`  
		Last Modified: Thu, 10 Nov 2022 21:43:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8135fd3b1a7fb4ba0376bff32ea0d6c3c8583357f33897100650bc82b67c85b3`  
		Last Modified: Thu, 15 Dec 2022 17:55:52 GMT  
		Size: 1.0 MB (1032680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f2e51c5d562836cfc4b9e9d24a82a6ff1ef92bb4a3f7f21ee66c3249ab859c`  
		Last Modified: Thu, 15 Dec 2022 17:55:59 GMT  
		Size: 36.7 MB (36665702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2d2b140cf7b5f900e4663a7cda3292efc55712020d95ccc9a181cfb641c723`  
		Last Modified: Thu, 15 Dec 2022 17:55:52 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebdf142c9f098b251a2d2ca742b6beb01d95a8df4de3fe8f806336a7ab9ec93`  
		Last Modified: Thu, 15 Dec 2022 17:55:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:30b0b6f2e0aa309db6cc58084a181c77398ca5500b4dc029d588c6df5245d5b3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41130107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281d1b61f7d2cecbc0a979c50d0eeaf9b0026cd54ccc8b62573f80061de6a572`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:03:31 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 10 Nov 2022 22:03:31 GMT
RUN adduser -S eggdrop
# Thu, 10 Nov 2022 22:03:32 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Dec 2022 18:40:14 GMT
ENV EGGDROP_SHA256=297c0dacb6c3ea03b260d863be9f0f34099f5ed6d4f4ba07b7493b0f66c2cbae
# Thu, 15 Dec 2022 18:40:14 GMT
ENV EGGDROP_COMMIT=6f4309cdfb82cf0763c27d30a3db75dc96e4a8ab
# Thu, 15 Dec 2022 18:40:15 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 15 Dec 2022 18:43:47 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 15 Dec 2022 18:43:47 GMT
ENV NICK=
# Thu, 15 Dec 2022 18:43:47 GMT
ENV SERVER=
# Thu, 15 Dec 2022 18:43:47 GMT
ENV LISTEN=3333
# Thu, 15 Dec 2022 18:43:47 GMT
ENV OWNER=
# Thu, 15 Dec 2022 18:43:47 GMT
ENV USERFILE=eggdrop.user
# Thu, 15 Dec 2022 18:43:47 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 15 Dec 2022 18:43:47 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 15 Dec 2022 18:43:47 GMT
EXPOSE 3333
# Thu, 15 Dec 2022 18:43:48 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 15 Dec 2022 18:43:48 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 15 Dec 2022 18:43:48 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 15 Dec 2022 18:43:48 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0978db877eba00ad9d43a52f1f6b67ecf10580acd57dcecb0bbf56618c8b6c6`  
		Last Modified: Thu, 10 Nov 2022 22:08:28 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70602ff34b989fc029480804413ff335d293fb78a34841211b726953832e7d3d`  
		Last Modified: Thu, 10 Nov 2022 22:08:26 GMT  
		Size: 10.8 KB (10767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da0cd2e9e3988dfb1f4958b1f57afd10d44ec27c08bf3d6a59f436664eda4b8`  
		Last Modified: Thu, 15 Dec 2022 18:44:59 GMT  
		Size: 1.1 MB (1087928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b961d9173ccbd25198ddd2034fff1883b21ceea2198f7323113dca243664f1b3`  
		Last Modified: Thu, 15 Dec 2022 18:45:03 GMT  
		Size: 37.3 MB (37309110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e752f3f0c6123e2ed22543e67bb1ab2162cc122468aee37d187f70afa50b88`  
		Last Modified: Thu, 15 Dec 2022 18:44:58 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edafd910e5c7f087c40967636d5930decddccec5db72a139f1b1ea717b81cdf5`  
		Last Modified: Thu, 15 Dec 2022 18:44:58 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
