## `erlang:latest`

```console
$ docker pull erlang@sha256:f9ee7e6df6c65a633a1b5e8691ec8787021d57f16a598025a84c05c43e558641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `erlang:latest` - linux; amd64

```console
$ docker pull erlang@sha256:4ceb0c90e6dcb8ebef851628c4ebe87c96a84ca13c86721d19245c7820d1110f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563297783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8350ad93fe31cfc1e44ff91ae0d97cffda988a5ba9f108f1032f0d6645d4a07b`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:18 GMT
ADD file:ff01c6dedb67cf22e9b0735e099b9b6367770c4880941862cc7ec0e979b4118b in / 
# Tue, 13 Sep 2022 00:56:19 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:43:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 03:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:44:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:21:29 GMT
ENV OTP_VERSION=25.1 REBAR3_VERSION=3.19.0
# Wed, 21 Sep 2022 18:21:29 GMT
LABEL org.opencontainers.image.version=25.1
# Wed, 21 Sep 2022 18:28:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e00b2e02350688ee4ac83c41ec25c210774fe73b7f806860c46b185457ae135e" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:28:53 GMT
CMD ["erl"]
# Wed, 21 Sep 2022 18:28:54 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 21 Sep 2022 18:28:57 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 21 Sep 2022 18:29:12 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:23858da423a6737f0467fab0014e5b53009ea7405d575636af0c3f100bbb2f10`  
		Last Modified: Tue, 13 Sep 2022 01:00:00 GMT  
		Size: 55.0 MB (55029732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326f452ade5c33097eba4ba88a24bd77a93a3d994d4dc39b936482655e664857`  
		Last Modified: Tue, 13 Sep 2022 03:50:03 GMT  
		Size: 5.2 MB (5163200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42821cd14fb31c4aa253203e7f8e34fc3b15d69ce370f1223fbbe4252a64202`  
		Last Modified: Tue, 13 Sep 2022 03:50:03 GMT  
		Size: 10.9 MB (10876384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8471b75885efc7790a16be5328e3b368567b76a60fc3feabd6869c15e175ee05`  
		Last Modified: Tue, 13 Sep 2022 03:50:26 GMT  
		Size: 54.6 MB (54584419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffa7aaef4041744c03222b6b241a78a3b4ab9e8a8b99fb633a1f14b42f8bc56`  
		Last Modified: Tue, 13 Sep 2022 03:51:05 GMT  
		Size: 196.8 MB (196849089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a69dc84f2c71a6767b37a54d632646d1a7ea571ff1adc3ca9c4435ee34e1f4`  
		Last Modified: Wed, 21 Sep 2022 18:41:26 GMT  
		Size: 239.6 MB (239608043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b923df1517e1448db38ebbb6e3bc605c588696265d27ae29bd78dc9facc42bce`  
		Last Modified: Wed, 21 Sep 2022 18:40:57 GMT  
		Size: 198.6 KB (198623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c459a7da030957288dcd8af585352dd76c6cb6d35975f0726c2c6f2b3faf35e`  
		Last Modified: Wed, 21 Sep 2022 18:40:57 GMT  
		Size: 988.3 KB (988293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; arm variant v5

```console
$ docker pull erlang@sha256:9ed54b349035a8ed8142ad57e69903b09f3ce7d2bbe589f45caf353c7099f27b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511376859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35d3518d435c4e5b078315169af7dbee994c9e03789971c51724d25a61bbdd6`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Sep 2022 00:53:03 GMT
ADD file:ad560226d0aa0be51fbe1d98a8877aeb30110956b3a7c0f849a4331e99477ee4 in / 
# Tue, 13 Sep 2022 00:53:04 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:24:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:24:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 01:25:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:26:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 17:48:18 GMT
ENV OTP_VERSION=25.1 REBAR3_VERSION=3.19.0
# Wed, 21 Sep 2022 17:48:18 GMT
LABEL org.opencontainers.image.version=25.1
# Wed, 21 Sep 2022 18:06:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e00b2e02350688ee4ac83c41ec25c210774fe73b7f806860c46b185457ae135e" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:06:11 GMT
CMD ["erl"]
# Wed, 21 Sep 2022 18:06:11 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 21 Sep 2022 18:06:16 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 21 Sep 2022 18:06:57 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:f33103174415e8d15c8ebada62aae8327ecba6afa6035819128965eb1a64966e`  
		Last Modified: Tue, 13 Sep 2022 01:00:25 GMT  
		Size: 52.5 MB (52532200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74e3dd9c2e4e29e0f4df5b3d5a6bb6b72260bbd689082c1a14fa9f93bb7356c`  
		Last Modified: Tue, 13 Sep 2022 01:31:25 GMT  
		Size: 5.1 MB (5070938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ac23bd65f92366f98c6b75e0e91d6a10949d9f11f5c82875829dcc719266d2`  
		Last Modified: Tue, 13 Sep 2022 01:31:25 GMT  
		Size: 10.6 MB (10573721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88b67ca98f8f48ca0cdb936b58bba7b8133804ce01e0e8b3f6b7c9894f01ed5`  
		Last Modified: Tue, 13 Sep 2022 01:31:54 GMT  
		Size: 52.3 MB (52321510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453689f1385dde9166ee34ee9749cb1a1efa6f0c560b192dac4a0d47524eff54`  
		Last Modified: Tue, 13 Sep 2022 01:32:50 GMT  
		Size: 175.0 MB (175023501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f8fafc9bb665cf26430edfedc26d60ab45d38826c73e91e2c3c4cb3dcb8198`  
		Last Modified: Wed, 21 Sep 2022 18:23:30 GMT  
		Size: 214.7 MB (214668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2212b26aa0e36a95c64d1b6ef01c7d6197d1f8f19d49b9423ec055b09dfd16`  
		Last Modified: Wed, 21 Sep 2022 18:22:40 GMT  
		Size: 198.6 KB (198593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8813e73f2200246174c4911cf61b7041002dc734410621fd23b9e8b068fdcc0`  
		Last Modified: Wed, 21 Sep 2022 18:22:40 GMT  
		Size: 988.3 KB (988297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; arm variant v7

```console
$ docker pull erlang@sha256:5698e20139faa765394ea5a42b85e997e599eb422350785f97f3d4669594d4e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.3 MB (494277032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3285213cfb14c6f51f6470aa24b6604734499176c622fef66fb18a4a3305f184`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:17 GMT
ADD file:c60a3ffee6188f27e9b642109e01c6145bdbb8d4fc17475a2711795799597766 in / 
# Tue, 13 Sep 2022 03:42:18 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:31:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 07:32:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:33:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 17:57:40 GMT
ENV OTP_VERSION=25.1 REBAR3_VERSION=3.19.0
# Wed, 21 Sep 2022 17:57:40 GMT
LABEL org.opencontainers.image.version=25.1
# Wed, 21 Sep 2022 18:19:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e00b2e02350688ee4ac83c41ec25c210774fe73b7f806860c46b185457ae135e" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:19:57 GMT
CMD ["erl"]
# Wed, 21 Sep 2022 18:19:57 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 21 Sep 2022 18:20:02 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 21 Sep 2022 18:20:40 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:c0b863d4b31f0197ba7a7b6995cafb984dfbe6a0dcdedf88f2ce4a2f2c70b2cd`  
		Last Modified: Tue, 13 Sep 2022 03:49:09 GMT  
		Size: 50.2 MB (50195605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8418b877b4075c62cc53eb0d02b6b19d0d930a8e54ef2875bff8e9a948025c2a`  
		Last Modified: Tue, 13 Sep 2022 07:43:57 GMT  
		Size: 4.9 MB (4931269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d43cbe35130a47e93c66cb18df3b645f264e50e2d44ba95531a11148d4029`  
		Last Modified: Tue, 13 Sep 2022 07:43:57 GMT  
		Size: 10.2 MB (10217819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac653e751f5deb6b91cd5e0f6350d506b388ed88b8246ad86a39359c8a1a649d`  
		Last Modified: Tue, 13 Sep 2022 07:44:27 GMT  
		Size: 50.3 MB (50341630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ba417daab3d8668a82f95060a31e0f183fb308d21cccd0e223d0b3226ca360`  
		Last Modified: Tue, 13 Sep 2022 07:45:18 GMT  
		Size: 167.3 MB (167303683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a953f5add4a96a112860fd72a3c288753f8882362ba3b3b4a5ca87f42cee3e1c`  
		Last Modified: Wed, 21 Sep 2022 18:42:11 GMT  
		Size: 210.1 MB (210100125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb8e11ce048bcc50996942b94e51a153fc9122324114358804471dd2507c8e5`  
		Last Modified: Wed, 21 Sep 2022 18:41:43 GMT  
		Size: 198.6 KB (198604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3d3d13c24aaa035e300c0d6446f0edfb116baa7531960de090ed350231b164`  
		Last Modified: Wed, 21 Sep 2022 18:41:43 GMT  
		Size: 988.3 KB (988297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:b68b82ea3ab0fc79df191478cb911edd211512479b2d2a2ac676da3e523c3b28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.6 MB (540593958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb514c1abdf59ca37eac2c5a6b5fb99785f3dbb4268618d68cdf8de6dc89b45`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:41 GMT
ADD file:879fb0cd23107ac6f53581456074c7ff13c051aa262de3ca16ffa8475cf04dec in / 
# Tue, 13 Sep 2022 02:10:42 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:01:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 05:02:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:02:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 17:42:14 GMT
ENV OTP_VERSION=25.1 REBAR3_VERSION=3.19.0
# Wed, 21 Sep 2022 17:42:15 GMT
LABEL org.opencontainers.image.version=25.1
# Wed, 21 Sep 2022 17:48:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e00b2e02350688ee4ac83c41ec25c210774fe73b7f806860c46b185457ae135e" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Sep 2022 17:48:59 GMT
CMD ["erl"]
# Wed, 21 Sep 2022 17:49:01 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 21 Sep 2022 17:49:05 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 21 Sep 2022 17:49:20 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:10cff8997b4d4f243419e6bede830f1ac33f3d18c5200e5fb80e19333883ec2b`  
		Last Modified: Tue, 13 Sep 2022 02:15:49 GMT  
		Size: 53.7 MB (53691380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f2bf6f4deeb7ed2acd14f7997ec0a0cdf45b5b314051ddaab1911e22d997d`  
		Last Modified: Tue, 13 Sep 2022 05:09:57 GMT  
		Size: 5.1 MB (5148962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa25dbffbabb85498e5d2c2d270f81ca67f9679617c9611bf18faf6ed4a09a0`  
		Last Modified: Tue, 13 Sep 2022 05:09:57 GMT  
		Size: 10.7 MB (10657461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9360b3024e18f921a2fcec8614f617312c87ea1a31b5c94c9c643535bde9775`  
		Last Modified: Tue, 13 Sep 2022 05:10:20 GMT  
		Size: 54.7 MB (54681497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9175ba771bff9348347af555b31874fcf715783d5265e9282369fbcb0f5048c5`  
		Last Modified: Tue, 13 Sep 2022 05:11:00 GMT  
		Size: 189.7 MB (189722604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03226d5db897dbc02171e1ff72167dae955a3f6fbcb4250498949da88456ae8d`  
		Last Modified: Wed, 21 Sep 2022 18:02:01 GMT  
		Size: 225.5 MB (225505324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9db50f502b174d8f66f9f2baffd6d6b04df3848d74557defb0bfc543b9ab8f`  
		Last Modified: Wed, 21 Sep 2022 18:01:31 GMT  
		Size: 198.5 KB (198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b2ce66f74ebaf3c66989dd3422b4d81c6abeb9396e8f476f64b179693b3b72`  
		Last Modified: Wed, 21 Sep 2022 18:01:31 GMT  
		Size: 988.2 KB (988197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; 386

```console
$ docker pull erlang@sha256:69e7199ef4d4c0ebdfc0ca063ac5723c421e3ccbef9754649e3587d074584721
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (564009925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e464bab0e566289f20538954f6b0e29b475aafa4c73112c482e3994379592cb1`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:28 GMT
ADD file:7cd0a464573b537cf29f9a72bf3b895bfe96cce867ba3851402a98bca7272ca0 in / 
# Tue, 13 Sep 2022 01:39:28 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 04:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 04:49:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 04:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 04:50:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:38:39 GMT
ENV OTP_VERSION=25.1 REBAR3_VERSION=3.19.0
# Wed, 21 Sep 2022 18:38:40 GMT
LABEL org.opencontainers.image.version=25.1
# Wed, 21 Sep 2022 18:46:03 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e00b2e02350688ee4ac83c41ec25c210774fe73b7f806860c46b185457ae135e" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:46:05 GMT
CMD ["erl"]
# Wed, 21 Sep 2022 18:46:06 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 21 Sep 2022 18:46:12 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 21 Sep 2022 18:46:39 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:c56ebffcd7db97f938c62b9ad03478fefdde78fc8b85916da5d75054970df458`  
		Last Modified: Tue, 13 Sep 2022 01:44:50 GMT  
		Size: 56.0 MB (56009860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415b2926e999b0f68db69f91ece9d0bb97c79da80699d3a387e1ac5681d01b1f`  
		Last Modified: Tue, 13 Sep 2022 04:57:05 GMT  
		Size: 5.3 MB (5290983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25017ef00a9bb56c10606c65882cf1a863cf50ae6da48809e67da77aad2607cc`  
		Last Modified: Tue, 13 Sep 2022 04:57:05 GMT  
		Size: 11.0 MB (11032776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fcc67e3ad5b81078334e7e5fd41bc3736caa9c371ee3b620b5ba9dc06bb007`  
		Last Modified: Tue, 13 Sep 2022 04:57:28 GMT  
		Size: 55.9 MB (55923299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a006a23cb4da6c14d11fa73e6fce2101a8361be662bee80773a324bc9fc426`  
		Last Modified: Tue, 13 Sep 2022 04:58:05 GMT  
		Size: 199.8 MB (199755008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee626ea0087d0e6f1fdfc5f155de2a828390132048b58e4d475f7ff18cdb1973`  
		Last Modified: Wed, 21 Sep 2022 19:01:21 GMT  
		Size: 234.8 MB (234811243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23077fadaeb9adf8ee802f625bdbd0a5d02d1d5c4649c42e4ff905de23e13d34`  
		Last Modified: Wed, 21 Sep 2022 19:00:53 GMT  
		Size: 198.6 KB (198559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afd1a6776123fc1e32adcef655184a39fd2299585a13e3469deffa18b5349d2`  
		Last Modified: Wed, 21 Sep 2022 19:00:54 GMT  
		Size: 988.2 KB (988197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; mips64le

```console
$ docker pull erlang@sha256:bef022a8abd2842b379500f314282dfb2ccdb6845b0dc9dd0ef461cbc22686c1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.7 MB (515710080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74cf1169df5f441f4c5e9cec5c0b0ca4e17b4afd47ad4ddf1f60aabf7b27a7c`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Sep 2022 01:10:24 GMT
ADD file:01a7dd1465cd33040941b52c4ec3699247b2ecf8c53533b3a234445013452157 in / 
# Tue, 13 Sep 2022 01:10:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:50:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:50:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 01:52:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:57:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:07:32 GMT
ENV OTP_VERSION=25.1 REBAR3_VERSION=3.19.0
# Wed, 21 Sep 2022 18:07:38 GMT
LABEL org.opencontainers.image.version=25.1
# Wed, 21 Sep 2022 18:41:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e00b2e02350688ee4ac83c41ec25c210774fe73b7f806860c46b185457ae135e" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:41:47 GMT
CMD ["erl"]
# Wed, 21 Sep 2022 18:41:55 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 21 Sep 2022 18:42:19 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 21 Sep 2022 18:43:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:ec9a494c35bfb06348155378649b8055458795ad2d004f471b887021323b94f2`  
		Last Modified: Tue, 13 Sep 2022 01:18:07 GMT  
		Size: 53.3 MB (53251789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee02f93015f130da8dbe807a5b123a0f332fa75b55257f44d6a0f3c8fcc5da3`  
		Last Modified: Tue, 13 Sep 2022 02:05:49 GMT  
		Size: 5.1 MB (5123957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f6f6b0c2dd6acd42de4af694f71bf39f08a8daf7243600350b63f5c4b85787`  
		Last Modified: Tue, 13 Sep 2022 02:05:50 GMT  
		Size: 10.7 MB (10660929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a306342df3564e840a58fd4c03e8813c294edba4954f0791454308788492`  
		Last Modified: Tue, 13 Sep 2022 02:06:39 GMT  
		Size: 53.3 MB (53304679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd9b19e99fe0e23455f7bee784dfbba073d514c9d7b7b2d2fb287d2cb42cf2a`  
		Last Modified: Tue, 13 Sep 2022 02:08:43 GMT  
		Size: 179.0 MB (178963942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671117e5d658f45e8a21bc91070db6298d3be1a7b7acd79c0f6ba52ed525ecf5`  
		Last Modified: Wed, 21 Sep 2022 19:10:10 GMT  
		Size: 213.2 MB (213218037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5680bbf003594c6144f6192c0ad192f6bffca77d8fcfb03e8bf97dd0767a570c`  
		Last Modified: Wed, 21 Sep 2022 19:06:43 GMT  
		Size: 198.6 KB (198550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b639d5a2d8d7b69ba5b1f8ae1acc3954bc748f7ac0d76adc50a71390b7a0629`  
		Last Modified: Wed, 21 Sep 2022 19:06:43 GMT  
		Size: 988.2 KB (988197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; ppc64le

```console
$ docker pull erlang@sha256:285e0d2a9c972d6c5f53ef072241329eda211a9395abe467447ce9532c6af015
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.8 MB (561807268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2f7526ee4fb597deec40fbf3b78ab3c5586a831f2c022db9116c132637ad5a`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Sep 2022 02:07:34 GMT
ADD file:01cdcbf6300ec08ebb8bff41970509b38aff6d26164dea3fb476a6254e441e9b in / 
# Tue, 13 Sep 2022 02:07:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:14:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:14:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 05:14:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:16:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:16:33 GMT
ENV OTP_VERSION=25.1 REBAR3_VERSION=3.19.0
# Wed, 21 Sep 2022 18:16:33 GMT
LABEL org.opencontainers.image.version=25.1
# Wed, 21 Sep 2022 18:26:18 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e00b2e02350688ee4ac83c41ec25c210774fe73b7f806860c46b185457ae135e" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:26:25 GMT
CMD ["erl"]
# Wed, 21 Sep 2022 18:26:26 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 21 Sep 2022 18:26:35 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 21 Sep 2022 18:27:21 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:7d6144dab736564be3fb6a092ba7b12047adae858b56388b2c30f57e044d7565`  
		Last Modified: Tue, 13 Sep 2022 02:13:01 GMT  
		Size: 58.9 MB (58902594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7fa9a7ad3fd314802c655b3450a54569fcfa864dbfa0229721d8bc79f2a0b7`  
		Last Modified: Tue, 13 Sep 2022 05:24:55 GMT  
		Size: 5.4 MB (5412954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2712f6dbb2a2d0105245643b5cbd920b09c66574e06dba7618247607f8c8827b`  
		Last Modified: Tue, 13 Sep 2022 05:24:56 GMT  
		Size: 11.6 MB (11629060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eafe3c07d4e203ed51c77052a03bb7bf8728801864abea6cce0c4b15ec1e845`  
		Last Modified: Tue, 13 Sep 2022 05:25:28 GMT  
		Size: 58.9 MB (58866249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b447ed866efce197a7056139aac56bd68feee2b250a9ce18d4800c47d7fd60e`  
		Last Modified: Tue, 13 Sep 2022 05:26:29 GMT  
		Size: 196.2 MB (196194089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d4ae65d132faefbd54c94a34db59ee461bf0880a078ca92bb491ba65931735`  
		Last Modified: Wed, 21 Sep 2022 18:45:05 GMT  
		Size: 229.6 MB (229615413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5439fccdd08a53d941753b41d56c9282c9f7348ef7d61a8ee9cdd87a77833cc`  
		Last Modified: Wed, 21 Sep 2022 18:44:14 GMT  
		Size: 198.6 KB (198610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f75bffcd05e04540bda34a05b66dc33503294add131eef164866b352e200885`  
		Last Modified: Wed, 21 Sep 2022 18:44:14 GMT  
		Size: 988.3 KB (988299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; s390x

```console
$ docker pull erlang@sha256:5a1f3b8e7d55ef6e58d90769add0d8ca9a3dd6900da1a21a3da75f8f97a433e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.1 MB (525080296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de950cf2258a784d2c2a98b6c98907e9a9249594774e583f383bb196275f778`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Sep 2022 00:47:47 GMT
ADD file:2965b342d27ea25d073bb5f216362150cb8ec0e05df43fae8e4ee6251006d17d in / 
# Tue, 13 Sep 2022 00:47:50 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:25:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:25:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 01:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 01:27:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 17:41:36 GMT
ENV OTP_VERSION=25.1 REBAR3_VERSION=3.19.0
# Wed, 21 Sep 2022 17:41:36 GMT
LABEL org.opencontainers.image.version=25.1
# Wed, 21 Sep 2022 17:48:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="e00b2e02350688ee4ac83c41ec25c210774fe73b7f806860c46b185457ae135e" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0 			libwxgtk-webview3.0-gtk3-0v5' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk-webview3.0-gtk3-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Sep 2022 17:48:18 GMT
CMD ["erl"]
# Wed, 21 Sep 2022 17:48:18 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 21 Sep 2022 17:48:22 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 21 Sep 2022 17:48:40 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:cf58bfabf9fb5ab735277c32678e319fed106496e2f1070ac6bcf35a57d3870e`  
		Last Modified: Tue, 13 Sep 2022 00:52:18 GMT  
		Size: 53.3 MB (53264823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce515b66a74a291f416a7fb9b6e39594047957a72b0b2f38367f724790639590`  
		Last Modified: Tue, 13 Sep 2022 01:32:46 GMT  
		Size: 5.1 MB (5146951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bf6be09afafe08d5aecef2a5a139e863d43fb30c9c5dd6aed8fe8bee2c15c7`  
		Last Modified: Tue, 13 Sep 2022 01:32:46 GMT  
		Size: 10.8 MB (10765828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4c0b442ebbbf2a3574149920262648ea94715375d8db9298b73fd7de702ffc`  
		Last Modified: Tue, 13 Sep 2022 01:33:03 GMT  
		Size: 54.1 MB (54055046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7dcf62b7dcab5e57c828202a74ebfd9b811dd6d4b14740d1d77f87028f8e95`  
		Last Modified: Tue, 13 Sep 2022 01:33:30 GMT  
		Size: 172.8 MB (172824389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e8c8871c7bbb37657b2b3434beffe3c7188fc2524cfa5780d5f731480be849`  
		Last Modified: Wed, 21 Sep 2022 17:59:23 GMT  
		Size: 227.8 MB (227836370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f603d45f6f1dd8a7c53d0519fcb869820499dfd1fea0ef9f95bf8f10fe8c40`  
		Last Modified: Wed, 21 Sep 2022 17:58:58 GMT  
		Size: 198.6 KB (198601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98e65001cb1cc21f91aa95ca206b71d7bdfaf1dc25cb8e1d03ae972e46c5f19`  
		Last Modified: Wed, 21 Sep 2022 17:58:58 GMT  
		Size: 988.3 KB (988288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
