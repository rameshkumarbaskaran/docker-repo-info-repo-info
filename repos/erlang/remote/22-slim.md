## `erlang:22-slim`

```console
$ docker pull erlang@sha256:95ac5294c4f02a3719dd2d03d6ac3c4cbe75eed6e305d01d025846c4cba0c0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:22-slim` - linux; amd64

```console
$ docker pull erlang@sha256:f38aa6fc5f8bb6e0e3e311001c834b0af6a781a85a943c65c385132f327e0f15
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109938787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffbbcec441a3b954fd4c5da03058c2ac78cb38937e0303b1db9d448d85101ec`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Thu, 30 Jul 2020 19:34:56 GMT
ENV OTP_VERSION=22.3.4.4
# Thu, 30 Jul 2020 19:34:56 GMT
LABEL org.opencontainers.image.version=22.3.4.4
# Thu, 30 Jul 2020 19:52:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8dd1f21eadf5973f3278a4035a629f538bfbe3664679b45fe1d94b65f2f4a716" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 30 Jul 2020 19:52:50 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78d654f2d92ffd8d4c30f2c3d09daebf4b1453a7f25835ad3905bc5bdefa6a8`  
		Last Modified: Thu, 30 Jul 2020 21:15:23 GMT  
		Size: 59.5 MB (59548462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:7ce84fdb2fb1a18ae8a0de32163035b3ee3407984d0da859c5a68b11aaa39d41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101189476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52702e9b141e1b4d3611aba7e45f82678edcd375a81aaffe37596210c6889c02`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 01:18:19 GMT
ADD file:38965defa0df84392a8ff562c2fa6393fe8d42f65f85591c07a581d694eebc30 in / 
# Wed, 22 Jul 2020 01:18:24 GMT
CMD ["bash"]
# Thu, 30 Jul 2020 19:08:10 GMT
ENV OTP_VERSION=22.3.4.4
# Thu, 30 Jul 2020 19:08:10 GMT
LABEL org.opencontainers.image.version=22.3.4.4
# Thu, 30 Jul 2020 19:14:35 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8dd1f21eadf5973f3278a4035a629f538bfbe3664679b45fe1d94b65f2f4a716" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 30 Jul 2020 19:14:37 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f890282b0ef00faf11d62374bcdfc54ca574d085127c66977d9a08ab80978a98`  
		Last Modified: Wed, 22 Jul 2020 01:40:13 GMT  
		Size: 45.9 MB (45868714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5009a51d8e32d8ffecea49cae856750f0b1d97ece13ae51c074377d87d37ae39`  
		Last Modified: Thu, 30 Jul 2020 19:47:29 GMT  
		Size: 55.3 MB (55320762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:0039994f2bd299d4ec4ee1292da89bcaff68f28e84d7780295900d798f7eab37
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105640300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c575675ce05d22a66e84827fb906bc0dc4838c5866d05bef1e5d672cc23d7e82`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 00:40:37 GMT
ADD file:14b8dca0bc0e6dae2f0bdb018a3a4e6d8d041abd03d118ae27cf7a72668f4970 in / 
# Wed, 22 Jul 2020 00:40:41 GMT
CMD ["bash"]
# Thu, 30 Jul 2020 19:55:06 GMT
ENV OTP_VERSION=22.3.4.4
# Thu, 30 Jul 2020 19:55:07 GMT
LABEL org.opencontainers.image.version=22.3.4.4
# Thu, 30 Jul 2020 20:04:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8dd1f21eadf5973f3278a4035a629f538bfbe3664679b45fe1d94b65f2f4a716" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 30 Jul 2020 20:04:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e2b2cb832ad58353bcc4edbdd16023beb64ec7856b469d202975f8de836c6906`  
		Last Modified: Wed, 22 Jul 2020 00:47:20 GMT  
		Size: 49.2 MB (49168473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d5a7053b65db187ed1c49d22061186447d891ab79fa9a7d7fb3ebe8b5da7`  
		Last Modified: Thu, 30 Jul 2020 20:39:01 GMT  
		Size: 56.5 MB (56471827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; 386

```console
$ docker pull erlang@sha256:9b7aac48455170dd399d6eceb740b2d3a78adc9875a9dc41b809fc1e61390874
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110076470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364ae38150d146bb4f13e87476bde04ba3326a8ccc29aff0853f5d5e2908745a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 02:08:55 GMT
ADD file:2f4b8d9ab41b6e158f5926883b6bffdab1757086d903f3f0244f75bafc2e4876 in / 
# Wed, 22 Jul 2020 02:08:56 GMT
CMD ["bash"]
# Thu, 30 Jul 2020 20:04:53 GMT
ENV OTP_VERSION=22.3.4.4
# Thu, 30 Jul 2020 20:04:53 GMT
LABEL org.opencontainers.image.version=22.3.4.4
# Thu, 30 Jul 2020 20:27:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8dd1f21eadf5973f3278a4035a629f538bfbe3664679b45fe1d94b65f2f4a716" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 30 Jul 2020 20:27:17 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:88151d2519867746e4945a0a06b45430b9ddc2ae4be7e7f927cc00e3f640290d`  
		Last Modified: Wed, 22 Jul 2020 02:15:24 GMT  
		Size: 51.2 MB (51157197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebdcd299476c8044e6c2784ad0bd022511dccd10658e4174d1889f158d3c1dc`  
		Last Modified: Thu, 30 Jul 2020 21:46:39 GMT  
		Size: 58.9 MB (58919273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:e7ae8ef92c318c360bd7e59271607358cdaf99e77c8fe3ea9ab2bbff8bc64c4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111511112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f124cab65dbe22176765353ae76d5c97b6262ff4e8e18772a615159c167993`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 02:15:14 GMT
ADD file:3e8bf6319c2535d9da6756a6f316eac0a488312c1297fdd54c9e064959e50da8 in / 
# Wed, 22 Jul 2020 02:15:27 GMT
CMD ["bash"]
# Thu, 30 Jul 2020 19:35:34 GMT
ENV OTP_VERSION=22.3.4.4
# Thu, 30 Jul 2020 19:35:36 GMT
LABEL org.opencontainers.image.version=22.3.4.4
# Thu, 30 Jul 2020 19:47:08 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8dd1f21eadf5973f3278a4035a629f538bfbe3664679b45fe1d94b65f2f4a716" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 30 Jul 2020 19:47:14 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1c8685784756ef2cf52bfd7aa4cf826bd407c500b8402bd2b5b799a2e734e133`  
		Last Modified: Wed, 22 Jul 2020 02:24:38 GMT  
		Size: 54.1 MB (54143905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4dd5a611d5d14fc605fc9c6c0ef98ddb19863a309132d5b04df4ab08ee2ecb`  
		Last Modified: Thu, 30 Jul 2020 19:56:50 GMT  
		Size: 57.4 MB (57367207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; s390x

```console
$ docker pull erlang@sha256:8dc251650ada47bbe635dd23121e437aeb749e801b4f102de26ecb120397e631
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107646674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1aa86dc6824978ce985900970c831f5468ba8a964e812da1e44fffd1ce69101`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:24 GMT
ADD file:e5fcdcbbd996899922beac57e202b7e0895321e07263147e96c6e3b7b811d8a2 in / 
# Wed, 22 Jul 2020 00:42:26 GMT
CMD ["bash"]
# Mon, 03 Aug 2020 20:52:40 GMT
ENV OTP_VERSION=22.3.4.5
# Mon, 03 Aug 2020 20:52:40 GMT
LABEL org.opencontainers.image.version=22.3.4.5
# Mon, 03 Aug 2020 20:58:48 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6117318970bf5d83d52aa1d782078f78803279f4a46a390adcbd29dc0bc617bc" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 03 Aug 2020 20:58:54 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7ecdd8436fd4d951f4ca002a2aa8b01d427a7c4b535083e3ef0792444053154d`  
		Last Modified: Wed, 22 Jul 2020 00:45:30 GMT  
		Size: 49.0 MB (48966422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677d6b10fc21757158f92cd7982b0ef804d9877b1bf5b1992a3c32606e607603`  
		Last Modified: Mon, 03 Aug 2020 21:06:58 GMT  
		Size: 58.7 MB (58680252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
