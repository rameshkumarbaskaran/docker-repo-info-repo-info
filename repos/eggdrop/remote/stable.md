## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:bf954c76a6b22bafa5a1152045e8320cec873b0adf46bfb885db6bd81d6a4ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:dc3eb82740c517c499ab8a0e0e6029d31a1355132e054984cd9c9da42631d8c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8786443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52c01e299f093296afc165d5f00b03e59207ddae8c434f7496b67c1292dce6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 23 Mar 2020 22:01:52 GMT
RUN adduser -S eggdrop
# Mon, 23 Mar 2020 22:01:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 23 Mar 2020 22:03:53 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 23 Mar 2020 22:05:14 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 23 Mar 2020 22:05:15 GMT
ENV NICK=
# Mon, 23 Mar 2020 22:05:15 GMT
ENV SERVER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV LISTEN=3333
# Mon, 23 Mar 2020 22:05:16 GMT
ENV OWNER=
# Mon, 23 Mar 2020 22:05:16 GMT
ENV USERFILE=eggdrop.user
# Mon, 23 Mar 2020 22:05:17 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 23 Mar 2020 22:05:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 23 Mar 2020 22:05:18 GMT
EXPOSE 3333
# Mon, 23 Mar 2020 22:05:18 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Mon, 23 Mar 2020 22:05:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 23 Mar 2020 22:05:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de90ac254f3b2092e08d0d1a27fade104236143c7429ad4bfd7a17858c302031`  
		Last Modified: Mon, 23 Mar 2020 22:05:43 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7989bd96822c15f6ae1d0789c29950de5717ef922d3f3f8e284011e9e169c4`  
		Last Modified: Mon, 23 Mar 2020 22:05:41 GMT  
		Size: 9.6 KB (9581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7689126dd51138dc04d8f316f2219b9bb5588d4f9a6b7fb9d19fe9917cfa76e`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 2.7 MB (2684248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c63278b54642d69450022162c6395d8b02367c5b0cc0745d295e8e4165b196c`  
		Last Modified: Mon, 23 Mar 2020 22:05:48 GMT  
		Size: 3.3 MB (3285542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef178bab7af5fea90f56fd61a8ee49c76fb93729d8d4deb48bf776213dc02c1e`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb097a7c2750f9c97142d213394ada805c5e33cba328e781699e8303c560664`  
		Last Modified: Mon, 23 Mar 2020 22:05:47 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
