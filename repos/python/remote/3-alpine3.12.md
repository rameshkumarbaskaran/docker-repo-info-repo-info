## `python:3-alpine3.12`

```console
$ docker pull python@sha256:5e88b15a5a60927769b6b830202965d29cb0688e6e4198c071cb879d18f310cf
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

### `python:3-alpine3.12` - linux; amd64

```console
$ docker pull python@sha256:bac35a32f292ea6467fdd424f03507409a99f35c684d9b913ab4f240d7c63fa1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17330783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38d32ec75d25522e5211cfcfe4108bb771ebe428bdae58e9af6e05ae411e858`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:48:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 04:33:20 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 04:33:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 15 Apr 2021 04:51:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 15 Apr 2021 04:51:56 GMT
ENV PYTHON_VERSION=3.9.4
# Thu, 15 Apr 2021 04:59:56 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 15 Apr 2021 04:59:58 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 03 May 2021 22:13:54 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Mon, 03 May 2021 22:13:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Mon, 03 May 2021 22:13:55 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Mon, 03 May 2021 22:14:01 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 03 May 2021 22:14:01 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10fb83f8d87c8aff3b967582dc9e6ebc4ae331f587a295e74942cd23ae6de90`  
		Last Modified: Thu, 15 Apr 2021 08:46:46 GMT  
		Size: 655.7 KB (655732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3904f40f6d4957a5ddba82bb4288611c6e64d0b7484d6b1d983e0bca547bedf7`  
		Last Modified: Thu, 15 Apr 2021 08:47:38 GMT  
		Size: 11.6 MB (11562375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4ba313677532a0e91a7d5c5391c5696f0f1e703c6849df9874d48683a2fe13`  
		Last Modified: Thu, 15 Apr 2021 08:47:36 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877034d7564dd3fc8763611da2bbc0cc45b62ea6c4597f19254bfde2147ef69f`  
		Last Modified: Mon, 03 May 2021 22:21:15 GMT  
		Size: 2.3 MB (2311878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-alpine3.12` - linux; arm variant v6

```console
$ docker pull python@sha256:02aad827a32c9b1bb1184c23a343508dea98e0ac881b0148f3d03d8294d5cc83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16783993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb98d3fb54704655e7cc857f4d03ea308f27f72562211089416d72b4c660471`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:29:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 03:29:25 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 03:29:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 15 Apr 2021 03:53:42 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 15 Apr 2021 03:53:43 GMT
ENV PYTHON_VERSION=3.9.4
# Thu, 15 Apr 2021 04:04:11 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 15 Apr 2021 04:04:14 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 03 May 2021 22:31:58 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Mon, 03 May 2021 22:31:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Mon, 03 May 2021 22:32:00 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Mon, 03 May 2021 22:32:25 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 03 May 2021 22:32:27 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22d9b29dc18cb822ea3d5f85d3217efa8f16b0feac0502d2d837c8878b9866`  
		Last Modified: Thu, 15 Apr 2021 05:19:15 GMT  
		Size: 659.6 KB (659617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d379de9d529a6f2db29c0fc4d929ee8a9b9ee03ddf0df63afc8173cef7348529`  
		Last Modified: Thu, 15 Apr 2021 05:19:54 GMT  
		Size: 11.2 MB (11206877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd4dad177bfb0afe7ec3c3364a8003a312865edabba74fc4e99b1efa5767f0e`  
		Last Modified: Thu, 15 Apr 2021 05:19:49 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4ddd8cfb7d9b94c6a2da0dd4694ba6cc43077e2618d7e8282cac61855836ef`  
		Last Modified: Mon, 03 May 2021 22:38:01 GMT  
		Size: 2.3 MB (2312017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-alpine3.12` - linux; arm variant v7

```console
$ docker pull python@sha256:2003dd9b1aeb59dbe8cfcbe2ce18134df527842185a278328e5296da8e5d49e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15634269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45367a9e55d3b63e38f0f869d5c9f248f568dbdd75f9ef1c152aa422af2c881`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 04:24:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 04:24:52 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 04:24:57 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 15 Apr 2021 04:40:19 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 15 Apr 2021 04:40:20 GMT
ENV PYTHON_VERSION=3.9.4
# Thu, 15 Apr 2021 04:45:30 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 15 Apr 2021 04:45:33 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 03 May 2021 23:17:21 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Mon, 03 May 2021 23:17:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Mon, 03 May 2021 23:17:26 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Mon, 03 May 2021 23:17:46 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 03 May 2021 23:17:48 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbc3dd24a8cf7bda941c450c7729d3e80b142b2f026d84c86685559ebf5195d`  
		Last Modified: Thu, 15 Apr 2021 05:43:36 GMT  
		Size: 652.0 KB (651957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce6b4ecd0b4a1ee392cdf3adcdea153741868d3f7d53c4c157715807300629c`  
		Last Modified: Thu, 15 Apr 2021 05:44:14 GMT  
		Size: 10.3 MB (10260898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2372feeaf7bf21af4a6fb66af1ee5be1d5fdd8799764bcdfa7b202d4e01003`  
		Last Modified: Thu, 15 Apr 2021 05:44:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad9df4addeb9e0d90e8bdc8160992856dc049ae425461dab9bc3550c77152f4`  
		Last Modified: Mon, 03 May 2021 23:29:54 GMT  
		Size: 2.3 MB (2312005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull python@sha256:1fe5abe8f16dde2a8033d25f5ec73f11dcfda21b7e4945e2912df74dbc8e0951
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17326121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764f5271e8b355d8ed08c95b1a14b6c83b2dbe8d08e68d7c3fc7be53e5bcd67b`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:13:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 04:38:28 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 04:38:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 15 Apr 2021 04:56:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 15 Apr 2021 04:56:42 GMT
ENV PYTHON_VERSION=3.9.4
# Thu, 15 Apr 2021 05:04:20 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 15 Apr 2021 05:04:23 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 03 May 2021 22:24:35 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Mon, 03 May 2021 22:24:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Mon, 03 May 2021 22:24:38 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Mon, 03 May 2021 22:24:58 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 03 May 2021 22:25:01 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853110725fcad2152238b2a7dba8383d923fb5aad245c2018aa0288dcc919dfb`  
		Last Modified: Thu, 15 Apr 2021 06:11:31 GMT  
		Size: 658.3 KB (658297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138df36bcac6201671d094df095ce554617dfeba0e727c3e76dbe50ba6d6c900`  
		Last Modified: Thu, 15 Apr 2021 06:12:13 GMT  
		Size: 11.6 MB (11644895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ffb7ec072845207e57a98b135c181607663c7749f27c028783f86f582b258a`  
		Last Modified: Thu, 15 Apr 2021 06:12:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e90fe9d59fdf0d3e3e64a59ee919ef5be0bf5bf44c9f7f764f98434eb3f78a`  
		Last Modified: Mon, 03 May 2021 22:41:04 GMT  
		Size: 2.3 MB (2312004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-alpine3.12` - linux; 386

```console
$ docker pull python@sha256:37f83758984344ea32c19a3404fec9bb9dffe39a1ebd4f768475b39b06570ec0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17569944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3ca59806dac85568566f414facf53639b3681567d23c2e8fbce73432b075c5`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:25:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 19:25:48 GMT
ENV LANG=C.UTF-8
# Wed, 14 Apr 2021 19:25:49 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 14 Apr 2021 19:41:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 14 Apr 2021 19:41:30 GMT
ENV PYTHON_VERSION=3.9.4
# Wed, 14 Apr 2021 19:48:51 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Wed, 14 Apr 2021 19:48:52 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 03 May 2021 21:48:06 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Mon, 03 May 2021 21:48:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Mon, 03 May 2021 21:48:06 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Mon, 03 May 2021 21:48:13 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 03 May 2021 21:48:14 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af60c61b427f5518b074029ecdcbbd47445fa852df39326d1ecbeee2d7eb3d5`  
		Last Modified: Wed, 14 Apr 2021 23:34:53 GMT  
		Size: 661.9 KB (661850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6ce2a300db4590332508f27222fee34800217303713c565158f14fc455d1a5`  
		Last Modified: Wed, 14 Apr 2021 23:36:06 GMT  
		Size: 11.8 MB (11800239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3888501471c6dcd5d76ef935f8b5f59917740a6b91f3f8d985449fe89413d46b`  
		Last Modified: Wed, 14 Apr 2021 23:36:03 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f08965210a4063158438c76cf6c8ac747a14651509347a513ceae106eb7ba5`  
		Last Modified: Mon, 03 May 2021 21:59:20 GMT  
		Size: 2.3 MB (2311830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-alpine3.12` - linux; ppc64le

```console
$ docker pull python@sha256:5930558c3a265f40d0bb61e7b68bbc402fc21bc88cc609b14755e9c09931619e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18120572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe5533b5a8a3f4f88978258605339d7142daa94cd4447aa4d54c4fbb0614c07`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 05:21:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 05:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 05:21:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 15 Apr 2021 05:41:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 15 Apr 2021 05:41:42 GMT
ENV PYTHON_VERSION=3.9.4
# Thu, 15 Apr 2021 05:49:54 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 15 Apr 2021 05:50:04 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 03 May 2021 22:54:27 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Mon, 03 May 2021 22:54:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Mon, 03 May 2021 22:54:37 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Mon, 03 May 2021 22:55:22 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 03 May 2021 22:55:50 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72e0cf4bbf8f6a43d488c1e80e36218d61c3dcc8c6ebd5ef3dd9c1fd0816f8e`  
		Last Modified: Thu, 15 Apr 2021 06:59:09 GMT  
		Size: 664.6 KB (664628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1482ae88b63deaa0d70ac809a0f106bb4d5bb03a07a21bc7e21c307ceab87cce`  
		Last Modified: Thu, 15 Apr 2021 07:00:01 GMT  
		Size: 12.3 MB (12337015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8c3fed5071a515cc2e3981248899ee287971c1faf2c86dccc8d6837ba8457d`  
		Last Modified: Thu, 15 Apr 2021 06:59:58 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9a635e2a5adb09c967380a9df88f96dad0dcf04dbe3147dd45295e12fb215b`  
		Last Modified: Mon, 03 May 2021 23:18:58 GMT  
		Size: 2.3 MB (2311947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-alpine3.12` - linux; s390x

```console
$ docker pull python@sha256:b8373c7806a2a5e8464251ce3e0d130de2624705722b1c4c6d32221adb385d44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17108872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d6c9272cfe5292386da818df1a22066f75c2feeb29385186d5b80ae136b962`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:03:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 03:03:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 03:03:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 15 Apr 2021 03:15:03 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 15 Apr 2021 03:15:04 GMT
ENV PYTHON_VERSION=3.9.4
# Thu, 15 Apr 2021 03:20:00 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 15 Apr 2021 03:20:01 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 03 May 2021 22:07:09 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Mon, 03 May 2021 22:07:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Mon, 03 May 2021 22:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Mon, 03 May 2021 22:07:22 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 03 May 2021 22:07:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3003d9f853d0f905ce6502084f7a6423cd871f2dbf70b8a1fdc6ada2253b5064`  
		Last Modified: Thu, 15 Apr 2021 06:50:17 GMT  
		Size: 660.5 KB (660522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab474271623af816b4a47232d1ac1a2a1699c592c2bec713d4049c39028e7ed2`  
		Last Modified: Thu, 15 Apr 2021 06:50:50 GMT  
		Size: 11.6 MB (11567870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd9578ca0ad974b9bd86117cad2d4fa06ee4532697023bcf3669dbf79f667b4`  
		Last Modified: Thu, 15 Apr 2021 06:50:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0dc4d6976f06cce995f2874bae66d259e479b73ed255fa767618940c20b32a`  
		Last Modified: Mon, 03 May 2021 22:15:16 GMT  
		Size: 2.3 MB (2311820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
