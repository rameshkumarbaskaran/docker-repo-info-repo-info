## `unit:go1.21`

```console
$ docker pull unit@sha256:113564850a91a2c2a418c8815cd4f8138990e60e4fedcaa96a4628232f252bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `unit:go1.21` - linux; amd64

```console
$ docker pull unit@sha256:692230ea4e2206bc782aecc3b0fd435d47f1c959b51425862a66cd1da89ce427
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.9 MB (285880562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c3e11da52a254f3c9bbe3b3e5812491a536b4258701456c6edeed064d8763c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 18:51:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 18:51:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 18:51:46 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 19 Dec 2023 18:51:54 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.5.linux-mips64le.tar.gz'; 			sha256='0799ce6a33181d09d623551e108b8d48359ace39eef9dc935f3140618f844f12'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armhf' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		go version
# Tue, 19 Dec 2023 18:51:55 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 Dec 2023 18:51:55 GMT
ENV GOPATH=/go
# Tue, 19 Dec 2023 18:51:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 18:51:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 19 Dec 2023 18:51:56 GMT
WORKDIR /go
# Tue, 19 Dec 2023 23:58:26 GMT
LABEL org.opencontainers.image.title=Unit (go1.21)
# Tue, 19 Dec 2023 23:58:26 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 19 Dec 2023 23:58:26 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 19 Dec 2023 23:58:26 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 19 Dec 2023 23:58:26 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 19 Dec 2023 23:58:26 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 Dec 2023 23:58:26 GMT
LABEL org.opencontainers.image.version=1.31.1
# Tue, 19 Dec 2023 23:59:18 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Tue, 19 Dec 2023 23:59:18 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Tue, 19 Dec 2023 23:59:19 GMT
COPY multi:44b909b4ee0b15a0820a0f95f866a48ec9fbcb6e3c46d6d937842c09126ebe93 in /usr/share/unit/welcome/ 
# Tue, 19 Dec 2023 23:59:19 GMT
STOPSIGNAL SIGTERM
# Tue, 19 Dec 2023 23:59:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 23:59:19 GMT
EXPOSE 80
# Tue, 19 Dec 2023 23:59:19 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d278fc41a93b35689afe55f7bbeda81194c3ed9d7162d8adf2ed2af1e042ea`  
		Last Modified: Tue, 19 Dec 2023 04:42:32 GMT  
		Size: 54.6 MB (54595440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e75cdbd7a06f7dcf0e2c0d7c5949d141e3cf6880a29f9f85b2aeef46b56a48`  
		Last Modified: Tue, 19 Dec 2023 18:53:35 GMT  
		Size: 86.1 MB (86085949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0078b41bdffaba1210e718fd1a914b861f6213f803550d4b63b3b827005a972`  
		Last Modified: Tue, 19 Dec 2023 18:53:35 GMT  
		Size: 67.0 MB (66982571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ba0bd45bc25e70a50a40ba8ee00bdb77a43c33ed24b9386b35110434524ff4`  
		Last Modified: Tue, 19 Dec 2023 18:53:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d3fe5af8efd2af6730dc687e49b80eef7ef646d3a2f48a464a1dfc4f1da12b`  
		Last Modified: Wed, 20 Dec 2023 00:04:19 GMT  
		Size: 7.4 MB (7391540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a6296863f53ef562714bd949a3ecebf9ceec919aae6c384c35e791423081a9`  
		Last Modified: Wed, 20 Dec 2023 00:04:17 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd6b40bf551c155423ca0aaba61285b52502bcff36bc4b317c7acf362ad087a`  
		Last Modified: Wed, 20 Dec 2023 00:04:17 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `unit:go1.21` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:014307502e18b86305239571bf650810b50d8c8f110c1c5926cb564c483165ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (276966544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9dde930a93a8bd1e58f9905da2a2975474ca4539209b8de5007a1526f3c2ed`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:35:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 20:02:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 20:02:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 20:02:06 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 19 Dec 2023 20:02:13 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.5.linux-mips64le.tar.gz'; 			sha256='0799ce6a33181d09d623551e108b8d48359ace39eef9dc935f3140618f844f12'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armhf' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		go version
# Tue, 19 Dec 2023 20:02:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 19 Dec 2023 20:02:15 GMT
ENV GOPATH=/go
# Tue, 19 Dec 2023 20:02:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 20:02:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 19 Dec 2023 20:02:15 GMT
WORKDIR /go
# Tue, 19 Dec 2023 20:44:44 GMT
LABEL org.opencontainers.image.title=Unit (go1.21)
# Tue, 19 Dec 2023 20:44:44 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 19 Dec 2023 20:44:44 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 19 Dec 2023 20:44:44 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 19 Dec 2023 20:44:44 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 19 Dec 2023 20:44:44 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 Dec 2023 20:44:44 GMT
LABEL org.opencontainers.image.version=1.31.1
# Tue, 19 Dec 2023 20:45:24 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Tue, 19 Dec 2023 20:45:24 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Tue, 19 Dec 2023 20:45:24 GMT
COPY multi:44b909b4ee0b15a0820a0f95f866a48ec9fbcb6e3c46d6d937842c09126ebe93 in /usr/share/unit/welcome/ 
# Tue, 19 Dec 2023 20:45:24 GMT
STOPSIGNAL SIGTERM
# Tue, 19 Dec 2023 20:45:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 20:45:24 GMT
EXPOSE 80
# Tue, 19 Dec 2023 20:45:24 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010797996cc86cf2cf7495aebc22e5be7d18a10bde1e11562dbe5283c226c0e9`  
		Last Modified: Tue, 19 Dec 2023 11:43:17 GMT  
		Size: 15.8 MB (15750308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70092c2a6b382a0cc0bd2adeb187b94d74c8bcf2ceb6f33bb8e4e4e9c6561141`  
		Last Modified: Tue, 19 Dec 2023 11:43:31 GMT  
		Size: 54.7 MB (54699871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aea5ee0f94d038f071199297175350bfa92e575e220b1f772fbf67b942202c9`  
		Last Modified: Tue, 19 Dec 2023 20:03:39 GMT  
		Size: 81.5 MB (81486689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd16c867d3ac3e7ac5bbe44bc94fcbc0525d37487050eb5777fdee48265ebb21`  
		Last Modified: Tue, 19 Dec 2023 20:03:39 GMT  
		Size: 64.1 MB (64072171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47714dc42648e49a3f6b7ec7a307d492237fc794a8360aca866dd05139813ed`  
		Last Modified: Tue, 19 Dec 2023 20:03:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9ccaf05fe2fa1539f04cecdc7bba52c5a759f26e2737234fd9deceee324aaf`  
		Last Modified: Tue, 19 Dec 2023 20:51:53 GMT  
		Size: 7.2 MB (7246510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c76bb8518ea4e3f2a5ef6ea4010599ca310ecf8e738e5b28f53998bbce4fe7`  
		Last Modified: Tue, 19 Dec 2023 20:51:52 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfedafa5cbc58ffdf920a05e0c62d619f10a3a0a8fa8033a9c3e4aa090d241ea`  
		Last Modified: Tue, 19 Dec 2023 20:51:52 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
