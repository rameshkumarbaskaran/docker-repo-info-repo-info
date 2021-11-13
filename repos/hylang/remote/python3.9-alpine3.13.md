## `hylang:python3.9-alpine3.13`

```console
$ docker pull hylang@sha256:707183cf059d27055d981e868fbc7d6d066b7a4731d2696274e3aa33e384ea89
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

### `hylang:python3.9-alpine3.13` - linux; amd64

```console
$ docker pull hylang@sha256:01e3c2fbeb0474ea922a8c282a421c54e59623da8a8e50314718101b81b07d53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20451775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88193170385769100d7480294a294a8d4d7a22bdf879da6c7fe1b0b2adadf776`
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
# Sat, 13 Nov 2021 03:28:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 13 Nov 2021 03:56:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 13 Nov 2021 03:56:08 GMT
ENV PYTHON_VERSION=3.9.8
# Sat, 13 Nov 2021 04:03:00 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 04:03:01 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 04:03:01 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 04:03:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 04:03:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 04:03:01 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 04:03:09 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 04:03:09 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 14:22:21 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 14:22:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 14:22:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9292b3ab1647e1bb411cdd98d02b0c2436ba3c029431a7d733ecfb3de59cce21`  
		Last Modified: Sat, 13 Nov 2021 04:57:32 GMT  
		Size: 677.7 KB (677699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8f3ab93a7d93e66248c23b428eb46078b3bc3722358d05a1be261efacba28d`  
		Last Modified: Sat, 13 Nov 2021 04:58:15 GMT  
		Size: 11.5 MB (11504313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e7a4c59f48b187d40ba5c978f629ff9825fc706ee216861bb561a9e5034e7e`  
		Last Modified: Sat, 13 Nov 2021 04:58:11 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43897e8f5a407cb22ebbdfab6b7361c5b18af0fa94cd10187b89a8565a7b8db`  
		Last Modified: Sat, 13 Nov 2021 04:58:13 GMT  
		Size: 2.3 MB (2348962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad80a15d3e733dee1b74952fc9b9f6381b15c9bf03f36ec5b784dd0407a67bbb`  
		Last Modified: Sat, 13 Nov 2021 14:26:04 GMT  
		Size: 3.1 MB (3098146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine3.13` - linux; arm variant v6

```console
$ docker pull hylang@sha256:2908f0f296764fd1f95177f5eaa6aacd29b41970050c7b18045dda13f762eec8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19820712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76eed55be2a8752d033a7d0565a9c0bb9f7a8aa12a25e256f6081c83d546e3b8`
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
# Fri, 12 Nov 2021 20:01:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 12 Nov 2021 20:45:59 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 12 Nov 2021 20:46:00 GMT
ENV PYTHON_VERSION=3.9.8
# Fri, 12 Nov 2021 20:58:01 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 12 Nov 2021 20:58:03 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Nov 2021 20:58:03 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 12 Nov 2021 20:58:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 12 Nov 2021 20:58:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 12 Nov 2021 20:58:05 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 12 Nov 2021 20:58:22 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Nov 2021 20:58:23 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 12:18:27 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 12:18:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 12:18:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f7d80233aba524fa90756e5fe92070e3f9c9e6fffa4e568a0a139683eeca6d`  
		Last Modified: Sat, 13 Nov 2021 00:09:13 GMT  
		Size: 682.9 KB (682857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c3279e9d8b9628ba68c88e2382b3a7ba0d0f061b004aa2a0b9f9efd5fff4c7`  
		Last Modified: Sat, 13 Nov 2021 00:10:14 GMT  
		Size: 11.1 MB (11056756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02296550d7ded8f24d5e43c49d6f35db2b5a7675f5f0010fac36751553bd00b`  
		Last Modified: Sat, 13 Nov 2021 00:10:07 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0435b924336f09453dacae4f4702df0f7e30d1d9d69a56427ddff59fbec4208c`  
		Last Modified: Sat, 13 Nov 2021 00:10:09 GMT  
		Size: 2.3 MB (2349135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1216a88a1c14d72d0aa9a59e7ae523cd6cf6e65f9385897b78ff51406fcaa6f`  
		Last Modified: Sat, 13 Nov 2021 12:25:19 GMT  
		Size: 3.1 MB (3098390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine3.13` - linux; arm variant v7

```console
$ docker pull hylang@sha256:efb387963f7d13fa01cc59b58ed85781b2a269b3b9f541d230e3d61be9c5c7bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19127970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e9e2702d97cc196b4fe253124fdbee46b7b1a08e3870f2d0930ecbc8089331`
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
# Fri, 12 Nov 2021 23:42:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 13 Nov 2021 00:25:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 13 Nov 2021 00:25:14 GMT
ENV PYTHON_VERSION=3.9.8
# Sat, 13 Nov 2021 00:36:49 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 00:36:51 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 00:36:51 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 00:36:52 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 00:36:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 00:36:53 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 00:37:09 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 00:37:10 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 15:58:38 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 15:58:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 15:58:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:767c1b67bc22761376676021ea5a310e7a7d1344b7a017bb8ede1a202340dbaf`  
		Last Modified: Fri, 12 Nov 2021 16:59:54 GMT  
		Size: 2.4 MB (2436506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a8bde8bec95fb486c126d7f176651eddcbb77935d82fc566f7df1f46bc7e9f`  
		Last Modified: Sat, 13 Nov 2021 02:12:25 GMT  
		Size: 676.7 KB (676723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e974818d9235938d9d3a0fcb59decfe6026bfb311b990a33b418bb11622501`  
		Last Modified: Sat, 13 Nov 2021 02:13:33 GMT  
		Size: 10.6 MB (10567103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef516fd694116aea3e82b5342c34a462e5a6c0c66830f95f9a1b89aa4e40872a`  
		Last Modified: Sat, 13 Nov 2021 02:13:29 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363edb09205ef3b03035af47a464cbc19d758abe61e5634ff754c82e20da975f`  
		Last Modified: Sat, 13 Nov 2021 02:13:30 GMT  
		Size: 2.3 MB (2349101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d96ddab262a94a0d3bff5bf47eedca4c7eb937d7ba554133b134b77cd8b1358`  
		Last Modified: Sat, 13 Nov 2021 16:09:09 GMT  
		Size: 3.1 MB (3098305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0a222309030004a896eb13f28b2b2d1e61a8850b72b31d7504f14bae6ab3e0aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20411804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e734187409753a162305e29e3848fd9f38f1ac7c1ebdcba4800af79055bc17`
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
# Fri, 12 Nov 2021 22:21:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 12 Nov 2021 22:44:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 12 Nov 2021 22:44:53 GMT
ENV PYTHON_VERSION=3.9.8
# Fri, 12 Nov 2021 22:50:45 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 12 Nov 2021 22:50:46 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Nov 2021 22:50:47 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 12 Nov 2021 22:50:48 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 12 Nov 2021 22:50:49 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 12 Nov 2021 22:50:50 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 12 Nov 2021 22:50:59 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Nov 2021 22:51:00 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 15:37:14 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 15:37:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 15:37:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c77ac88be53731c3295ce183badd4d6e279435d5b18ab0d8115c7b6c0f8f20`  
		Last Modified: Fri, 12 Nov 2021 23:38:45 GMT  
		Size: 679.9 KB (679888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbef8a6a88390b5f7d649d12321170468eefb8d9b13ec508cf68e54cf0553bf4`  
		Last Modified: Fri, 12 Nov 2021 23:39:27 GMT  
		Size: 11.6 MB (11563248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d0303e1959ae581810b7344fca8d30f3ac173429ad73531060a8a2b41af6d5`  
		Last Modified: Fri, 12 Nov 2021 23:39:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1021f743e53baa468290dc319012008625c1ba41460574482253dc8128c433b4`  
		Last Modified: Fri, 12 Nov 2021 23:39:26 GMT  
		Size: 2.4 MB (2350504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a308f6ce4f1715b4f5d5d5f6dfb9544dcae99be0a4f5a3caec487753555fedd5`  
		Last Modified: Sat, 13 Nov 2021 15:43:10 GMT  
		Size: 3.1 MB (3098294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine3.13` - linux; 386

```console
$ docker pull hylang@sha256:bc8e1f0809380a3c1afa4d5d711c3f5a8012f1cc71ffcd9f8bb3949c315293b1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20649637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c185a415357d8965a6636df8f40f656951429a010955e3114194ef8b30b3e42e`
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
# Fri, 12 Nov 2021 22:18:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 12 Nov 2021 22:42:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 12 Nov 2021 22:42:09 GMT
ENV PYTHON_VERSION=3.9.8
# Fri, 12 Nov 2021 22:49:24 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 12 Nov 2021 22:49:25 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Nov 2021 22:49:25 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 12 Nov 2021 22:49:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 12 Nov 2021 22:49:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 12 Nov 2021 22:49:26 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 12 Nov 2021 22:49:34 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Nov 2021 22:49:35 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 09:59:44 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 09:59:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 09:59:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9b0a34e47114bdc2ae8da2c0f4741507de370e11199fbbf14e7427b4c31666`  
		Last Modified: Fri, 12 Nov 2021 23:40:53 GMT  
		Size: 685.1 KB (685062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9cd9a1990f58efc56abacd94f685cb198a3af0355e7cf8274be229c44c811a`  
		Last Modified: Fri, 12 Nov 2021 23:41:45 GMT  
		Size: 11.7 MB (11688184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddb294c745273a1047c3e3365bf3682ec1c6bc50b9aad76dd2734b5cf05f0a2`  
		Last Modified: Fri, 12 Nov 2021 23:41:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8bda186d5b56cf6471bb4c0a75c304993b240b961566370b4fe1de555bc534`  
		Last Modified: Fri, 12 Nov 2021 23:41:43 GMT  
		Size: 2.3 MB (2349049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311849ec019f424b9d57aea73a16b390c56b7a24c0692e72276238a3226968e8`  
		Last Modified: Sat, 13 Nov 2021 10:08:50 GMT  
		Size: 3.1 MB (3098301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine3.13` - linux; ppc64le

```console
$ docker pull hylang@sha256:9911e1b404c80b9f085c2859a3566e6a40b2185f171a2f2c89629d2fb283c73b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20758143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b804c6c4b18409e6411366e0cebee7e38b01e26c22fc38c1688d3e1d3beb1a9a`
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
# Sat, 13 Nov 2021 04:04:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 13 Nov 2021 04:36:57 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 13 Nov 2021 04:37:00 GMT
ENV PYTHON_VERSION=3.9.8
# Sat, 13 Nov 2021 04:45:41 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 04:45:52 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 04:45:56 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 04:45:58 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 04:46:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 04:46:09 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 04:46:31 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 04:46:34 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 18:04:54 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 18:05:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 18:05:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6729720a3e6b58511df148134bb67d786ad90f9fce1c02ba5bbfd31f33055fbe`  
		Last Modified: Fri, 12 Nov 2021 21:19:49 GMT  
		Size: 2.8 MB (2820517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82f7b88e852ef28af6d661f7f7205b897bdafddbe130bd7c614bcf322cc8142`  
		Last Modified: Sat, 13 Nov 2021 05:55:45 GMT  
		Size: 686.6 KB (686582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a247cd5b663ce45284fd59f0f320bef446c87ac30f3a7de495b4b870a45dccf`  
		Last Modified: Sat, 13 Nov 2021 05:56:30 GMT  
		Size: 11.8 MB (11803250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6675d0fbf02744ee70a5231336adec7d62432f702669415bf656c22cab794213`  
		Last Modified: Sat, 13 Nov 2021 05:56:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6678267fa43cb1e095291c76c927120e3d820edf00a1cc4f6b5b22667a3bbd50`  
		Last Modified: Sat, 13 Nov 2021 05:56:28 GMT  
		Size: 2.3 MB (2349000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b05644e9cc1856c904695decceee55935a2e967a102b511064fc851f88de40`  
		Last Modified: Sat, 13 Nov 2021 18:15:07 GMT  
		Size: 3.1 MB (3098563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine3.13` - linux; s390x

```console
$ docker pull hylang@sha256:10bb98f137919450f40863b96cd629fddae39c7e1108b3b346998b8acef2f4ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20215507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a283152e5c57d995070bef2864bbafc868f5d1756806b2c22c7fdbd367357219`
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
# Fri, 12 Nov 2021 18:00:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 12 Nov 2021 18:16:49 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 12 Nov 2021 18:16:49 GMT
ENV PYTHON_VERSION=3.9.8
# Fri, 12 Nov 2021 18:21:22 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 12 Nov 2021 18:21:23 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Nov 2021 18:21:23 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 12 Nov 2021 18:21:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 12 Nov 2021 18:21:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 12 Nov 2021 18:21:23 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 12 Nov 2021 18:21:30 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Nov 2021 18:21:30 GMT
CMD ["python3"]
# Sat, 13 Nov 2021 05:01:30 GMT
ENV HY_VERSION=1.0a3
# Sat, 13 Nov 2021 05:01:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Nov 2021 05:01:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b872f056719bde6e6722091afb2a3376d720c69c142b91ac352050080dd79615`  
		Last Modified: Fri, 12 Nov 2021 16:42:54 GMT  
		Size: 2.6 MB (2611155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f412b5d08d98838da7975a6a78d11e3afaa9100fa92d93f1a900ecaec6cd42`  
		Last Modified: Fri, 12 Nov 2021 18:59:21 GMT  
		Size: 684.1 KB (684068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d55ab9abc6f5ee5441a485766d64e21eaa1beaa479108b8e2994f538fb0686`  
		Last Modified: Fri, 12 Nov 2021 18:59:57 GMT  
		Size: 11.5 MB (11473096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c3ed017fb4f59874b081a15b1e53f3707239958417b3616729aa3be07ecf76`  
		Last Modified: Fri, 12 Nov 2021 18:59:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f604cd04b145cf5a26595edf77b2a343c6eddb49ff57fb91888b21a026ebd49`  
		Last Modified: Fri, 12 Nov 2021 18:59:56 GMT  
		Size: 2.3 MB (2348933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3187e605884109166b90480c6e7a47332d2a79ca7b1c9992b8abefeed3f68c39`  
		Last Modified: Sat, 13 Nov 2021 05:06:44 GMT  
		Size: 3.1 MB (3098025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
