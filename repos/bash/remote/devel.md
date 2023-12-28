## `bash:devel`

```console
$ docker pull bash@sha256:c9791f51cb06214c048e8b118a28af194351997ce494b0dcc1a6a442700d8130
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

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:bc3c0202579c38e5b37c9205b7b8c2d22b86685b5e3c2bf8d58e316f6468da33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6265813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9ff996ec5fc2ff1c921dae8c1e80a4620e7530229c417034d5cbc9fc25a630`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_COMMIT=aa2d23cfac90bebe2924ba075fef0a03fddd521d
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_VERSION=devel-20231219
# Tue, 26 Dec 2023 05:20:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f525946368f52f3b5ef959f2e2ddb978fa1d4e5e287ab3e3729e6cdc3c16e`  
		Last Modified: Wed, 27 Dec 2023 21:54:00 GMT  
		Size: 2.9 MB (2857000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f337f8ce82afb5e4c0700250cd676fcaef164f26584d72bddd8cd191a02816`  
		Last Modified: Wed, 27 Dec 2023 21:54:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3c5602f5a0e8b0624b017f0836490e4b50f96ddb897055d4c83b1c8f1ad923b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (114012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7ab8cdeb283b0e8930caa32474004c15b1ba8d9cd0078be0878184481c850`

```dockerfile
```

-	Layers:
	-	`sha256:32446115023967ffb04508ed3e70bd5f49b9aed766551b47bb67812d117e9101`  
		Last Modified: Wed, 27 Dec 2023 21:54:00 GMT  
		Size: 97.7 KB (97732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41359366dc92143029bac0253aa7f8b6154d08035de76711e534a0bdc047d778`  
		Last Modified: Wed, 27 Dec 2023 21:54:01 GMT  
		Size: 16.3 KB (16280 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:6481a7780ae8f189d6fa30442012e9601f7a99d184159846ab7e18ff3be6166f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a044b4ee50fa9d177dc8bdceb715419efa4bd3904b76137ec714a6a66be2eb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_COMMIT=aa2d23cfac90bebe2924ba075fef0a03fddd521d
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_VERSION=devel-20231219
# Tue, 26 Dec 2023 05:20:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a94f52861e490ba889af5d3c57cfba2f6e9109772b90cddc33f5decca824b3`  
		Last Modified: Thu, 28 Dec 2023 02:43:54 GMT  
		Size: 2.8 MB (2805169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cf95374fb0987c87526d858462fa63b3775fc98ec9e41e8411f37418b33f18`  
		Last Modified: Thu, 28 Dec 2023 02:43:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:32daa70e5c8c8810124001b4ba80cfb1850ff35c44b5d4de3856a7645eab1830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18347bf4ff4fa3f2f287f9ed5c1c3aad4d146cef85df6060f582eeceac849d27`

```dockerfile
```

-	Layers:
	-	`sha256:f6d2566e37b15990ccc128d047b622a7960dd2061e703a24dac01155bf4b824c`  
		Last Modified: Thu, 28 Dec 2023 02:43:54 GMT  
		Size: 16.1 KB (16135 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:aa7921844947e43656a6b1c0a54f447bca9731cdad1f27d408b56c4c0b1ff4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c30625d711a661e8bef1c0c7e9b03387cea1c74c3e93286ea6bfa418e689bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_COMMIT=aa2d23cfac90bebe2924ba075fef0a03fddd521d
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_VERSION=devel-20231219
# Tue, 26 Dec 2023 05:20:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88af1017af7c933750fa7b474a0e81fefa5315d6cd10e2687b9d9e9940d91c4f`  
		Last Modified: Wed, 27 Dec 2023 22:14:57 GMT  
		Size: 2.8 MB (2752938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37e3eff961bd9cfc5e256c5e8610a54e5fcb25c4c35b5b8d421e2559f0f4f43`  
		Last Modified: Wed, 27 Dec 2023 22:14:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a1f87f8b749f19d14707365c734d360ded1a1b415f922169fdc4cd69d80731ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (113951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37fdfa5d87fd83fa193ffb9a7f60bcdaa2deac57e9dbba28757b50230d7c7f`

```dockerfile
```

-	Layers:
	-	`sha256:7b9e85fa1de3132988af4e8b1099b7947a843c381bb7b754bd66960f4bc4fdf9`  
		Last Modified: Wed, 27 Dec 2023 22:14:56 GMT  
		Size: 97.8 KB (97768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50e1ec82e027f5e5b6a8b954021fabb99c4666bb08d3a9129e659d663154c907`  
		Last Modified: Wed, 27 Dec 2023 22:14:56 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:5ecc8e051d08161d4312841854683f65f4b5c177f0bb5b23d898e284446e4c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6307792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9fdc46c077b1137c5679e22525d1513d74bfeffb24945f10d2d8e0efb67d6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_COMMIT=aa2d23cfac90bebe2924ba075fef0a03fddd521d
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_VERSION=devel-20231219
# Tue, 26 Dec 2023 05:20:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08067edc2dd6538a71c98d88e95827eed2d937d2856fca15bb256970300c6b`  
		Last Modified: Thu, 28 Dec 2023 01:16:49 GMT  
		Size: 3.0 MB (2959666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b688aea8721b178c5956d60c59550b929622feb5893a0ea715ebd7a1611922`  
		Last Modified: Thu, 28 Dec 2023 01:16:49 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7e1229602fcd2da4660bcea960d649a7fe818e19b4d94be7288cb096bf8d83ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2108daed2db64d40584a11121e2ff3fbca5410f9fa10fd947f10feda38e7a03d`

```dockerfile
```

-	Layers:
	-	`sha256:aec2ecfe3f84fa02e2f1ef828d6705a1b3d4e074a2c604b2d328825acb953884`  
		Last Modified: Thu, 28 Dec 2023 01:16:49 GMT  
		Size: 97.7 KB (97743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a16ad14d37abe735de08004d42f149693a0bebe204b4ead411101e64bed3eb39`  
		Last Modified: Thu, 28 Dec 2023 01:16:49 GMT  
		Size: 16.1 KB (16124 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:64512f628311af54d6c40d4f867e83dadd677e07122416ee7ada429c8882d9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6048955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4564c73a35f23deb6128203fcf728fa6142ae9940e0d456d57c81bdb22c8bf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_COMMIT=aa2d23cfac90bebe2924ba075fef0a03fddd521d
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_VERSION=devel-20231219
# Tue, 26 Dec 2023 05:20:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb831cae4dc680d5e795c2b283c9222bbe014465cbfa7a02206471f8c6511d36`  
		Last Modified: Wed, 27 Dec 2023 21:53:59 GMT  
		Size: 2.8 MB (2804507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d965541fe30ee10a8a1395336ec22351e1c4be7da1ff0391c3619f730ba479`  
		Last Modified: Wed, 27 Dec 2023 21:53:58 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:88c5481ddfcc8587495c5e83d504c283c792bddbcd2cf3c0bc20ecdefe2df0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (113958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e8a763bdfba854faedda956f067c01e0dbda1f00c3f8dcace5ff5b4720bcb8`

```dockerfile
```

-	Layers:
	-	`sha256:c0a136af84aac058a61a224d8fcd315057e5839f4e2eec433891f3d18050e969`  
		Last Modified: Wed, 27 Dec 2023 21:53:58 GMT  
		Size: 97.7 KB (97707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc315d882ff7642a855ab91b8d1a118ab1c8d032c382629ba63d760a3150f2cf`  
		Last Modified: Wed, 27 Dec 2023 21:53:58 GMT  
		Size: 16.3 KB (16251 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:518e2e9d1b6f7e32e6514fa055db26d2335eed8cf32d8055d2b53aa9f956d74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6488843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7683b643a3ba648bb8b629dd14fcfafe73650e58656a7de3daab6af3bacbc008`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_COMMIT=aa2d23cfac90bebe2924ba075fef0a03fddd521d
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_VERSION=devel-20231219
# Tue, 26 Dec 2023 05:20:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dd66607bd3d90ec9caf5e5b5a6bba41bfe800be0a699fc9cf5203767c8d0f8`  
		Last Modified: Wed, 27 Dec 2023 22:11:39 GMT  
		Size: 3.1 MB (3130274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a17ed45d46127a50b584128c81adaac40b778da3fb8f87432218c3c04410ce0`  
		Last Modified: Wed, 27 Dec 2023 22:11:38 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:fb4b61e2164dab0f0f447321e8a94a8fd17861786bb92c2aa1c544efee901106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 KB (112282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c49b9282dc11e4ef6e2b7382e843928f54edabb6019d788a002e6367556d69`

```dockerfile
```

-	Layers:
	-	`sha256:5c3c65d97025a6b3b47615a7b4e999939c7e158ed30cf918d28deb28708435d9`  
		Last Modified: Wed, 27 Dec 2023 22:11:39 GMT  
		Size: 96.1 KB (96130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1dc2f59c724957b0534b8f39d971f45f7696fd05695d81d6d16ee796cea948`  
		Last Modified: Wed, 27 Dec 2023 22:11:38 GMT  
		Size: 16.2 KB (16152 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:74790a4b94f9249399594b324901445da31ce049e1150e9137e427c52a02f9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6199891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8b73db17fa50db6985f183c1ae133aed88ce4cefae0cb2df86e4abc09c3de3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_COMMIT=aa2d23cfac90bebe2924ba075fef0a03fddd521d
# Tue, 26 Dec 2023 05:20:08 GMT
ENV _BASH_VERSION=devel-20231219
# Tue, 26 Dec 2023 05:20:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Dec 2023 05:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Dec 2023 05:20:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918f1cb64a7404c9137aa66d7661954420b26efa3c32f3701e091268b3cd15ee`  
		Last Modified: Thu, 28 Dec 2023 00:00:29 GMT  
		Size: 3.0 MB (2957221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d924b43efe563d6159e4367e27b7e93e8ebb441900111acfd611a459a0a701`  
		Last Modified: Thu, 28 Dec 2023 00:00:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:bb9326ad29d8ba3971dddb2f2a89f6d59bdaa85147ef85bbc0b55a26a98d3e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 KB (112210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d473fd1830943194eded78037de92366c96a41f3609a91230a882667c70b9206`

```dockerfile
```

-	Layers:
	-	`sha256:2e824081177fbcccfcc3dc2abffbb76a8c4dc3fef8112b743c1753105f546817`  
		Last Modified: Thu, 28 Dec 2023 00:00:29 GMT  
		Size: 96.1 KB (96096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c773a58fe91c9136dbbf53122d91311a81615e6c6b6acdf3198e02c5d5054f`  
		Last Modified: Thu, 28 Dec 2023 00:00:29 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json
