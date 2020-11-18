## `erlang:21-slim`

```console
$ docker pull erlang@sha256:91d437b45f81e1fffc888be52c02f4343be11f401f5eba3cd448a67b0345494a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `erlang:21-slim` - linux; amd64

```console
$ docker pull erlang@sha256:ae7fae3a6a357a86e123ca926404cd6381611fe156be910a0fbc7fe9e4f3401c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107694855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84e17112e2ce71695fe5f28b106bd57f592fc4983188cb55e734746b83a9fbe`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:35:56 GMT
ENV OTP_VERSION=21.3.8.18
# Tue, 17 Nov 2020 22:35:56 GMT
LABEL org.opencontainers.image.version=21.3.8.18
# Tue, 17 Nov 2020 22:54:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3481a47503e1ac0c0296970b460d1936ee0432600f685a216608e04b2f608367" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:54:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7919f5b7d60254cafc73c0d097b8ccffb72e0b6472957ece4dd5b378c5ca7cc1`  
		Last Modified: Tue, 17 Nov 2020 20:30:26 GMT  
		Size: 45.4 MB (45377037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd2ceb76d21eff38b13921d73aac989b4ff2080db3d8a56d4fa8c5b8ed5f62b`  
		Last Modified: Tue, 17 Nov 2020 23:52:38 GMT  
		Size: 62.3 MB (62317818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4d87a479feb5ea4f02fe4568850e01813fb5149e0c0c7fe0897df516e32189bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99235200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f149c52ac6f08a303c11f24db47f4a85784bfa8e6ec38b6d49ab2f23435cad86`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Oct 2020 01:04:04 GMT
ADD file:fb1dab6b0ac08f52870fca9435eedd2f707a3b8a5d28e5d1c2ff88e096f695ec in / 
# Tue, 13 Oct 2020 01:04:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 03:02:06 GMT
ENV OTP_VERSION=21.3.8.18
# Tue, 13 Oct 2020 03:02:07 GMT
LABEL org.opencontainers.image.version=21.3.8.18
# Tue, 13 Oct 2020 03:08:43 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3481a47503e1ac0c0296970b460d1936ee0432600f685a216608e04b2f608367" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:08:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1b636fdf37230c276ff1507a9f2b0067182f369cd669d1852bf5b9f5ba3a43bf`  
		Last Modified: Tue, 13 Oct 2020 01:12:25 GMT  
		Size: 42.1 MB (42111286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6080e58b16e53d5f2e28019188057be7d00bf0f13cf0e45a3109d5a3019913e8`  
		Last Modified: Tue, 13 Oct 2020 04:18:45 GMT  
		Size: 57.1 MB (57123914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:b8245eb37773f30abaad17c43b68adcf9dff4a1561c13ebd5c4356d00f29f95a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101513591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cf07ca0a8f7b36635c2077f2b223951fda2b5ed6c6cdbadd225c52a1366ba`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:49 GMT
ADD file:2752d391988f4ad7e086be863c36a83a3226e31e44ea816ca4c89d6a410727b1 in / 
# Tue, 13 Oct 2020 01:43:51 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 03:54:44 GMT
ENV OTP_VERSION=21.3.8.18
# Tue, 13 Oct 2020 03:54:46 GMT
LABEL org.opencontainers.image.version=21.3.8.18
# Tue, 13 Oct 2020 04:01:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3481a47503e1ac0c0296970b460d1936ee0432600f685a216608e04b2f608367" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 13 Oct 2020 04:01:58 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:19e4d0e7f8f2c5cb8a0a8d0e741e9e387c34bd673da69cdcc8e758a5c4dbc106`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 43.2 MB (43171543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4751927215b7a75d84596af57f96871f8125da5916653b96381cb487d0410`  
		Last Modified: Tue, 13 Oct 2020 05:11:14 GMT  
		Size: 58.3 MB (58342048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; 386

```console
$ docker pull erlang@sha256:9f21f1ad8a4fd188b661ab23328fa23020983a073a7cfa9f7dcd01d9b3d938ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111360679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3153e67b19d1ee6a1b606d5b7510db150183fd4ffc8db6e569b1c154ba1ce2d2`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Oct 2020 01:45:07 GMT
ADD file:2c53d7197ae361c4b9c751cf700f3d286a3cf5c77cf07d16756f36f61666bb40 in / 
# Tue, 13 Oct 2020 01:45:07 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:39:01 GMT
ENV OTP_VERSION=21.3.8.18
# Tue, 13 Oct 2020 04:39:01 GMT
LABEL org.opencontainers.image.version=21.3.8.18
# Tue, 13 Oct 2020 04:59:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3481a47503e1ac0c0296970b460d1936ee0432600f685a216608e04b2f608367" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 13 Oct 2020 04:59:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3e5030fa46456155e6836658abedeff054349492fdd554f0476a8dd26a0da3d9`  
		Last Modified: Tue, 13 Oct 2020 01:51:57 GMT  
		Size: 46.1 MB (46086868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98332cf0a7d505ed0cff1dc71cdf36c18bdb9f85bce96a13f94e9837668d39c8`  
		Last Modified: Tue, 13 Oct 2020 07:00:48 GMT  
		Size: 65.3 MB (65273811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
