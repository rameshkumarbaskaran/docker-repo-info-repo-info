## `hylang:python3.6-alpine3.13`

```console
$ docker pull hylang@sha256:5915d897740baa8ebd13c08d9e982531ffade8ab96103d6b21522c1acc6d8aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hylang:python3.6-alpine3.13` - linux; amd64

```console
$ docker pull hylang@sha256:78d29777d52ab2ec6702b8ce41b2d1b06ad79a525e3293e1b17122a107537c2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18601189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c66bd7a3251862fd6a9311dd19537fcd3bad19cb8e7748dc00723a20d4bd47`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 00:09:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 03:28:43 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 04:09:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Sat, 13 Nov 2021 04:31:13 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 13 Nov 2021 04:47:52 GMT
ENV PYTHON_VERSION=3.6.15
# Sat, 13 Nov 2021 04:54:11 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 04:54:12 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 04:54:12 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 04:54:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 04:54:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 04:54:13 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 04:54:19 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 04:54:20 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 14:23:19 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 14:23:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 14:23:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8988a686bbdf503e1884e129cd15b1c21e9b99679011c8b181fcc33ac850f7b`  
		Last Modified: Sat, 13 Nov 2021 04:58:50 GMT  
		Size: 281.8 KB (281794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845d13a7d9f81e20474b23dbc91245ea51e408fd07913e4e85c1950709e705e5`  
		Last Modified: Sat, 13 Nov 2021 05:00:03 GMT  
		Size: 10.2 MB (10185001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7352d3dccdbbafadd715579ae6fcaef71351bfec92c46d94b089e1a0625783fc`  
		Last Modified: Sat, 13 Nov 2021 05:00:00 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1ea37bcc6a43d7322db88f8e46c6b225b7e6fe3e0341364117090f7b0e480`  
		Last Modified: Sat, 13 Nov 2021 05:00:01 GMT  
		Size: 2.2 MB (2208243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72cc78cba51b99d0a197bddfa04b6c687a47aca3e93cf6f9b517fe0e4c89a9`  
		Last Modified: Sat, 13 Nov 2021 14:27:34 GMT  
		Size: 3.1 MB (3103496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-alpine3.13` - linux; arm variant v6

```console
$ docker pull hylang@sha256:bae4e9bfa1bb6110c16c5422e33dc6e68c94eec16c4bf501edb0d60d213b0f43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18031767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb3bba34052622a916a88e23b6014c1bb7fe9fb496c9e556ba01fb788b295f3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:01:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 20:01:04 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 21:10:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 12 Nov 2021 21:42:09 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 12 Nov 2021 23:53:31 GMT
ENV PYTHON_VERSION=3.6.15
# Sat, 13 Nov 2021 00:04:24 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 00:04:26 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 00:04:27 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 00:04:27 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 00:04:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 00:04:28 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 00:04:44 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 00:04:45 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 12:20:54 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 12:21:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 12:21:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377dc661bfa03e678e939796b0bbd125725b11b0d779b3caa6d029f0d96ca26b`  
		Last Modified: Sat, 13 Nov 2021 00:10:54 GMT  
		Size: 281.9 KB (281884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f378094b726964fdb740c1548aacbbb394b1c1ec98041f69e969585b6ac228fd`  
		Last Modified: Sat, 13 Nov 2021 00:12:25 GMT  
		Size: 9.8 MB (9804080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aa26271637ebd498060793d98ed2d7fb43a4f594f8a540fd0c3aae67cf6e59`  
		Last Modified: Sat, 13 Nov 2021 00:12:19 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0bda7c68fdb757abe72278a55609d2776a38538d6a756f11e4fd261b8af260`  
		Last Modified: Sat, 13 Nov 2021 00:12:21 GMT  
		Size: 2.2 MB (2208347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f219dd5c6c0e899eb43bdf590f1ea7fa336a8c22f2782c32f5c4f669290ef9c`  
		Last Modified: Sat, 13 Nov 2021 12:27:11 GMT  
		Size: 3.1 MB (3103881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-alpine3.13` - linux; arm variant v7

```console
$ docker pull hylang@sha256:de4148ddb27eba619ed644555011a2560b63d36ab56369ae160d728de089908a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17386571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdf6a639bd7fecfef97729fd15b44b3b4c703c73d418d531a844f26a5d2d5a4`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:54 GMT
ADD file:a13993855beba2267575c54a0c6707ddda85d238e697a81046a8b1c1a34df054 in / 
# Fri, 12 Nov 2021 16:57:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 23:42:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 23:42:30 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 00:49:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Sat, 13 Nov 2021 01:20:12 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 13 Nov 2021 01:51:13 GMT
ENV PYTHON_VERSION=3.6.15
# Sat, 13 Nov 2021 02:01:52 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 02:01:54 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 02:01:54 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 02:01:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 02:01:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 02:01:55 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 02:02:12 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 02:02:13 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 16:02:04 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 16:02:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 16:02:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:767c1b67bc22761376676021ea5a310e7a7d1344b7a017bb8ede1a202340dbaf`  
		Last Modified: Fri, 12 Nov 2021 16:59:54 GMT  
		Size: 2.4 MB (2436506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0af384e4172ece4e9dce7ddf11f19b75ea1caa7d990df7afb815270a0a0800`  
		Last Modified: Sat, 13 Nov 2021 02:14:27 GMT  
		Size: 281.1 KB (281067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85884b5136a8cff8dfd81f8ca013a4569dbd5940915897abe6c00025b015aa28`  
		Last Modified: Sat, 13 Nov 2021 02:16:30 GMT  
		Size: 9.4 MB (9356391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb75bc8b49a386a25acb102a6dc192abeb190b7e7f660745ccd50db95802070f`  
		Last Modified: Sat, 13 Nov 2021 02:16:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afe1b2e88d91f2cc3cf063f27080b5baa70a0e36f6d6d292c9f2058c07a714c`  
		Last Modified: Sat, 13 Nov 2021 02:16:27 GMT  
		Size: 2.2 MB (2208523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de1555c2e6e2f77360dbcb8affb5b3c12889db4b74d75b4acc5288a4d263cc`  
		Last Modified: Sat, 13 Nov 2021 16:11:21 GMT  
		Size: 3.1 MB (3103854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d60658757ac56cab6a362d0885ef43e9fbe8966d5ead8ae98f2aca5982ca4e35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18587870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bf29569cc9e5835160a93a8e170631585c974ee9f93b577aabfd2783e2dd0c`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:21:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 22:21:32 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 22:57:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 12 Nov 2021 23:12:54 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 12 Nov 2021 23:28:25 GMT
ENV PYTHON_VERSION=3.6.15
# Fri, 12 Nov 2021 23:33:58 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 12 Nov 2021 23:33:59 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Nov 2021 23:33:59 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 12 Nov 2021 23:34:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 12 Nov 2021 23:34:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 12 Nov 2021 23:34:02 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 12 Nov 2021 23:34:10 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Nov 2021 23:34:11 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 15:38:49 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 15:38:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 15:38:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10ab9348049cbef907d6f367f6d4b5aca599bfd6cb00c721f328716097f2857`  
		Last Modified: Fri, 12 Nov 2021 23:40:02 GMT  
		Size: 281.8 KB (281804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d26cd7d450679cf74fab467d3c8336c66e30a592719d98ef93ee6f23f0cff2`  
		Last Modified: Fri, 12 Nov 2021 23:41:15 GMT  
		Size: 10.3 MB (10274064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d8119eee7842d91d130e74ba7c8ff0e12d6468d9cb8c64c7f6bdcb57312fbd`  
		Last Modified: Fri, 12 Nov 2021 23:41:14 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e1fbfcc05b97ffab0bb21b682380025b148ddbce0d3117383f94ab04b780c4`  
		Last Modified: Fri, 12 Nov 2021 23:41:14 GMT  
		Size: 2.2 MB (2209468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7639c9d54ac2251e07700929fae406d3758b2a30b4128b95d3b92012cc4a463`  
		Last Modified: Sat, 13 Nov 2021 15:44:48 GMT  
		Size: 3.1 MB (3102664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-alpine3.13` - linux; 386

```console
$ docker pull hylang@sha256:756ee75774720031fbcbce51fec082ff7104eec128412c1bd2eb8875b745a226
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18788105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262933a11f5e4ce7d5a9656ff4a41e1253bcfe9aec2c359ae72842c65b1fb993`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:18:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 22:18:31 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 22:57:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 12 Nov 2021 23:13:09 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 12 Nov 2021 23:29:03 GMT
ENV PYTHON_VERSION=3.6.15
# Fri, 12 Nov 2021 23:35:28 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 12 Nov 2021 23:35:29 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Nov 2021 23:35:29 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 12 Nov 2021 23:35:29 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 12 Nov 2021 23:35:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 12 Nov 2021 23:35:30 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 12 Nov 2021 23:35:37 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Nov 2021 23:35:37 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 10:02:24 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 10:02:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 10:02:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b73aaa09f0571c5319e8017fd9817c65b78b80f85c025bbedab5b1bc6f5d58`  
		Last Modified: Fri, 12 Nov 2021 23:42:33 GMT  
		Size: 282.3 KB (282321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4856c54cb637cf80cd9a44555c5e46c3ce93b2eb06a4462a5be1df0b99f7a3`  
		Last Modified: Fri, 12 Nov 2021 23:44:18 GMT  
		Size: 10.4 MB (10364681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c901f5a6b43f644cd7cc200ed0fa29b5982bbd030d72a1883dd910d649be91`  
		Last Modified: Fri, 12 Nov 2021 23:44:16 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec26c1e9e6bbb8a0ee9bcf078dd2c816793ba8b87e5823217454020fca8177f`  
		Last Modified: Fri, 12 Nov 2021 23:44:17 GMT  
		Size: 2.2 MB (2208297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259942cb8aae0889438f75b9ef1e5e35bfaa8c3089b122e272c3753f927c2d8e`  
		Last Modified: Sat, 13 Nov 2021 10:10:58 GMT  
		Size: 3.1 MB (3103758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-alpine3.13` - linux; ppc64le

```console
$ docker pull hylang@sha256:1956b7ee110b3fa5b77f14081edfb81484856259cefdccce7a9abec6d3eadfbc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18862618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdae4359d49f2e38afb5ee167791c9c62642c978ea4ed8167a167e74796931f`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:25 GMT
ADD file:f7216323de17450e653f77c86d2c1e2e8ec01e1133e93f29c515761b3e9d8f7d in / 
# Fri, 12 Nov 2021 21:18:28 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:04:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 04:04:14 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 04:57:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Sat, 13 Nov 2021 05:20:19 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 13 Nov 2021 05:42:32 GMT
ENV PYTHON_VERSION=3.6.15
# Sat, 13 Nov 2021 05:50:27 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 05:50:36 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 05:50:38 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 05:50:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 05:50:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 05:50:44 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 05:51:02 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 05:51:06 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 18:10:00 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 18:10:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 18:10:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6729720a3e6b58511df148134bb67d786ad90f9fce1c02ba5bbfd31f33055fbe`  
		Last Modified: Fri, 12 Nov 2021 21:19:49 GMT  
		Size: 2.8 MB (2820517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95314a1ef5d40d5e839cf46d867e24562c77fd14af8b75b710077ac16ad0acb6`  
		Last Modified: Sat, 13 Nov 2021 05:57:04 GMT  
		Size: 283.9 KB (283887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22892afd99963188938a78eec26c6d4b74bd68407547dc5b8ac31ba7c3a295d1`  
		Last Modified: Sat, 13 Nov 2021 05:58:20 GMT  
		Size: 10.4 MB (10445400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9d49eb09afe2deecf372fb22c78451051dde1d54840fd30a7ca316ba59a545`  
		Last Modified: Sat, 13 Nov 2021 05:58:18 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b88c1fa0777958a4b35f15f6447247e6c5b98931bd430451544b2d97761365`  
		Last Modified: Sat, 13 Nov 2021 05:58:18 GMT  
		Size: 2.2 MB (2208258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c189e0fb605046d29ef9279f501ffe6e89fb66d550ae10b1051259b49583d0e4`  
		Last Modified: Sat, 13 Nov 2021 18:16:58 GMT  
		Size: 3.1 MB (3104325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-alpine3.13` - linux; s390x

```console
$ docker pull hylang@sha256:044d83b0f537c360b07827e8019a57ec7e263476b13c68a27ca5f22152dfffb7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18399978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184376a5c6172b9c7f1a3e42b40b3d74ffa0b34e21c9f3686b32b371129c85e7`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:44 GMT
ADD file:637f327c9b07758709ef7dbc42eb472c888d221acde89b1c3775553864334d5c in / 
# Fri, 12 Nov 2021 16:41:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:00:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 18:00:18 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 18:26:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 12 Nov 2021 18:38:19 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 12 Nov 2021 18:49:58 GMT
ENV PYTHON_VERSION=3.6.15
# Fri, 12 Nov 2021 18:54:19 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 12 Nov 2021 18:54:19 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Nov 2021 18:54:20 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 12 Nov 2021 18:54:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 12 Nov 2021 18:54:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 12 Nov 2021 18:54:20 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 12 Nov 2021 18:54:25 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Nov 2021 18:54:26 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 05:03:11 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 05:03:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 05:03:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b872f056719bde6e6722091afb2a3376d720c69c142b91ac352050080dd79615`  
		Last Modified: Fri, 12 Nov 2021 16:42:54 GMT  
		Size: 2.6 MB (2611155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fdb710002c470931ee6b58887b9dcddd5d1e9aee6945a4e9a21c8b24bc615b`  
		Last Modified: Fri, 12 Nov 2021 19:00:28 GMT  
		Size: 282.2 KB (282208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4601551aec97b4c5c08dff3857b93c9f459d400d2dded07740d410c271eba6f`  
		Last Modified: Fri, 12 Nov 2021 19:01:29 GMT  
		Size: 10.2 MB (10194575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12fe996a76b672d3d39b46abb6834f2966d482f5fe29ab6c4b413814ae9be2f`  
		Last Modified: Fri, 12 Nov 2021 19:01:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69dc65daa7ed7521fbc5b87a7327d3666f8a8777b8d3d5d9e821e8d842b4661`  
		Last Modified: Fri, 12 Nov 2021 19:01:28 GMT  
		Size: 2.2 MB (2208245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dfbc9554b14c97bb965897b8f32a426d76d3709be9bc89fa329627dee54062`  
		Last Modified: Sat, 13 Nov 2021 05:07:43 GMT  
		Size: 3.1 MB (3103566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
