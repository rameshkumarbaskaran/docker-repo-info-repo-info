## `hylang:0-python2.7-alpine3.10`

```console
$ docker pull hylang@sha256:4b87342d224f8551581d8887dbd7954772122af905429d932ed0b99059af6049
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

### `hylang:0-python2.7-alpine3.10` - linux; amd64

```console
$ docker pull hylang@sha256:c187e165959151868abe941eb90ab29307c82c8d1106423e3bbfc8c1b4cf28b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27579712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef36a5ecff45bc3d275cd696122e51394157b45653d1b240465b64729f3e0865`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 18:05:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 23:09:17 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2020 02:52:32 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 24 Jan 2020 02:52:33 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Jan 2020 02:52:33 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Fri, 24 Jan 2020 02:52:33 GMT
ENV PYTHON_VERSION=2.7.17
# Fri, 24 Jan 2020 15:44:26 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 25 Jan 2020 02:55:25 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:55:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:55:25 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:55:31 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 25 Jan 2020 02:55:31 GMT
CMD ["python2"]
# Sat, 25 Jan 2020 03:39:13 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 03:39:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 25 Jan 2020 03:39:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e507aa444c2692079f4cf65add01b22020666dc8ee6957b54f385819b4ff451`  
		Last Modified: Fri, 24 Jan 2020 15:46:31 GMT  
		Size: 301.7 KB (301734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0815e166a2567b56b16e49164226c0b5f9e1c1b881973a2f86a054bd239d60`  
		Last Modified: Fri, 24 Jan 2020 15:46:47 GMT  
		Size: 20.1 MB (20119541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1150622632cc246e11c4cdd675fb3624f7d09c46d4fba20a52ed83274eb96db0`  
		Last Modified: Sat, 25 Jan 2020 02:58:42 GMT  
		Size: 1.9 MB (1883222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e51f843d8096b7914d297988028bb9b080f23c59dd43a5df976847f300ac3dc`  
		Last Modified: Sat, 25 Jan 2020 03:41:44 GMT  
		Size: 2.5 MB (2488253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7-alpine3.10` - linux; arm variant v6

```console
$ docker pull hylang@sha256:f37b9bfa51fea350ec512e20b5ee2a2b765817976ce066f1e773f876784a25a2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25971704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dbfdbd949396054d7bc64edf65ef544f586ad7a180b2e3bd4b85aa32f5a0fb`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:45:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 17:45:49 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 18:40:29 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 23 Jan 2020 18:40:34 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 18:40:38 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Thu, 23 Jan 2020 18:40:40 GMT
ENV PYTHON_VERSION=2.7.17
# Thu, 23 Jan 2020 18:48:53 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 25 Jan 2020 01:57:27 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 01:57:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 01:57:34 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 01:57:54 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 25 Jan 2020 01:57:55 GMT
CMD ["python2"]
# Sat, 25 Jan 2020 02:17:36 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 02:17:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 25 Jan 2020 02:17:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103fab25abafad353da8025ec698772c35a3872f2e5ea9a2d2b4a198168741c7`  
		Last Modified: Thu, 23 Jan 2020 18:51:37 GMT  
		Size: 302.0 KB (302017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b2a6ae937ba5dae9b86870478ad1a44b5d257dd3882728c420acf2ed830aa8`  
		Last Modified: Thu, 23 Jan 2020 18:51:47 GMT  
		Size: 18.7 MB (18725673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75191c7528d0d1a9b8533b9cd9867974f72235bc786375b6ac33a4d6e1ab6f2c`  
		Last Modified: Sat, 25 Jan 2020 02:00:38 GMT  
		Size: 1.9 MB (1883429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563cad3b84c1e11890d6b7d640feb142778d3548d30f1265ff1f1245687422a6`  
		Last Modified: Sat, 25 Jan 2020 02:19:37 GMT  
		Size: 2.5 MB (2489178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7-alpine3.10` - linux; arm variant v7

```console
$ docker pull hylang@sha256:586d80196d85f356a8b61a84645554b9eab4bb73f8aaad2db131a1b2aa904af9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25390894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7f5c7d438720b31de9a7ebd19fb6021dafbf89b30721bb3a2efe5b5f4370da`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:31 GMT
ADD file:d05c9f9143d11d12045d4faef882e5985e6b38fabe52237dd8d8c0627a9620ab in / 
# Thu, 23 Jan 2020 16:53:32 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:16:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 19:16:24 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 20:07:33 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 23 Jan 2020 20:07:35 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 20:07:36 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Thu, 23 Jan 2020 20:07:36 GMT
ENV PYTHON_VERSION=2.7.17
# Thu, 23 Jan 2020 20:15:32 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 25 Jan 2020 02:45:45 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:45:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:45:48 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:46:01 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 25 Jan 2020 02:46:03 GMT
CMD ["python2"]
# Sat, 25 Jan 2020 04:06:50 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 04:06:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 25 Jan 2020 04:07:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4e972d957a606327b0b6c2e8aa4a6045c263b7496a536298aaebf690e9d85f1d`  
		Last Modified: Thu, 23 Jan 2020 16:53:59 GMT  
		Size: 2.4 MB (2378408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0528659ad2096c7c67779e82c6317d46a6100d4050ae29f5cc8a8391a517c396`  
		Last Modified: Thu, 23 Jan 2020 20:19:21 GMT  
		Size: 300.9 KB (300947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94df0ee546fc6e571193703e856f01ef196ae6fc1f17993310758e876cda98d`  
		Last Modified: Thu, 23 Jan 2020 20:19:30 GMT  
		Size: 18.3 MB (18338914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dfd16bd99b3eb264e58ab7638f7277c6f100adfad17f991200af8714edca21`  
		Last Modified: Sat, 25 Jan 2020 02:51:23 GMT  
		Size: 1.9 MB (1883401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7636fd3183ca69816db90e18d7cf62d8ba20e4cb9c486159b31b6f9714ad179`  
		Last Modified: Sat, 25 Jan 2020 04:10:51 GMT  
		Size: 2.5 MB (2489224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7-alpine3.10` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:83a6bd6fbc3c6c3dee7d02ac564217bf6d131e0624a68f5e84fc576ca052547f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27207862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b969607392acd4bc83814480eeba730a25095a2e5ea61238a03929c469075bd`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:59:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 21:00:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 21:50:05 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 23 Jan 2020 21:50:08 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 21:50:09 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Thu, 23 Jan 2020 21:50:10 GMT
ENV PYTHON_VERSION=2.7.17
# Thu, 23 Jan 2020 21:58:41 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 25 Jan 2020 02:26:55 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:26:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:26:58 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:27:12 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 25 Jan 2020 02:27:14 GMT
CMD ["python2"]
# Sat, 25 Jan 2020 02:59:23 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 02:59:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 25 Jan 2020 02:59:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a125182a50f71661e1ddab2e929f60432e6d7df52c04ec7f06fd341fb7c0912`  
		Last Modified: Thu, 23 Jan 2020 22:02:06 GMT  
		Size: 302.4 KB (302361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58527918589164c54232196a2c9b1a4dcdf510ffe98b28e5f2825aa71b1ed687`  
		Last Modified: Thu, 23 Jan 2020 22:02:23 GMT  
		Size: 19.8 MB (19815363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2105ac38a5b1defeb871a00af5c1c11d84b553f1396f243960ae8d976bfa19`  
		Last Modified: Sat, 25 Jan 2020 02:32:45 GMT  
		Size: 1.9 MB (1883412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6b11ee7a572656bc07fff456f09f48f39247b64bfd412783a7aeef5547b7e7`  
		Last Modified: Sat, 25 Jan 2020 03:04:25 GMT  
		Size: 2.5 MB (2488994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7-alpine3.10` - linux; 386

```console
$ docker pull hylang@sha256:bf7c6c5b34c021e4364bccba69e34e2df8a157b5957256b48cd3ecb51c45c423
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26713648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95db3888de9dfe0a2823040ed92ad03699cb004e5220fa2794e5402ddc83f2b8`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:57 GMT
ADD file:8c429ecc11f3cadcecc39922ce15df6b51a649929959b331fed8d1f42d722474 in / 
# Thu, 23 Jan 2020 16:52:57 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2020 02:47:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2020 02:47:16 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2020 03:34:15 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 24 Jan 2020 03:34:16 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Jan 2020 03:34:16 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Fri, 24 Jan 2020 03:34:16 GMT
ENV PYTHON_VERSION=2.7.17
# Fri, 24 Jan 2020 03:40:05 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 25 Jan 2020 02:03:24 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:03:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:03:24 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:03:30 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 25 Jan 2020 02:03:30 GMT
CMD ["python2"]
# Sat, 25 Jan 2020 02:09:13 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 02:09:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 25 Jan 2020 02:09:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8ad089020f8a1fd366fb13feb183e2f4c7410e2232c54b40f6a54fd56029fdf3`  
		Last Modified: Thu, 23 Jan 2020 16:53:22 GMT  
		Size: 2.8 MB (2785861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0bf133891093637e0f53629d4203865f70dcbac7f233fe445430cb51fd78f4`  
		Last Modified: Fri, 24 Jan 2020 03:44:53 GMT  
		Size: 302.3 KB (302331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2f643d55ebf53e59f401e4a6fe4d6f4e83ace48de029cc0f379a803beb60e7`  
		Last Modified: Fri, 24 Jan 2020 03:44:57 GMT  
		Size: 19.3 MB (19253701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f980386af09c9b2a2e94148d936255daf85c5ee8dc8515a12da9604f5b00929`  
		Last Modified: Sat, 25 Jan 2020 02:06:54 GMT  
		Size: 1.9 MB (1883217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f1ed4c640dbecf0a1ea85555584c04b9100d62f2179aa7a493a336bcab0b7`  
		Last Modified: Sat, 25 Jan 2020 02:12:25 GMT  
		Size: 2.5 MB (2488538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7-alpine3.10` - linux; ppc64le

```console
$ docker pull hylang@sha256:66ceaa9d378d3a849642ae4c54212abfcb23d988caf8f3d50296d6a1c5f509ae
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28212005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4349efe7d917a60b7deb63141cbcb6d3317be08b3f7826dc4113ccf93a5427`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:57:54 GMT
ADD file:5e383dfaf3281b9cc17caf519d1aeba934fa92632c10afb8cc189f6ba12d9f64 in / 
# Thu, 23 Jan 2020 16:57:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:41:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 19:41:01 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 20:31:06 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 23 Jan 2020 20:31:13 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 20:31:15 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Thu, 23 Jan 2020 20:31:17 GMT
ENV PYTHON_VERSION=2.7.17
# Thu, 23 Jan 2020 20:38:38 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 25 Jan 2020 02:53:26 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:53:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:53:31 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:53:50 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 25 Jan 2020 02:53:52 GMT
CMD ["python2"]
# Sat, 25 Jan 2020 03:44:02 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 03:44:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 25 Jan 2020 03:44:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4ae00dedbff84a762d4b8b9176da2beee50017c43fe09a5ae92c2417d5634510`  
		Last Modified: Thu, 23 Jan 2020 16:58:43 GMT  
		Size: 2.8 MB (2808535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeee9f9e24f607d426fad2a62e4af0fc5fe6ac0d3f31a823a581c6223c8c83de`  
		Last Modified: Thu, 23 Jan 2020 20:43:28 GMT  
		Size: 304.5 KB (304457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca69543c610bd6bb9111de00aebd803a2b3968358ffe0fca79233acb2e6069b8`  
		Last Modified: Thu, 23 Jan 2020 20:43:35 GMT  
		Size: 20.7 MB (20726520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84ef332caff4f80ffd9da7755950828434b34ad96cf736832f965165cea346e`  
		Last Modified: Sat, 25 Jan 2020 03:02:23 GMT  
		Size: 1.9 MB (1883409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cdeed4e1f43f97c539c8709a6989388cde5cb91715113b2bd30deb91eb4136`  
		Last Modified: Sat, 25 Jan 2020 03:50:35 GMT  
		Size: 2.5 MB (2489084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7-alpine3.10` - linux; s390x

```console
$ docker pull hylang@sha256:2cc13939452fe563462492df58d63dcc92389e6263ea26e043d7c1cdcc4b03d5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27414980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345c468f7298adacc2ec3d7ae83ac758859cf6ccd6f162ac343dd0c03ff844c4`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:43 GMT
ADD file:922e12714922ae035a33d6ceb8d2683ad3e454deca21ad02b699db908443342b in / 
# Thu, 23 Jan 2020 16:52:44 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:28:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 19:28:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 19:53:17 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 23 Jan 2020 19:53:18 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 19:53:18 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Thu, 23 Jan 2020 19:53:19 GMT
ENV PYTHON_VERSION=2.7.17
# Thu, 23 Jan 2020 19:56:56 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 25 Jan 2020 01:56:12 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 01:56:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 01:56:12 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 01:56:16 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 25 Jan 2020 01:56:16 GMT
CMD ["python2"]
# Sat, 25 Jan 2020 02:14:29 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 02:14:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 25 Jan 2020 02:14:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0449d076b2977b7e7ce4c35b0fe5199d86cabaf453e869da73b2efb66d6282dd`  
		Last Modified: Thu, 23 Jan 2020 16:53:07 GMT  
		Size: 2.6 MB (2573620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1298c7257575492fea28ab91a8979f6651c69a3b2164f5960873727df8264295`  
		Last Modified: Thu, 23 Jan 2020 19:59:15 GMT  
		Size: 302.4 KB (302383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b289f9871612de6a8b610ea5ef5d91719b104d59248223e5c0f159a1fe025eef`  
		Last Modified: Thu, 23 Jan 2020 19:59:27 GMT  
		Size: 20.2 MB (20167603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f608d9f2dc188cae8d9972da89a293b4923f4ae61ea089171dcad973b1fb28`  
		Last Modified: Sat, 25 Jan 2020 01:59:50 GMT  
		Size: 1.9 MB (1883209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbfa8ed9fd1609088cce059fbf757ae52b75c53ca50cc783fb33b614a4430eb`  
		Last Modified: Sat, 25 Jan 2020 02:16:52 GMT  
		Size: 2.5 MB (2488165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
