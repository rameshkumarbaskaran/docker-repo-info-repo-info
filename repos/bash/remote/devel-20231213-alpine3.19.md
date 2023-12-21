## `bash:devel-20231213-alpine3.19`

```console
$ docker pull bash@sha256:1bb8da9b6f093c4d0250d195916bafd2d45fab123f80db8f66b6504b0441d5f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20231213-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:88f0d73f12aa9566a307451cf827e0e7c5a1085768d7fe9d76048f111ad62b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6265951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf5dbeeb709e02b4853cd775d45ea6d43e6af7e81bc7d51eddffeb908811c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_COMMIT=9d51df7546eab80ea6baa4a83b2ae2178e8020c5
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_VERSION=devel-20231213
# Tue, 19 Dec 2023 05:20:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46017a18de9392a51a8f96fb904944b1cca69041a0e4cd517b461def4bf6a338`  
		Last Modified: Wed, 20 Dec 2023 20:07:33 GMT  
		Size: 2.9 MB (2857134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b076c3820c3a22d27e35086148793cfd3fbfe8eddfd47c0953e38fdc789d0`  
		Last Modified: Wed, 20 Dec 2023 20:07:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20231213-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:9cab831779842b52d2a025c37129775b5fbcb698764ffad9aef6f7ef49c56f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 KB (114056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fcba1ee35fc29a426300ca51711f2ddc3b3c8593519d6fded3af52c7cca4fe`

```dockerfile
```

-	Layers:
	-	`sha256:e9aec4e33629a406ee5c6ff80f8f9c2c1a72c0c82a36faabad80df560027441d`  
		Last Modified: Wed, 20 Dec 2023 20:07:33 GMT  
		Size: 97.7 KB (97732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7bb86c00b7c5aa2c275266129773d51539aa8983ea36ddbba5326b22f9f8c45`  
		Last Modified: Wed, 20 Dec 2023 20:07:33 GMT  
		Size: 16.3 KB (16324 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20231213-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:dfb35810a99a94535d116a00edb13857b71b4d4d98c6ade78ea039d56f57c0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bab6cecc4fb1706fc66f7863a1b6578099b8db89873db4c5ebcf91569c5d3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_COMMIT=9d51df7546eab80ea6baa4a83b2ae2178e8020c5
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_VERSION=devel-20231213
# Tue, 19 Dec 2023 05:20:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42920852a9944b8a65eadc14d4693f7e2025286de046358322d7b8f0eaaa75d`  
		Last Modified: Wed, 20 Dec 2023 21:24:10 GMT  
		Size: 2.8 MB (2805277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31d3e90a6e258a647a7250e5263435b4d9086b69f1eefff0a7b40159db41289`  
		Last Modified: Wed, 20 Dec 2023 21:24:10 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20231213-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:ff8f25bceb6bf99bae688eb7bff193bccde4a81b4d360f0ca094a5b470f9ed80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (16013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc60021666e67244367296337846208c0b3adfde679b72dbf79c30b47c74b936`

```dockerfile
```

-	Layers:
	-	`sha256:352260a116518f11ea328548639cc9606f93ac48baccb6c339029683b3fe2e07`  
		Last Modified: Wed, 20 Dec 2023 21:24:10 GMT  
		Size: 16.0 KB (16013 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20231213-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:10bbdb1f61f9c4c94123d1338342d8f6f532851bd701f1fff41ccbff72b76bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571efdb847e89676b5758e574b024d1ae93c091ee720e472e10a03dec0fee3a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_COMMIT=9d51df7546eab80ea6baa4a83b2ae2178e8020c5
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_VERSION=devel-20231213
# Tue, 19 Dec 2023 05:20:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3c1cf22236ad1d9f9d39f925a77d305163b10ee2a2ed7b8e9d331f097b282c`  
		Last Modified: Wed, 20 Dec 2023 21:52:38 GMT  
		Size: 2.8 MB (2752561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5782f24b13292e734cb6110e51944f8658ed5319008f5d062c504335666862`  
		Last Modified: Wed, 20 Dec 2023 21:52:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20231213-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:dae5f9795c39448d842baf2f707262e94f1356165affc9dabca582949659d4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (113996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e574ee4646fe3b2d5d3edb8fc74f5e90f2e72e93e2a0be9c38f0b97243f475b8`

```dockerfile
```

-	Layers:
	-	`sha256:1d7e646113d8d77543ad6882f1425cd10499c11e930e5d7371ec1998b95d05b5`  
		Last Modified: Wed, 20 Dec 2023 21:52:38 GMT  
		Size: 97.8 KB (97768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc2b2ec4f994a80d786ad97598908c6ecd6aec71cdabff221549023dc45d4ff`  
		Last Modified: Wed, 20 Dec 2023 21:52:38 GMT  
		Size: 16.2 KB (16228 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20231213-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:fd01846ce1cee86e50b8799da162173ca618a3475ac9124388b44c4322dab58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6307649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de2011c20ca16041a1d224fb0d552ff4de44127dfb1f276079d9dd8bbd63434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_COMMIT=9d51df7546eab80ea6baa4a83b2ae2178e8020c5
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_VERSION=devel-20231213
# Tue, 19 Dec 2023 05:20:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea2c840659fe33d3f4d4826fb6310bbcab6ca71cb4488f7efad8f89bcfe511d`  
		Last Modified: Wed, 20 Dec 2023 20:44:58 GMT  
		Size: 3.0 MB (2959524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9d4db339d787d161d61b7ef0bcfa1d4089bfbada93351a6ef927a89fe9a7ec`  
		Last Modified: Wed, 20 Dec 2023 20:44:58 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20231213-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:bc375ed2a2e7574616e94ba0ea6cb314e967a97541e53dde222f7561650ca6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653fac086131e111936fb4e772ccdf921a38ff7dced6429386abc5de31cda742`

```dockerfile
```

-	Layers:
	-	`sha256:3d6487dc7fe72338d2ac07dbba577f48e1fc778ee588f829a594468a1a6c539e`  
		Last Modified: Wed, 20 Dec 2023 20:44:58 GMT  
		Size: 97.7 KB (97743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7294625c28706995e9595ee0e564d83dbeea4254f4b275a8ff1f3c57a38a4489`  
		Last Modified: Wed, 20 Dec 2023 20:44:58 GMT  
		Size: 16.2 KB (16168 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20231213-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:2a42666e34520d2f6ae5b614342f83397f6a2c8d9190d151bd14aa6658ce6672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f28f68fb1bb432608656b913f06b1b4601acea78bd047abdedf5389470ba5f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_COMMIT=9d51df7546eab80ea6baa4a83b2ae2178e8020c5
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_VERSION=devel-20231213
# Tue, 19 Dec 2023 05:20:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db07675a791f3d0e3e9d3df22af8a04f429e58ae9bce221f4cdd37a8956a7179`  
		Last Modified: Wed, 20 Dec 2023 20:07:31 GMT  
		Size: 2.8 MB (2804614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2015e40ec43b60540867f0d92603a17f6ab390060f8e00927c695bdab52632`  
		Last Modified: Wed, 20 Dec 2023 20:07:31 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20231213-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:30212850642acfdc66558c58114920a17605eca9166012f75cc8c569a5da2868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0038dc66be84c0e9a00cec6f8c1501e67d8ba92a3a34c660d4b9c448b945fc`

```dockerfile
```

-	Layers:
	-	`sha256:87fbe1490933945462a68555fbb1f55bf23965e6249cd855e2081496d0ea2360`  
		Last Modified: Wed, 20 Dec 2023 20:07:31 GMT  
		Size: 16.1 KB (16080 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20231213-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:f04f80e551f5e510ea63d107aaff80bd640d973355f147c2784556d4d34799fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6488912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e857f72eae8a93718a7e943237ee859cba77b79d1df3d23c45291906113d36a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_COMMIT=9d51df7546eab80ea6baa4a83b2ae2178e8020c5
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_VERSION=devel-20231213
# Tue, 19 Dec 2023 05:20:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cf50cdc78bdb9daf84c3d7f04c6abd9c9aaf7e41952e2f88454e4ef83de08`  
		Last Modified: Wed, 20 Dec 2023 20:19:04 GMT  
		Size: 3.1 MB (3130341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c28f31f8276230ddf09c0b6356354a62ce4196d77789be19daad8e2ecdb4c3`  
		Last Modified: Wed, 20 Dec 2023 20:19:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20231213-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:fd5d5f3924dbe47cdd189b5eadf18cf9d3662ef42339fe33c40f50ba68c6e126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 KB (112326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bde99c5137125ef3f5d64536caa6728f7195046931e9ffbdb7060a079682732`

```dockerfile
```

-	Layers:
	-	`sha256:68e8430d5fda5ee4cb5b5762c8a387307bcdf7888a7bfa08a954a57a8e7a57b4`  
		Last Modified: Wed, 20 Dec 2023 20:19:03 GMT  
		Size: 96.1 KB (96130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a62ea60d4f7fe1f802a5c31fdc1fc7b3be3bf89aacaf9a52748c53cfbd47ab4a`  
		Last Modified: Wed, 20 Dec 2023 20:19:03 GMT  
		Size: 16.2 KB (16196 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20231213-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:29e3850859900274c3242defb976e988b3d8b453f547902396677fe9be4cca38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6199818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35ad4a6d6de9d4139f05a5a5812adc54bf2b56e1d860b8a8ac366733cfa16b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_COMMIT=9d51df7546eab80ea6baa4a83b2ae2178e8020c5
# Tue, 19 Dec 2023 05:20:24 GMT
ENV _BASH_VERSION=devel-20231213
# Tue, 19 Dec 2023 05:20:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 05:20:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 05:20:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba1d06684b9372541c9e79f71a730d817186fd5976974f1d333ad236745246`  
		Last Modified: Wed, 20 Dec 2023 20:37:49 GMT  
		Size: 3.0 MB (2957155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c1a8c0cc1038c78ce893633e77a4dccdecc398509f07792d2da973d178512d`  
		Last Modified: Wed, 20 Dec 2023 20:37:49 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20231213-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:afbd127024756a91aa590fb2ec655b70ede31de425422e16b5fee8152a69e12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 KB (112254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cea8931310280b90407895fbb18d1d8c32919236c159e11d4c18266840f9eb`

```dockerfile
```

-	Layers:
	-	`sha256:e8fe103695418269996d622218f2189d5b3457368df5db486dc12e770f8a54f8`  
		Last Modified: Wed, 20 Dec 2023 20:37:49 GMT  
		Size: 96.1 KB (96096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067a3a291e95f1daba0dd375c4a08a8fbf7f14b5563eec20bd320b41e652bc24`  
		Last Modified: Wed, 20 Dec 2023 20:37:50 GMT  
		Size: 16.2 KB (16158 bytes)  
		MIME: application/vnd.in-toto+json
