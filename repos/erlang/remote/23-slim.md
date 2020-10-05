## `erlang:23-slim`

```console
$ docker pull erlang@sha256:bc3e7795564a32a19fcc762898001546064870e632e778dd9360fdd231b12c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:23-slim` - linux; amd64

```console
$ docker pull erlang@sha256:fa99fe3ad407a862a8dcbb82aee13041cbe728750b0ba6f8e6c657db20f50917
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111020607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4781fcc2d5f259a476a7616bf0150721daa7034858def652cf8b2534206f9f2`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Fri, 25 Sep 2020 21:33:22 GMT
ENV OTP_VERSION=23.1
# Fri, 25 Sep 2020 21:33:22 GMT
LABEL org.opencontainers.image.version=23.1
# Fri, 25 Sep 2020 21:44:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3591903503ea70be3ef1e42abc7a3e1f8af90f2c8989506bf9832175f091e6e5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 25 Sep 2020 21:44:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f58ff7330c82f1c83c5c5aee968266e34587554edbfec9bafc3b4a64d2d8ff`  
		Last Modified: Fri, 25 Sep 2020 22:02:04 GMT  
		Size: 60.6 MB (60624694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:bd0082f7fd63abe5d1ec1a4df721d9e5d0d24b1544e13dc0f24566c6fc3b6270
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102323557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa3396963b00626162f4c5314bff63e3c8af93dd127a0819404cf14008a1a32`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 10 Sep 2020 00:07:32 GMT
ADD file:340663c3add65bd8904ba51984e6080c6aa6d237bd845f4e0aa22626d31497b7 in / 
# Thu, 10 Sep 2020 00:07:35 GMT
CMD ["bash"]
# Mon, 05 Oct 2020 19:11:34 GMT
ENV OTP_VERSION=23.1.1
# Mon, 05 Oct 2020 19:11:35 GMT
LABEL org.opencontainers.image.version=23.1.1
# Mon, 05 Oct 2020 19:18:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8094484d94bce21d76f3a6c6137098839e7bc121e170c08b472f980296684ac9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 05 Oct 2020 19:18:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7d9beb74056b685831827b5f21351f021873d8ba1a1170b378e5edf5f46d114e`  
		Last Modified: Thu, 10 Sep 2020 00:17:29 GMT  
		Size: 45.9 MB (45869299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da795b4dcd79c0b1144dd95457377a318a2542f75fd775b10727d6eedfb0825a`  
		Last Modified: Mon, 05 Oct 2020 20:14:32 GMT  
		Size: 56.5 MB (56454258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:12490717ff55b6422164a19260deb93f358bf0417c3ca2402a8360f7015110cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106739213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd65f13ab5fadda6990c4df611c8b9753277c9a3e781130331fccc3c2d500cc`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:21 GMT
ADD file:c8c11e622b1b8a1e31f32e2457ff4d1314d5cd4a7ad22b3991ab9d0542db23fd in / 
# Wed, 09 Sep 2020 23:50:22 GMT
CMD ["bash"]
# Mon, 05 Oct 2020 18:51:03 GMT
ENV OTP_VERSION=23.1.1
# Mon, 05 Oct 2020 18:51:05 GMT
LABEL org.opencontainers.image.version=23.1.1
# Mon, 05 Oct 2020 18:57:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8094484d94bce21d76f3a6c6137098839e7bc121e170c08b472f980296684ac9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 05 Oct 2020 18:57:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d3a32671b6316bd11f4bf18cb034394ac94d2bb3bc6d09de388b19b06fb94b91`  
		Last Modified: Wed, 09 Sep 2020 23:58:45 GMT  
		Size: 49.2 MB (49175549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87691b81fc97f2be8107e6144437ee99fc0dc21198b84edef1da5525067df6ad`  
		Last Modified: Mon, 05 Oct 2020 19:53:36 GMT  
		Size: 57.6 MB (57563664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; 386

```console
$ docker pull erlang@sha256:c4ca64de37c3949dad7b82b083d8941474907a028e3927f91da68f7a1283d1a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111140043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd30f00b8ab78b7be4d315e2f9a45dba355b2c9102cb7dd503b68e7c9265047b`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Sep 2020 23:39:58 GMT
ADD file:39c4b1e1e5d34f52ad1f95b26bfbbf45f307b94a52d472a561496c440f96d8a2 in / 
# Wed, 09 Sep 2020 23:39:59 GMT
CMD ["bash"]
# Fri, 25 Sep 2020 22:02:45 GMT
ENV OTP_VERSION=23.1
# Fri, 25 Sep 2020 22:02:45 GMT
LABEL org.opencontainers.image.version=23.1
# Fri, 25 Sep 2020 22:13:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3591903503ea70be3ef1e42abc7a3e1f8af90f2c8989506bf9832175f091e6e5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 25 Sep 2020 22:13:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c89594b72f230eaccb7faa969906602c0f8e2667b7e30e66fe230243f1b5f1d0`  
		Last Modified: Wed, 09 Sep 2020 23:46:14 GMT  
		Size: 51.2 MB (51158853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5752ae5437aa60637b0f1fd3e736939535e11a41b2122104cb9fa6f6afb774bc`  
		Last Modified: Fri, 25 Sep 2020 22:27:05 GMT  
		Size: 60.0 MB (59981190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:0449df2055c9be46c6c918337d31a12f08efff4d637e1d3ff768ee5a42dfcf68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112622369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e83fda180d364a6d30908a0741dcb03a5083d10e0c8f87c98044ae337ea1b87`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 10 Sep 2020 01:04:56 GMT
ADD file:a2329a0372b3b40ca345795d86a78ab4cdaa3a1eeda3a5ece35a83881543db1a in / 
# Thu, 10 Sep 2020 01:05:18 GMT
CMD ["bash"]
# Fri, 25 Sep 2020 21:52:45 GMT
ENV OTP_VERSION=23.1
# Fri, 25 Sep 2020 21:53:04 GMT
LABEL org.opencontainers.image.version=23.1
# Fri, 25 Sep 2020 22:10:22 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3591903503ea70be3ef1e42abc7a3e1f8af90f2c8989506bf9832175f091e6e5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 25 Sep 2020 22:10:37 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:aff7fe9e9819c2b9d4338fae03bd06eb6784016bcf53b2eeab88c21e47dea428`  
		Last Modified: Thu, 10 Sep 2020 01:26:27 GMT  
		Size: 54.1 MB (54142644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3192dc05ee9b8bbeae16ebb907eb025ab15bd78c149c0599ee45a39b59869b`  
		Last Modified: Fri, 25 Sep 2020 22:26:53 GMT  
		Size: 58.5 MB (58479725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; s390x

```console
$ docker pull erlang@sha256:07c2e5030ca87cc74e209f4c798395fed25c544c5e770ef616802c7e739f4a61
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106563700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daff3e4f371ce7c26f84900be3d26bc5bea5df27c1c1339027728cd2e10cb181`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Sep 2020 23:42:11 GMT
ADD file:67eedff26215ed3c8100b93d0201c563ec8efe2af7bdfff5c7717037f95057af in / 
# Wed, 09 Sep 2020 23:42:15 GMT
CMD ["bash"]
# Mon, 05 Oct 2020 18:48:35 GMT
ENV OTP_VERSION=23.1.1
# Mon, 05 Oct 2020 18:48:35 GMT
LABEL org.opencontainers.image.version=23.1.1
# Mon, 05 Oct 2020 18:52:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8094484d94bce21d76f3a6c6137098839e7bc121e170c08b472f980296684ac9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 05 Oct 2020 18:52:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4c594945c9b37f16bdb296d1c06754e5bbcc3c28a736d7aa6091f61a081b3cfb`  
		Last Modified: Wed, 09 Sep 2020 23:46:12 GMT  
		Size: 49.0 MB (48966294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf419e4064ddbdcd154880dd4f2261a5ea79a966759bd1e0729ce31e19395cd`  
		Last Modified: Mon, 05 Oct 2020 19:12:18 GMT  
		Size: 57.6 MB (57597406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
