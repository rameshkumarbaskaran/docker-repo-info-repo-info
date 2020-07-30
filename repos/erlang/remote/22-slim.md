## `erlang:22-slim`

```console
$ docker pull erlang@sha256:d3ff5b29e3e2047042a29a0f4a0254e5cb18111fd12f443988c78abf424b5f25
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
$ docker pull erlang@sha256:d71b83f11533741116cd5056dd522736641bc3f8ef1710057f3ec6b8b2177119
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109936468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f17a3aad03c936de8d60e4bad4a347d76206ae5af41f76ea2bcebd0b03887f`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 15:22:56 GMT
ENV OTP_VERSION=22.3.4.3
# Wed, 22 Jul 2020 15:22:56 GMT
LABEL org.opencontainers.image.version=22.3.4.3
# Wed, 22 Jul 2020 15:37:12 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="557376f7fef07fd7f08eedebcd23de8c921d7dfc9430e214d29a4726d92537d2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 22 Jul 2020 15:37:13 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4d5d9b542f49460d05c448a1f1fbab8a3181c15845cd2790ce50a9d6994602`  
		Last Modified: Wed, 22 Jul 2020 18:05:43 GMT  
		Size: 59.5 MB (59546143 bytes)  
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
$ docker pull erlang@sha256:e959e97a8cbd62fe0a15f2a5b521a4a57f3f7ecb3b49e52a2c1b20b5c913705a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105614000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27df5b2b12eae24a6e283c3dd791a6a5c67a8e2ead7f03826b8bf69265fc1a60`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 00:40:37 GMT
ADD file:14b8dca0bc0e6dae2f0bdb018a3a4e6d8d041abd03d118ae27cf7a72668f4970 in / 
# Wed, 22 Jul 2020 00:40:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:06:52 GMT
ENV OTP_VERSION=22.3.4.3
# Wed, 22 Jul 2020 02:06:53 GMT
LABEL org.opencontainers.image.version=22.3.4.3
# Wed, 22 Jul 2020 02:13:39 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="557376f7fef07fd7f08eedebcd23de8c921d7dfc9430e214d29a4726d92537d2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 22 Jul 2020 02:13:42 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e2b2cb832ad58353bcc4edbdd16023beb64ec7856b469d202975f8de836c6906`  
		Last Modified: Wed, 22 Jul 2020 00:47:20 GMT  
		Size: 49.2 MB (49168473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742003b5c3d93761aa88079de3b10da6cdc0c46be802d6eb5fa6499e2e700d5c`  
		Last Modified: Wed, 22 Jul 2020 03:49:09 GMT  
		Size: 56.4 MB (56445527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; 386

```console
$ docker pull erlang@sha256:72565ac56316f71a7a79e41e52492d85bdb39efe6a2036b7c72d6188723b37f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110034846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05844e6f7cca23816206c20b75626f0515162b5380fb11b39b1481b3b6dc245`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 02:08:55 GMT
ADD file:2f4b8d9ab41b6e158f5926883b6bffdab1757086d903f3f0244f75bafc2e4876 in / 
# Wed, 22 Jul 2020 02:08:56 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:46:01 GMT
ENV OTP_VERSION=22.3.4.3
# Wed, 22 Jul 2020 04:46:01 GMT
LABEL org.opencontainers.image.version=22.3.4.3
# Wed, 22 Jul 2020 05:07:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="557376f7fef07fd7f08eedebcd23de8c921d7dfc9430e214d29a4726d92537d2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:07:24 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:88151d2519867746e4945a0a06b45430b9ddc2ae4be7e7f927cc00e3f640290d`  
		Last Modified: Wed, 22 Jul 2020 02:15:24 GMT  
		Size: 51.2 MB (51157197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebf68f1d532c9fb45a6b45c9986964f26ab57d2291011a8fc49c39e9dcafab9`  
		Last Modified: Wed, 22 Jul 2020 07:52:01 GMT  
		Size: 58.9 MB (58877649 bytes)  
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
$ docker pull erlang@sha256:46e160023c24c54b94d88150883437efabcbb579502d42d4f55c8f29305472ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105456385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17573a73da2e487a3114f59358ffd1431f3e8be852bca4379900361ba94aaeb`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:24 GMT
ADD file:e5fcdcbbd996899922beac57e202b7e0895321e07263147e96c6e3b7b811d8a2 in / 
# Wed, 22 Jul 2020 00:42:26 GMT
CMD ["bash"]
# Thu, 30 Jul 2020 19:47:52 GMT
ENV OTP_VERSION=22.3.4.4
# Thu, 30 Jul 2020 19:47:53 GMT
LABEL org.opencontainers.image.version=22.3.4.4
# Thu, 30 Jul 2020 19:52:44 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8dd1f21eadf5973f3278a4035a629f538bfbe3664679b45fe1d94b65f2f4a716" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 30 Jul 2020 19:52:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7ecdd8436fd4d951f4ca002a2aa8b01d427a7c4b535083e3ef0792444053154d`  
		Last Modified: Wed, 22 Jul 2020 00:45:30 GMT  
		Size: 49.0 MB (48966422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1260c4637e89b53832f464627d283833624245008f4ffa6ce6d408902b78000f`  
		Last Modified: Thu, 30 Jul 2020 19:59:19 GMT  
		Size: 56.5 MB (56489963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
