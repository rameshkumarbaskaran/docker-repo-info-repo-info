<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.4`](#eggdrop194)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:553f9f680e0f23ce7305e9e6f0df4742f6de01be1ea0c6b0578c7e5c01d754de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

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

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b380ac1a9a797f825411f8ca4ee8f3b97d727e3509fe406083878cd326778847
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8336614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d4bb15e44111516a55890b867a07bdcb783017d29e8439099a4074b95c6508`
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
# Thu, 15 Dec 2022 17:55:19 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 15 Dec 2022 17:55:19 GMT
ENV NICK=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV SERVER=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV LISTEN=3333
# Thu, 15 Dec 2022 17:55:19 GMT
ENV OWNER=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 15 Dec 2022 17:55:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 15 Dec 2022 17:55:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 15 Dec 2022 17:55:20 GMT
EXPOSE 3333
# Thu, 15 Dec 2022 17:55:20 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 15 Dec 2022 17:55:20 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 15 Dec 2022 17:55:20 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 15 Dec 2022 17:55:20 GMT
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
	-	`sha256:977bd0f129212a2f63565b44f77bf6dbc0cedb50e7c5d54bcc50e304d02ed9cc`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 3.0 MB (3027367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfb96772ab0bf8facffec93ff552abd5f3be28afac1064ee956f6e33292d3cc`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d37bbbdd0201657c2674731718169aa583ca30379a84283d77b7c9eda909af5`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

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

## `eggdrop:1.9.4`

```console
$ docker pull eggdrop@sha256:553f9f680e0f23ce7305e9e6f0df4742f6de01be1ea0c6b0578c7e5c01d754de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.4` - linux; amd64

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

### `eggdrop:1.9.4` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b380ac1a9a797f825411f8ca4ee8f3b97d727e3509fe406083878cd326778847
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8336614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d4bb15e44111516a55890b867a07bdcb783017d29e8439099a4074b95c6508`
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
# Thu, 15 Dec 2022 17:55:19 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 15 Dec 2022 17:55:19 GMT
ENV NICK=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV SERVER=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV LISTEN=3333
# Thu, 15 Dec 2022 17:55:19 GMT
ENV OWNER=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 15 Dec 2022 17:55:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 15 Dec 2022 17:55:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 15 Dec 2022 17:55:20 GMT
EXPOSE 3333
# Thu, 15 Dec 2022 17:55:20 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 15 Dec 2022 17:55:20 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 15 Dec 2022 17:55:20 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 15 Dec 2022 17:55:20 GMT
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
	-	`sha256:977bd0f129212a2f63565b44f77bf6dbc0cedb50e7c5d54bcc50e304d02ed9cc`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 3.0 MB (3027367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfb96772ab0bf8facffec93ff552abd5f3be28afac1064ee956f6e33292d3cc`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d37bbbdd0201657c2674731718169aa583ca30379a84283d77b7c9eda909af5`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.4` - linux; arm64 variant v8

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

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:a48395b9129145f29771e82f817b517a098cf97890ea1730d19fbfc49d801f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:79ac16c723c408b20527f372bdaecadaeef3d17a0c2de2c980b23be1396b233a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41192703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce0053b1783faa2ba278cf264822bc1446d3aa53c784e4573a10b54e9a9b05`
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
# Mon, 02 Jan 2023 18:23:23 GMT
ENV EGGDROP_SHA256=caafc1ad001e2e77793dca37998cb94d88efadb4ec9c3de44c1004b04f15aa6e
# Mon, 02 Jan 2023 18:23:23 GMT
ENV EGGDROP_COMMIT=2a6a36888f5aa2204d84a9e6282d35e5421c2c8a
# Mon, 02 Jan 2023 18:23:24 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 02 Jan 2023 18:27:21 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 02 Jan 2023 18:27:21 GMT
ENV NICK=
# Mon, 02 Jan 2023 18:27:21 GMT
ENV SERVER=
# Mon, 02 Jan 2023 18:27:21 GMT
ENV LISTEN=3333
# Mon, 02 Jan 2023 18:27:21 GMT
ENV OWNER=
# Mon, 02 Jan 2023 18:27:21 GMT
ENV USERFILE=eggdrop.user
# Mon, 02 Jan 2023 18:27:22 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 02 Jan 2023 18:27:22 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 02 Jan 2023 18:27:22 GMT
EXPOSE 3333
# Mon, 02 Jan 2023 18:27:22 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Mon, 02 Jan 2023 18:27:22 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 02 Jan 2023 18:27:22 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 02 Jan 2023 18:27:22 GMT
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
	-	`sha256:689efdd2fe8f24ef5736ec9110f67ae9b0ac450c5533cce1bad38d76192346ea`  
		Last Modified: Mon, 02 Jan 2023 18:27:42 GMT  
		Size: 1.1 MB (1090156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6ee02fd55f70247e17cdd1cad82664d3b7aab6963d00780c88d6b727c22570`  
		Last Modified: Mon, 02 Jan 2023 18:27:47 GMT  
		Size: 37.3 MB (37263856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150b454aae0ab1252c8c8f729df781015219124d1db8094687db52edeb560397`  
		Last Modified: Mon, 02 Jan 2023 18:27:41 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0777469ef0844a243aad5db67723b0d38167ae32d448d0c37bfd47a86e4097a4`  
		Last Modified: Mon, 02 Jan 2023 18:27:41 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5da006fd7ea92b30021cad06640ad6d8c9806fb51da7d81d1d5e076d67b6eb70
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40344335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5649301a76ad615c585682a9ad8316efa8a6b4965f0a3306cf803e56a70e8d3`
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
# Mon, 02 Jan 2023 17:53:30 GMT
ENV EGGDROP_SHA256=caafc1ad001e2e77793dca37998cb94d88efadb4ec9c3de44c1004b04f15aa6e
# Mon, 02 Jan 2023 17:53:30 GMT
ENV EGGDROP_COMMIT=2a6a36888f5aa2204d84a9e6282d35e5421c2c8a
# Mon, 02 Jan 2023 17:53:32 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 02 Jan 2023 17:58:07 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 02 Jan 2023 17:58:08 GMT
ENV NICK=
# Mon, 02 Jan 2023 17:58:09 GMT
ENV SERVER=
# Mon, 02 Jan 2023 17:58:09 GMT
ENV LISTEN=3333
# Mon, 02 Jan 2023 17:58:09 GMT
ENV OWNER=
# Mon, 02 Jan 2023 17:58:09 GMT
ENV USERFILE=eggdrop.user
# Mon, 02 Jan 2023 17:58:09 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 02 Jan 2023 17:58:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 02 Jan 2023 17:58:09 GMT
EXPOSE 3333
# Mon, 02 Jan 2023 17:58:09 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Mon, 02 Jan 2023 17:58:09 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 02 Jan 2023 17:58:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 02 Jan 2023 17:58:10 GMT
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
	-	`sha256:f80e32b4b1273dc126b76d604cf41a5072ebc6bc1cea3eef47a69fd2fc461029`  
		Last Modified: Mon, 02 Jan 2023 17:58:49 GMT  
		Size: 1.0 MB (1032686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1519581bdda6a0a4134f1162287408462aa16c295b8cfae90d39395f4b003e39`  
		Last Modified: Mon, 02 Jan 2023 17:58:55 GMT  
		Size: 36.7 MB (36665650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da0db09093c9bfb500f45689e4b5387613c1fea5a5fa10bad1b63b542c30034`  
		Last Modified: Mon, 02 Jan 2023 17:58:49 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7061b691ffb83572e42c305eab8b98b338c694539be58bb63b27a70a051b48f6`  
		Last Modified: Mon, 02 Jan 2023 17:58:48 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7c5163e2376c441e8245e892ffe507da5d8861f7e0c8bda9ea40dad5c32c23b9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41131248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c219ad30945e297c83eb7f43e991ebb61f42e1db5740d050c1ad055796b68b64`
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
# Mon, 02 Jan 2023 17:40:37 GMT
ENV EGGDROP_SHA256=caafc1ad001e2e77793dca37998cb94d88efadb4ec9c3de44c1004b04f15aa6e
# Mon, 02 Jan 2023 17:40:37 GMT
ENV EGGDROP_COMMIT=2a6a36888f5aa2204d84a9e6282d35e5421c2c8a
# Mon, 02 Jan 2023 17:40:38 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 02 Jan 2023 17:44:12 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 02 Jan 2023 17:44:12 GMT
ENV NICK=
# Mon, 02 Jan 2023 17:44:13 GMT
ENV SERVER=
# Mon, 02 Jan 2023 17:44:13 GMT
ENV LISTEN=3333
# Mon, 02 Jan 2023 17:44:13 GMT
ENV OWNER=
# Mon, 02 Jan 2023 17:44:13 GMT
ENV USERFILE=eggdrop.user
# Mon, 02 Jan 2023 17:44:13 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 02 Jan 2023 17:44:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 02 Jan 2023 17:44:13 GMT
EXPOSE 3333
# Mon, 02 Jan 2023 17:44:13 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Mon, 02 Jan 2023 17:44:13 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 02 Jan 2023 17:44:13 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 02 Jan 2023 17:44:13 GMT
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
	-	`sha256:4454707cf8910a8f297397f40a7d87d9ebecc3a998ac68d054804e72b4e0a3ff`  
		Last Modified: Mon, 02 Jan 2023 17:44:40 GMT  
		Size: 1.1 MB (1087920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac63334a6e5c826bb67938acca0628ba7514b71eda84faa0580da7b94b491988`  
		Last Modified: Mon, 02 Jan 2023 17:44:44 GMT  
		Size: 37.3 MB (37309889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0994698876ca09d27dad78403094b9ea7811b6db5d18a179a0dfef3067f05a6`  
		Last Modified: Mon, 02 Jan 2023 17:44:39 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4df2cee2d2c12b7f28793df4e99ecf31324df19b07fd2b230b795208b56dd`  
		Last Modified: Mon, 02 Jan 2023 17:44:39 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:553f9f680e0f23ce7305e9e6f0df4742f6de01be1ea0c6b0578c7e5c01d754de
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
$ docker pull eggdrop@sha256:b380ac1a9a797f825411f8ca4ee8f3b97d727e3509fe406083878cd326778847
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8336614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d4bb15e44111516a55890b867a07bdcb783017d29e8439099a4074b95c6508`
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
# Thu, 15 Dec 2022 17:55:19 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 15 Dec 2022 17:55:19 GMT
ENV NICK=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV SERVER=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV LISTEN=3333
# Thu, 15 Dec 2022 17:55:19 GMT
ENV OWNER=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 15 Dec 2022 17:55:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 15 Dec 2022 17:55:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 15 Dec 2022 17:55:20 GMT
EXPOSE 3333
# Thu, 15 Dec 2022 17:55:20 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 15 Dec 2022 17:55:20 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 15 Dec 2022 17:55:20 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 15 Dec 2022 17:55:20 GMT
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
	-	`sha256:977bd0f129212a2f63565b44f77bf6dbc0cedb50e7c5d54bcc50e304d02ed9cc`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 3.0 MB (3027367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfb96772ab0bf8facffec93ff552abd5f3be28afac1064ee956f6e33292d3cc`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d37bbbdd0201657c2674731718169aa583ca30379a84283d77b7c9eda909af5`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 706.0 B  
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

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:553f9f680e0f23ce7305e9e6f0df4742f6de01be1ea0c6b0578c7e5c01d754de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

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

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b380ac1a9a797f825411f8ca4ee8f3b97d727e3509fe406083878cd326778847
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8336614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d4bb15e44111516a55890b867a07bdcb783017d29e8439099a4074b95c6508`
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
# Thu, 15 Dec 2022 17:55:19 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 15 Dec 2022 17:55:19 GMT
ENV NICK=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV SERVER=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV LISTEN=3333
# Thu, 15 Dec 2022 17:55:19 GMT
ENV OWNER=
# Thu, 15 Dec 2022 17:55:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 15 Dec 2022 17:55:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 15 Dec 2022 17:55:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 15 Dec 2022 17:55:20 GMT
EXPOSE 3333
# Thu, 15 Dec 2022 17:55:20 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 15 Dec 2022 17:55:20 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 15 Dec 2022 17:55:20 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 15 Dec 2022 17:55:20 GMT
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
	-	`sha256:977bd0f129212a2f63565b44f77bf6dbc0cedb50e7c5d54bcc50e304d02ed9cc`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 3.0 MB (3027367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfb96772ab0bf8facffec93ff552abd5f3be28afac1064ee956f6e33292d3cc`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d37bbbdd0201657c2674731718169aa583ca30379a84283d77b7c9eda909af5`  
		Last Modified: Thu, 15 Dec 2022 17:56:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

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
