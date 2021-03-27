## `erlang:21-slim`

```console
$ docker pull erlang@sha256:715ecfda1f38a75cf57b5fe880ef934c463d82d4f2443029b53622c4ab0294ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `erlang:21-slim` - linux; amd64

```console
$ docker pull erlang@sha256:d267778c97f5cc86d3aae5e64f477437f8eace9f9a7c5d6857bd1ab608e9a690
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107727307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0018628ddd96ad427498d89003f727e419cc2e07c672dc1599e2963b90b99c`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 06:22:16 GMT
ENV OTP_VERSION=21.3.8.21
# Fri, 12 Mar 2021 06:22:16 GMT
LABEL org.opencontainers.image.version=21.3.8.21
# Fri, 12 Mar 2021 06:39:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47a0edb246c267f905564245ca3019e8491db5537dfa5441dc5031a4d091ea15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 12 Mar 2021 06:39:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4f683a17ee30ba26ddbad14cd192f3c9eceac9a35a20ee4939cd4e280117e9`  
		Last Modified: Fri, 12 Mar 2021 08:59:00 GMT  
		Size: 62.3 MB (62347091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:5ab8801385b1323351bfa423a7a84d1eb86fc70c8659525c0c1c813016f95fa9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99322878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe5f6fd3e07a2cb2ec0a2a8727d454185edebceb7eae65d9e98c1a1cd3c7324`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 13:38:23 GMT
ENV OTP_VERSION=21.3.8.21
# Fri, 12 Mar 2021 13:38:24 GMT
LABEL org.opencontainers.image.version=21.3.8.21
# Fri, 12 Mar 2021 13:44:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47a0edb246c267f905564245ca3019e8491db5537dfa5441dc5031a4d091ea15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 12 Mar 2021 13:44:39 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b7d6af41b941035d2020b1b7aec101d5dd34f3a4abe8c6ea90317250310520`  
		Last Modified: Fri, 12 Mar 2021 14:53:28 GMT  
		Size: 57.2 MB (57202690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:54a655dbb0d6d1ac7c4e62a8408d560ba06f4597f4d5df7c16a297b50d071282
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101592631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28f592afdeeff8a2551d679f5c2ad1351f70d295aefc18afc35e8ac65da1aed`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 04:30:19 GMT
ENV OTP_VERSION=21.3.8.21
# Fri, 12 Mar 2021 04:30:21 GMT
LABEL org.opencontainers.image.version=21.3.8.21
# Fri, 12 Mar 2021 04:37:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47a0edb246c267f905564245ca3019e8491db5537dfa5441dc5031a4d091ea15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 12 Mar 2021 04:37:03 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13191231dec3178e522c1b50f09b64288a04bae8b16b0555844da7d9089ced0`  
		Last Modified: Fri, 12 Mar 2021 05:41:35 GMT  
		Size: 58.4 MB (58415168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; 386

```console
$ docker pull erlang@sha256:a9e210f2e0b790e20911f0f9bd924db2127832311b6fe98d58a913b00afd2ebe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111457100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c16f778fd87ccc0d9c7eed3cf06bb2a67b5b3f4a6c4f837d1869ea965c00751`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 26 Mar 2021 13:55:57 GMT
ADD file:0a48869723941cb015604aec94e5f955449b86eca7c73ec978c3d1dcaf3517ba in / 
# Fri, 26 Mar 2021 13:55:58 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:37:58 GMT
ENV OTP_VERSION=21.3.8.21
# Fri, 26 Mar 2021 15:37:58 GMT
LABEL org.opencontainers.image.version=21.3.8.21
# Fri, 26 Mar 2021 15:52:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="47a0edb246c267f905564245ca3019e8491db5537dfa5441dc5031a4d091ea15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:52:18 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:01c2b0829d8abcf8cd9012766b99919fd21d4a2c1fae4d9312b5716bf40ba27e`  
		Last Modified: Fri, 26 Mar 2021 14:06:26 GMT  
		Size: 46.1 MB (46098430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a552f1575a34fedea5b908ee938cd93d870e7dfd311314eb7190941314a55d3d`  
		Last Modified: Fri, 26 Mar 2021 16:40:41 GMT  
		Size: 65.4 MB (65358670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
