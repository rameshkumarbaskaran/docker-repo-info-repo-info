## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:abe33157c3548d61a52022c5f604aa185cb019a8c158a7052d35590e69cafc98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:3ce67c429faa0940691a25b69178376a7517a5316da0cb909d96da66c3088c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8587783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda93b1ac58bbf488b049e1ff2f3b78b5d24a7f05f4c7b2140ef067081328d13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:20:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 12 Nov 2022 05:20:03 GMT
RUN adduser -S eggdrop
# Sat, 12 Nov 2022 05:20:04 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 05:20:06 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 15 Dec 2022 18:24:35 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 15 Dec 2022 18:24:35 GMT
ENV NICK=
# Thu, 15 Dec 2022 18:24:35 GMT
ENV SERVER=
# Thu, 15 Dec 2022 18:24:35 GMT
ENV LISTEN=3333
# Thu, 15 Dec 2022 18:24:35 GMT
ENV OWNER=
# Thu, 15 Dec 2022 18:24:36 GMT
ENV USERFILE=eggdrop.user
# Thu, 15 Dec 2022 18:24:36 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 15 Dec 2022 18:24:36 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 15 Dec 2022 18:24:36 GMT
EXPOSE 3333
# Thu, 15 Dec 2022 18:24:36 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 15 Dec 2022 18:24:36 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 15 Dec 2022 18:24:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 15 Dec 2022 18:24:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdb365c6f8a662a987df4b9f8aa0a038b4ccf8835a9cf6a10c487d137c48493`  
		Last Modified: Sat, 12 Nov 2022 05:21:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc68fd90aec1c649bae31b0426236225d421b45b0010bc88add392ee53e0dcf0`  
		Last Modified: Sat, 12 Nov 2022 05:21:19 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cc94fc4b8d42ca4dc27cfd6217256fb76fdab0a0f617ee8f065a731a48c63c`  
		Last Modified: Sat, 12 Nov 2022 05:21:20 GMT  
		Size: 2.8 MB (2757973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad1a267f3d087fe7d0f6505f8e7dfef1b4ace808042a2a8ae29cb812f4fea53`  
		Last Modified: Thu, 15 Dec 2022 18:25:11 GMT  
		Size: 3.0 MB (3008779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c672e238e2da25ec4d3d554ff9cb85115b6133856f396e7cc05bdb2126968b81`  
		Last Modified: Thu, 15 Dec 2022 18:25:10 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fff0a5aefc166450f6287f3ab3c0ce47a0269271a795954ae1c77091cebea2`  
		Last Modified: Thu, 15 Dec 2022 18:25:10 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:50a07cdf1bada1775c3b781a3ee3737279bb43aeae54a819122ccd44196f93ec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11742560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c476afa7931112fd727f4327057d3b200838454a919953f051002743d1a3357`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:30:04 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 12 Nov 2022 04:30:04 GMT
RUN adduser -S eggdrop
# Sat, 12 Nov 2022 04:30:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 04:30:07 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 12 Jan 2023 23:59:04 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 12 Jan 2023 23:59:05 GMT
ENV NICK=
# Thu, 12 Jan 2023 23:59:05 GMT
ENV SERVER=
# Thu, 12 Jan 2023 23:59:05 GMT
ENV LISTEN=3333
# Thu, 12 Jan 2023 23:59:06 GMT
ENV OWNER=
# Thu, 12 Jan 2023 23:59:06 GMT
ENV USERFILE=eggdrop.user
# Thu, 12 Jan 2023 23:59:06 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 12 Jan 2023 23:59:06 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 12 Jan 2023 23:59:06 GMT
EXPOSE 3333
# Thu, 12 Jan 2023 23:59:07 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 12 Jan 2023 23:59:07 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 12 Jan 2023 23:59:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 12 Jan 2023 23:59:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6634c0ac1b0155242161d0523c05ac568cc7ea7fe315b83be1e9c30a35003815`  
		Last Modified: Sat, 12 Nov 2022 04:31:52 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da2504930a2fea0a18c825055d88cccea76872ba6bb63a0ee3417437e4f9715`  
		Last Modified: Sat, 12 Nov 2022 04:31:50 GMT  
		Size: 10.6 KB (10635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c78cb829fdc1f1248122fcf43eb2d037f10e1e2603b43986980e0f380e4ef5a`  
		Last Modified: Sat, 12 Nov 2022 04:31:51 GMT  
		Size: 2.7 MB (2679712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f50d8e33bc006254f1fc0de808bd47bc5b4c64472db5f67c9aa3a93220ab4cb`  
		Last Modified: Thu, 12 Jan 2023 23:59:48 GMT  
		Size: 6.4 MB (6433314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5621d9bbdf08fc9aa46b65d390c505b46e6fc29eb541ab32fa915b90c64d20`  
		Last Modified: Thu, 12 Jan 2023 23:59:46 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8809d0a9f10b50d803ceb4166179bd9d8a150d09704f29cf0bd999cf97a11d6a`  
		Last Modified: Thu, 12 Jan 2023 23:59:46 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:73648f94b4971b996d21f6d69d3a02f22fc12348be398b6fd10028f31b1d8022
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8545969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdad150055ad70cfaf82be589e7b8452cd254a451c13bb87c6eceff5cfbffce0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:04:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 12 Nov 2022 06:04:38 GMT
RUN adduser -S eggdrop
# Sat, 12 Nov 2022 06:04:39 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 06:04:40 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 15 Dec 2022 18:44:44 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 15 Dec 2022 18:44:44 GMT
ENV NICK=
# Thu, 15 Dec 2022 18:44:44 GMT
ENV SERVER=
# Thu, 15 Dec 2022 18:44:44 GMT
ENV LISTEN=3333
# Thu, 15 Dec 2022 18:44:45 GMT
ENV OWNER=
# Thu, 15 Dec 2022 18:44:45 GMT
ENV USERFILE=eggdrop.user
# Thu, 15 Dec 2022 18:44:45 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 15 Dec 2022 18:44:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 15 Dec 2022 18:44:45 GMT
EXPOSE 3333
# Thu, 15 Dec 2022 18:44:45 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 15 Dec 2022 18:44:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 15 Dec 2022 18:44:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 15 Dec 2022 18:44:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92c78c1ea1eb5bd99e8235633c5ca1d2a958406fd8a85aac01e596b1ff2417f`  
		Last Modified: Sat, 12 Nov 2022 06:05:48 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e27509a5daaf58faee461c8bfe32ca75c13af7a01476ebd7851958d6fb12f2`  
		Last Modified: Sat, 12 Nov 2022 06:05:45 GMT  
		Size: 10.7 KB (10744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c7e3fd37ee9132ed87bbe8aacd43c174f80d6f6234c8635c3580e0d1146df4`  
		Last Modified: Sat, 12 Nov 2022 06:05:46 GMT  
		Size: 2.8 MB (2776457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9437b2d02e3611eb914c84f805d4bb6fe19d85f5b29d41914b5d281f21c6c4fc`  
		Last Modified: Thu, 15 Dec 2022 18:45:10 GMT  
		Size: 3.0 MB (3047190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b7b447bbfc5dc87ed6ccb31b879dbeeb2cfab824bbe32900bc640293265482`  
		Last Modified: Thu, 15 Dec 2022 18:45:10 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c65adac070a167661967b988c637351ae909e7ab6db813cb5a9644ca6b098e`  
		Last Modified: Thu, 15 Dec 2022 18:45:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
