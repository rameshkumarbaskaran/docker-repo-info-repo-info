## `erlang:slim`

```console
$ docker pull erlang@sha256:a0d25ff5146ffd1a7f78b907abced193434578873ccf0d7d703045582c216f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:aa3adf5b3fa6b01770f825fc896e197e388e53e2f031bf49612cfb9bf8f0bb39
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109864873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821c0f3472d196db453bf78a7b954caa1912e47cf249479fd854b996559864be`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 21:54:21 GMT
ENV OTP_VERSION=22.3.1
# Mon, 06 Apr 2020 21:54:21 GMT
LABEL org.opencontainers.image.version=22.3.1
# Mon, 06 Apr 2020 22:08:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="34677d4604b6357db03b6cf79226d9fc1bbdf0ecb5e7545f2fe7a834cec93a83" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 06 Apr 2020 22:08:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623b3c67700296552a5ae40aa71c124993ae80c81853a06b6aa976e9e28e42e4`  
		Last Modified: Mon, 06 Apr 2020 22:21:43 GMT  
		Size: 59.5 MB (59482832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:04ec5fbbb57ecba2dd892c9c79055d0a36ba80250c8b9bdf75caa414a284023f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101116155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6798a407e5e857152bdc917f7c7c459f593e1ba51d1c31aff949fbd38319618`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 01:47:44 GMT
ADD file:57841d22461f051368fcd3488aab2f2ce27ec7583af772026a228feeb5d00cd9 in / 
# Tue, 31 Mar 2020 01:47:47 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 21:09:53 GMT
ENV OTP_VERSION=22.3.1
# Mon, 06 Apr 2020 21:09:54 GMT
LABEL org.opencontainers.image.version=22.3.1
# Mon, 06 Apr 2020 21:16:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="34677d4604b6357db03b6cf79226d9fc1bbdf0ecb5e7545f2fe7a834cec93a83" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 06 Apr 2020 21:16:18 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a893843c75627d21c8a132a2b8559c62371e185dc82e30169102b547264b4f20`  
		Last Modified: Tue, 31 Mar 2020 01:56:02 GMT  
		Size: 45.9 MB (45862803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30267e4847db092b40ba5e382f19c4493cd861419d87623e78ee2968ae89a2dd`  
		Last Modified: Mon, 06 Apr 2020 21:26:52 GMT  
		Size: 55.3 MB (55253352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:59c3a1429e1ab95873489df16832bdcb70e6979e9e63834da5969d95a522ceb9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105569601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a292075657ac7e0980a32973d1840a3df3e6f188b22e003c356caaef239ee80`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:07 GMT
ADD file:d0df7ac13226f8d35c078941a20d8a465b09a4e226c5ca37709fa23599cd56dc in / 
# Tue, 31 Mar 2020 02:05:09 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 20:49:27 GMT
ENV OTP_VERSION=22.3.1
# Mon, 06 Apr 2020 20:49:28 GMT
LABEL org.opencontainers.image.version=22.3.1
# Mon, 06 Apr 2020 20:55:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="34677d4604b6357db03b6cf79226d9fc1bbdf0ecb5e7545f2fe7a834cec93a83" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 06 Apr 2020 20:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5767fbcc7692f25971758138978eed9bd3add831a79561cd58bf281e60a5159f`  
		Last Modified: Tue, 31 Mar 2020 02:11:54 GMT  
		Size: 49.2 MB (49169998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88761a7ab7ed99d67751d71860a97653608afb7099d43574d83942c1143a19`  
		Last Modified: Mon, 06 Apr 2020 21:07:43 GMT  
		Size: 56.4 MB (56399603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:63aa1a98ab381081b33ff2e676fea1c7ff67070fd142cd369e0719abebe7a510
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109992335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42a8a73e236d20601145bf5426f2d75c401cb8f23df3bd7ad3af1e81ef59b21`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:25 GMT
ADD file:3dbe042e711d452b61bbca02798da5695de980649d3fd51ae6983b2445eaa792 in / 
# Tue, 31 Mar 2020 00:39:25 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 20:54:36 GMT
ENV OTP_VERSION=22.3.1
# Mon, 06 Apr 2020 20:54:36 GMT
LABEL org.opencontainers.image.version=22.3.1
# Mon, 06 Apr 2020 21:09:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="34677d4604b6357db03b6cf79226d9fc1bbdf0ecb5e7545f2fe7a834cec93a83" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 06 Apr 2020 21:09:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:acd641cee0ec134334632eecb48cf0c487a224a27ad5661fcd7eed50b0a1ab34`  
		Last Modified: Tue, 31 Mar 2020 00:45:15 GMT  
		Size: 51.1 MB (51146119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9430882e52614e9e5ed0990501b78f185e8361763ac8695b38ae5cff3671db09`  
		Last Modified: Mon, 06 Apr 2020 21:28:30 GMT  
		Size: 58.8 MB (58846216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:66428088aaf95bddfec6a5a590bc72ff2c9be0328596a6a5a8e63fed64cba9ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111439260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbfe5af04e767428c55310dfeb49d721677a54b2816ba333bc38ea06cc9bb37`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 01:32:00 GMT
ADD file:ccb86d1c4380ce5c6d0f26560ca6d637d15f7a9dd5a3e56977bcf80edcac69ac in / 
# Tue, 31 Mar 2020 01:32:04 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 21:31:00 GMT
ENV OTP_VERSION=22.3.1
# Mon, 06 Apr 2020 21:31:03 GMT
LABEL org.opencontainers.image.version=22.3.1
# Mon, 06 Apr 2020 21:41:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="34677d4604b6357db03b6cf79226d9fc1bbdf0ecb5e7545f2fe7a834cec93a83" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 06 Apr 2020 21:41:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2ee2adf89ee904a62d0e8993a1c564c340ff8a0d3ae152066c13e15fbae902ea`  
		Last Modified: Tue, 31 Mar 2020 01:44:47 GMT  
		Size: 54.1 MB (54138582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec7d04bf980c7b48e3e1a8c9882ed2974e3e2354bdc04ca5db053af7d20783f`  
		Last Modified: Mon, 06 Apr 2020 21:51:30 GMT  
		Size: 57.3 MB (57300678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:d2f0b3856ec0ce2fe6fce212968d14de4e9209348c391b08e90b4b42cb5f8a6a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105385768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a4fcb571aa561bc4323338d98373cf6a675b31c0127a2e944601babd511677`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 01:08:46 GMT
ADD file:a2690e2e8794d163493c5a6daa8b6503432365b11e48372e175d855c28ec64db in / 
# Tue, 31 Mar 2020 01:08:49 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 20:56:39 GMT
ENV OTP_VERSION=22.3.1
# Mon, 06 Apr 2020 20:56:39 GMT
LABEL org.opencontainers.image.version=22.3.1
# Mon, 06 Apr 2020 21:00:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="34677d4604b6357db03b6cf79226d9fc1bbdf0ecb5e7545f2fe7a834cec93a83" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 06 Apr 2020 21:00:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e5611e94178b5632fbdf7d00655f2a077f35fbef849c9665429c154c52784cd2`  
		Last Modified: Tue, 31 Mar 2020 01:12:24 GMT  
		Size: 49.0 MB (48958144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a5a397adb2a093ec1239895324d23bb53936645098d605cdb8bda7683d13b8`  
		Last Modified: Mon, 06 Apr 2020 21:07:31 GMT  
		Size: 56.4 MB (56427624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
