## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:72a31c7334a4bfbd4130c242240b169943c0f5d32685e9d9f5bdb3c620a3a043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:c4ebedf06862c9026d330cdd4338a64d7e3b89490339570140f4e6267a674839
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39697078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d62289e6d48df02c3eccf815833a7761bedd9be6b341e801e799d52395f26ea`
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
# Thu, 06 Oct 2022 20:37:03 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Thu, 06 Oct 2022 20:37:03 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Thu, 06 Oct 2022 20:37:04 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 06 Oct 2022 20:40:58 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:40:58 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:40:58 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:40:58 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:40:58 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:40:59 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:40:59 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:40:59 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:40:59 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:40:59 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:40:59 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:40:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:40:59 GMT
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
	-	`sha256:964303ee5d62f80866e95b46166f29a7be0468f0e716a1139834084d1207c01b`  
		Last Modified: Thu, 06 Oct 2022 20:42:27 GMT  
		Size: 1.1 MB (1089951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0e8a3453fdbbc9f5ffc9f8d53a61eea8148a23cd044982b920b601ce44ea3`  
		Last Modified: Thu, 06 Oct 2022 20:42:32 GMT  
		Size: 35.8 MB (35768829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a87c918fc6d1812304b4adb80d63e980cbd841ff7158022764c789c4f4c96c`  
		Last Modified: Thu, 06 Oct 2022 20:42:26 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f63ce19783f457880f6b6b97916947caeb76e4d0f6d0bc8ee04ce17788d9f4`  
		Last Modified: Thu, 06 Oct 2022 20:42:26 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:56d92d7d1b3fb19da36e36a0c6ecb10e9f82841988d391b219f2062074c16ee5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39089475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14abf1fb3ac41c0aa0f75edb489f24709b9b3b72cd93a7e86a1f8f1d0c60b3a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:03:00 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:03:00 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:03:01 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:03:02 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Thu, 06 Oct 2022 20:03:02 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Thu, 06 Oct 2022 20:03:03 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 06 Oct 2022 20:07:22 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:07:22 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:07:22 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:07:22 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:07:22 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:07:23 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:07:23 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:07:23 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:07:23 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:07:23 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:07:23 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:07:23 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:07:23 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26b6e2ab9ed4e4939d215dc6c3a329a190b6bf7a1050fc2024e0308a06a3973`  
		Last Modified: Thu, 06 Oct 2022 20:09:21 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90839ec2ad222a22d0f9266a297ee245744be011bac966e48c813c6b6382a`  
		Last Modified: Thu, 06 Oct 2022 20:09:19 GMT  
		Size: 10.7 KB (10655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1945403abbd221018a4262a7bf5c3b8293f43ab856e8d6866225d4b6e0e6c5`  
		Last Modified: Thu, 06 Oct 2022 20:09:20 GMT  
		Size: 1.0 MB (1032562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f17059a2c6014977c812871493885f8e770eb0f47d9a4db96ef62c2387171c`  
		Last Modified: Thu, 06 Oct 2022 20:09:27 GMT  
		Size: 35.4 MB (35411278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3927f9b97979f383b7066540afeea1bd7ee3260578222c0e53586ef2330de97c`  
		Last Modified: Thu, 06 Oct 2022 20:09:19 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a420f0b5e336bb077b3a6a10d1d1fb836736bb865456b41069e459ce07592b`  
		Last Modified: Thu, 06 Oct 2022 20:09:19 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2f4f47fb5fb7d10a35c1aa6328abe42690cbc858fa37c05b0a832413a55dbd4e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39757335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a75ff50f216be7e43914539a9ea25d0f596f427bc8ad65662211665fb38e75e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:09:47 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:09:48 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:09:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:09:50 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Thu, 06 Oct 2022 20:09:51 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Thu, 06 Oct 2022 20:09:52 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 06 Oct 2022 20:14:31 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:14:31 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:14:32 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:14:33 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:14:34 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:14:35 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:14:36 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:14:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:14:38 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:14:40 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:14:41 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:14:41 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:14:42 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ae7c1c7a9cf57ec4ef5bc0d760e018a0311f072731e1e901545c9782fd65c8`  
		Last Modified: Thu, 06 Oct 2022 20:16:57 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b485351e4651f72208d60653a9cb6c36bb54c79f68b2425fb5a56abb2841ded3`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87ea7cd947be80731b8ff53dd407cde03c2cd85241c969335c1daf35ad11612`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 1.1 MB (1087561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c7adbda228ebb750dd06ea1218347eb8ae7b23508e6e321a7acbe411493a7`  
		Last Modified: Thu, 06 Oct 2022 20:17:00 GMT  
		Size: 35.9 MB (35936831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea50726c4310e7b95883f40ab4219d7a46d83f5cab0ee0225e591d207709d83`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225cbb6c09999045b9e86ec94dedb3192bed5f338120ee7b752a73a6e0df34fe`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
