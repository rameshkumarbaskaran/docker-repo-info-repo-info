## `bash:devel`

```console
$ docker pull bash@sha256:c386f72c3dbd32718c0573e5e448b14259737f1d8ac4bdafcf22073798b95576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:d7c8ee089a845f6e393a8b23cf49ea1d4b01bfc35e1099581b495965f09d116a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcbaa162e618d4c741b2e41728f1820cb1274fe5e112795cd2c0b75aa1cc587`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Mon, 18 May 2020 19:19:25 GMT
ENV _BASH_COMMIT=7bd086c2bf8bbbd066a46624448153cc0a3c5329
# Mon, 18 May 2020 19:19:25 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200515 snapshot
# Mon, 18 May 2020 19:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Mon, 18 May 2020 19:20:14 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Mon, 18 May 2020 19:20:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 19:20:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3595533e39faa460e01f327d316a651c449ea9fa754c4ba92e440b8c1329e9`  
		Last Modified: Mon, 18 May 2020 19:20:58 GMT  
		Size: 2.9 MB (2924800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c9e320c4b48223e7607b54702ff9f0034bfae5b82dbb65e97582f380f4310`  
		Last Modified: Mon, 18 May 2020 19:20:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:f7b33128c81019fd553fda27921de88c2f49ff9998f068446bcdcc0b44378cc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5435826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4893806017e7f0310222ffc1ecba25f46ead8a995d7db0d5b228ff29258e5ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2020 22:53:10 GMT
ENV _BASH_COMMIT=e76c732799615a5c51c64605454aaf492ebdd83d
# Wed, 20 May 2020 22:53:11 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200518 snapshot
# Wed, 20 May 2020 22:54:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Wed, 20 May 2020 22:54:19 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Wed, 20 May 2020 22:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2020 22:54:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a205a7bfacca4d53ddc53b7538328d16bbb4f4f308958ac8fedd9246d83cf`  
		Last Modified: Wed, 20 May 2020 22:55:25 GMT  
		Size: 2.8 MB (2815551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57df1440199cfb634b19a27f06dcc593451678e79e349e87cf17ebcb765176be`  
		Last Modified: Wed, 20 May 2020 22:55:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:e04c32e1a31c3e8879f06572df71f724f982f7c09c4fc95dd0614f46775103b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5182363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e25529f14be3b6114929f7f03e71fa002999a0077f743fe45252a4d1aadc96d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2020 23:19:37 GMT
ENV _BASH_COMMIT=e76c732799615a5c51c64605454aaf492ebdd83d
# Wed, 20 May 2020 23:19:38 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200518 snapshot
# Wed, 20 May 2020 23:21:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Wed, 20 May 2020 23:21:14 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Wed, 20 May 2020 23:21:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2020 23:21:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174f879dbb704c1fee2ad797ab2c8988e85844a3821d2e7e89b694f813826a1f`  
		Last Modified: Wed, 20 May 2020 23:22:58 GMT  
		Size: 2.8 MB (2759957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd732b0fe06885270576e827998ebdbbe0466462cdeeba592a3a37c21b424646`  
		Last Modified: Wed, 20 May 2020 23:22:57 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:129c896c9bd91797ea0e7bf9d6148110b36a94f80d7a057f9a8522b54476c389
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5648013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8d3ef806b1fd73bac1615ad910663384f0e1d6d0b71de539047b6e5cc8514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Mon, 18 May 2020 18:39:42 GMT
ENV _BASH_COMMIT=7bd086c2bf8bbbd066a46624448153cc0a3c5329
# Mon, 18 May 2020 18:39:43 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200515 snapshot
# Mon, 18 May 2020 18:40:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Mon, 18 May 2020 18:40:43 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Mon, 18 May 2020 18:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 18:40:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80ccb18e6f4d4c49acc95f8cc30752c1601d8c5540ac0b6754b606d9587b8d0`  
		Last Modified: Mon, 18 May 2020 18:41:57 GMT  
		Size: 2.9 MB (2923246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7450d532471347c4842762b3466299c24e67e677279e587d96b8abedbc3da6`  
		Last Modified: Mon, 18 May 2020 18:41:56 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:22ea359ed385f55729fb146b7ef197c12c11f4495c4eaae2168d0819315a2e5a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498f4fb74466d574414457ec3ef0242683ac69cb5154147f78462cbc27ba59dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Mon, 18 May 2020 18:38:20 GMT
ENV _BASH_COMMIT=7bd086c2bf8bbbd066a46624448153cc0a3c5329
# Mon, 18 May 2020 18:38:20 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200515 snapshot
# Mon, 18 May 2020 18:39:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Mon, 18 May 2020 18:39:22 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Mon, 18 May 2020 18:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 18:39:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196d58fe49847ef10e05cd7d319790e83305a1477315efbf9608279da3d337f3`  
		Last Modified: Mon, 18 May 2020 18:40:14 GMT  
		Size: 2.9 MB (2862992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad54c4e38aa482c24a3ec11390b7fe25d8b5c29b625d7d3b52af94444c1357ea`  
		Last Modified: Mon, 18 May 2020 18:40:13 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:cd0204f16ec4ef502b1e19e714b1007c90cfe3067b128bb90f63388bd9021c70
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5990777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b740a48bbae77efd937c71e30f50e61f36258c77dfbed284cdb22f3f86d9341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2020 01:24:53 GMT
ENV _BASH_COMMIT=7bd086c2bf8bbbd066a46624448153cc0a3c5329
# Tue, 19 May 2020 01:24:56 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200515 snapshot
# Tue, 19 May 2020 01:25:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Tue, 19 May 2020 01:25:52 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Tue, 19 May 2020 01:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2020 01:25:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a9b26916c1143343b28a838541ce16b90237cba8113ce3298f6e5df6a04922`  
		Last Modified: Tue, 19 May 2020 01:26:48 GMT  
		Size: 3.2 MB (3168590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2ccb40b1f9426af9980b651ccc73d6c1ad136fdf45e5c7e0a0b56adba9dcf8`  
		Last Modified: Tue, 19 May 2020 01:26:47 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:f5a71f6cad402d1b8430a7344a0942c84ca07f8a263be51b63842c0525d67dbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5498471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a059df106c9c8f59136c7d294c899493d9c0490574fc3b2471cb9af20e94e93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Mon, 18 May 2020 18:41:28 GMT
ENV _BASH_COMMIT=7bd086c2bf8bbbd066a46624448153cc0a3c5329
# Mon, 18 May 2020 18:41:28 GMT
ENV _BASH_COMMIT_DESC=commit bash-20200515 snapshot
# Mon, 18 May 2020 18:41:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version
# Mon, 18 May 2020 18:41:57 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Mon, 18 May 2020 18:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 18:41:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763add25d8c80719e3ec9d43e9844be160549c9c96f6906db9cc22c3355b6de`  
		Last Modified: Mon, 18 May 2020 18:42:56 GMT  
		Size: 2.9 MB (2915273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394c336f4f15b5992740c66aefb39dfff4b664ad2ffb5e3730ba64a797a5d47f`  
		Last Modified: Mon, 18 May 2020 18:42:56 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
