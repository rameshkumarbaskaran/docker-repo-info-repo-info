## `hylang:python3.9-alpine`

```console
$ docker pull hylang@sha256:f3d0df467d78dd4770eefcc9ca1dc24bfc4c46945096e03185ddf6067a0fa2cf
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

### `hylang:python3.9-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:f8f088c438d6fb576e8334b74d25a3a0aa084fb98a01d18d3a6c7c1b83747fe6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20387170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33d2d3036d2f79afeacc43d69a4e5c782e0668a9463dcede9b74f45b4708159`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:37:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:11:33 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 21:11:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 06 Aug 2021 21:23:06 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 21:23:07 GMT
ENV PYTHON_VERSION=3.9.6
# Fri, 06 Aug 2021 21:30:00 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 06 Aug 2021 21:30:01 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 12 Aug 2021 21:33:21 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Thu, 12 Aug 2021 21:33:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Thu, 12 Aug 2021 21:33:22 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Thu, 12 Aug 2021 21:33:28 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 12 Aug 2021 21:33:29 GMT
CMD ["python3"]
# Thu, 12 Aug 2021 22:00:08 GMT
ENV HY_VERSION=1.0a3
# Thu, 12 Aug 2021 22:00:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 12 Aug 2021 22:00:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7905544193a12a0403a4adefebf29fc062dcaef14503592607f0b5bd84de00ca`  
		Last Modified: Fri, 06 Aug 2021 22:00:46 GMT  
		Size: 656.4 KB (656378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e5def5d5f7d9958b318f1fa52b3bb21146ad9287c12b6c7a44068178b9421a`  
		Last Modified: Fri, 06 Aug 2021 22:02:11 GMT  
		Size: 11.5 MB (11472889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef6c1fdc9e4cac180568966c3798ccdcbda510e239403471e8ebf951d8d9240`  
		Last Modified: Fri, 06 Aug 2021 22:02:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e85e6a20ef97c449024bcbb2c93bb70331991ce2c04b26da42f2f7dc59c992`  
		Last Modified: Thu, 12 Aug 2021 21:40:27 GMT  
		Size: 2.3 MB (2348894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c3543c093b47a9ca40fbfdf086d9f51689070644a0d104c6936fb21c96deed`  
		Last Modified: Thu, 12 Aug 2021 22:04:03 GMT  
		Size: 3.1 MB (3095772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:4776f759e293a79230df274b0574edd54f2568d34c39cf240ee44129bf86fe4b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19757465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041543faee6ebcab23b260c1cc967a97ebf45a60103198e6d6845ffe343d238d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 22:10:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 22:10:56 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 22:10:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 06 Aug 2021 22:26:24 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 22:26:25 GMT
ENV PYTHON_VERSION=3.9.6
# Fri, 06 Aug 2021 22:39:14 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 06 Aug 2021 22:39:17 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 13 Aug 2021 00:28:52 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 13 Aug 2021 00:28:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 13 Aug 2021 00:28:53 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 13 Aug 2021 00:29:11 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 13 Aug 2021 00:29:11 GMT
CMD ["python3"]
# Fri, 13 Aug 2021 02:02:30 GMT
ENV HY_VERSION=1.0a3
# Fri, 13 Aug 2021 02:02:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 13 Aug 2021 02:02:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77af9e0bf001b6117819159285db62ea39c525f4bdcf22afabbc103ddecd3388`  
		Last Modified: Fri, 06 Aug 2021 23:29:34 GMT  
		Size: 662.0 KB (661997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f935896bf57569e67b094e54eebaffd25a0a65835d9c95e7f3ee1ed6da66eeb0`  
		Last Modified: Fri, 06 Aug 2021 23:30:35 GMT  
		Size: 11.0 MB (11023866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83d51ae82155eb5e68f29d6b2feebcd5287b3f7cf28ec115aff1baf536af1e7`  
		Last Modified: Fri, 06 Aug 2021 23:30:26 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729aba95b1a2177a061a16d444bf35a7b990ade71e63fc0dcc6f2d784ae4a78`  
		Last Modified: Fri, 13 Aug 2021 00:36:32 GMT  
		Size: 2.3 MB (2348881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b969ddd28874e5ee712113f3a5ad3b35e51e5cb5443aa6bec0054ff4ceb705ed`  
		Last Modified: Fri, 13 Aug 2021 02:09:20 GMT  
		Size: 3.1 MB (3096138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:744b75a98855f701176571a2ce353128ab52462ec75b20cb3d424c3914248ac9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19066409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25345ac29745c46cdcab0b5f59733202424a25ff3ae4be5a4c70a2b35fb98e8b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 23:39:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 23:39:14 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 23:39:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 06 Aug 2021 23:52:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 23:52:54 GMT
ENV PYTHON_VERSION=3.9.6
# Sat, 07 Aug 2021 00:03:41 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 07 Aug 2021 00:03:43 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 07 Aug 2021 00:03:43 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Sat, 07 Aug 2021 00:03:44 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Sat, 07 Aug 2021 00:03:44 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Sat, 07 Aug 2021 00:04:01 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 07 Aug 2021 00:04:01 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 07:25:44 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 07:25:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 07:25:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2abd71660dfee6728fd561a2bec4120e5048a413649e0b7abfe7f3a22b238c`  
		Last Modified: Sat, 07 Aug 2021 00:59:18 GMT  
		Size: 655.2 KB (655210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb40097973eb2406a12e9efbaa824c88149741d1238bdf50861148547c341ca`  
		Last Modified: Sat, 07 Aug 2021 01:01:19 GMT  
		Size: 10.5 MB (10531076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7296a96d484afaf23af391c121b983db4155ebaa74f18f7603469c42786c72c`  
		Last Modified: Sat, 07 Aug 2021 01:01:13 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec0d074fb01af37bf8e385b55190293cea2a97b40c96ec62ee1a7cdcd43820`  
		Last Modified: Sat, 07 Aug 2021 01:01:14 GMT  
		Size: 2.4 MB (2355293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5382f8f213dbd0ef94e6e48bbb8bed085dd846990cb0b27980638b8a652f404`  
		Last Modified: Sat, 07 Aug 2021 07:36:52 GMT  
		Size: 3.1 MB (3095237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c00a80f7433be44c0e07fe5b1bcaa67e162a21fb6da4162553b241b2dd346c43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20339779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea14f6e096ee18f9f5cc3c7bd4ebf0d9d3cb66dba41b3f017589129e390fc65f`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:48:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 23:28:08 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 23:28:10 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 06 Aug 2021 23:36:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 23:36:08 GMT
ENV PYTHON_VERSION=3.9.6
# Fri, 06 Aug 2021 23:42:23 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 06 Aug 2021 23:42:24 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 23:42:24 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 23:42:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 23:42:24 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 23:42:31 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 23:42:32 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 04:08:26 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 04:08:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 04:08:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8658fe6f1167429e7a1eb051477cf244d81bbf3ceb3595703ecd1ee1eea42f10`  
		Last Modified: Sat, 07 Aug 2021 00:12:16 GMT  
		Size: 658.8 KB (658828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b11b8a71f54ed5e419bbd81bed60a6d116e1324828c8635b312905580c76d`  
		Last Modified: Sat, 07 Aug 2021 00:13:49 GMT  
		Size: 11.5 MB (11519763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb203dc11a6d62341cb60abe2b34025613c71611b95e5d1ecb02dc221c84a553`  
		Last Modified: Sat, 07 Aug 2021 00:13:47 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e32ff9ba9f00fe39768e6bb0657f51764ee4395f745a8122eadbb3d9aa6d6aa`  
		Last Modified: Sat, 07 Aug 2021 00:13:48 GMT  
		Size: 2.4 MB (2355254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad73d18d112025dec3df4762617a5515956afdb250eb47b89a193ec8d26c8f76`  
		Last Modified: Sat, 07 Aug 2021 04:14:11 GMT  
		Size: 3.1 MB (3095090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine` - linux; 386

```console
$ docker pull hylang@sha256:f2f1749b1ea7469e043fa064a229d9d2925b9981dc73d93d231396b616221c4f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20589797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473292c31feda3b6f7a509d12e166c36e2c1bb07c9368d9a9349f847b591b929`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 22:30:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 22:30:10 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 22:30:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 06 Aug 2021 22:39:19 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 22:39:20 GMT
ENV PYTHON_VERSION=3.9.6
# Fri, 06 Aug 2021 22:47:05 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 06 Aug 2021 22:47:06 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 12 Aug 2021 21:40:04 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Thu, 12 Aug 2021 21:40:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Thu, 12 Aug 2021 21:40:05 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Thu, 12 Aug 2021 21:40:12 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 12 Aug 2021 21:40:13 GMT
CMD ["python3"]
# Thu, 12 Aug 2021 22:11:25 GMT
ENV HY_VERSION=1.0a3
# Thu, 12 Aug 2021 22:11:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 12 Aug 2021 22:11:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff2d714abf347ae20c3cd57a6f612ce68eba17d9e9817a7e5296ce1933b8e8d`  
		Last Modified: Sat, 07 Aug 2021 02:19:29 GMT  
		Size: 664.2 KB (664187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6271c41ae5499d75d442799c69031d7c4878f4ff4b2f56d1e2f18a285f8bc1a7`  
		Last Modified: Sat, 07 Aug 2021 02:21:03 GMT  
		Size: 11.7 MB (11658670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e943d755b0758338bbb8a390ee8f86697dac7c5eab6c95ca6a9517d5412e9790`  
		Last Modified: Sat, 07 Aug 2021 02:21:01 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15522761da11bd955724d39890b9e4d16e52452406e8f3835ad8d2ccef82bf5`  
		Last Modified: Thu, 12 Aug 2021 21:50:27 GMT  
		Size: 2.3 MB (2348875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822600eedacf26f062f92cb0e6c15bb7d9c0669836d6a2ca6949a132c48a7ca6`  
		Last Modified: Thu, 12 Aug 2021 22:17:51 GMT  
		Size: 3.1 MB (3095922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:aa9c8772e684d77301cdb252811f9d64629479a5adf0470ea0c0afd3dfd6e0e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20697396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a801b72339a47095f5cef9f87232b429295233550ff4200debaba5d8a28db31e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:34:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 18:34:35 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 18:34:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 06 Aug 2021 18:50:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 18:50:59 GMT
ENV PYTHON_VERSION=3.9.6
# Fri, 06 Aug 2021 18:59:45 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 06 Aug 2021 19:00:00 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 19:00:09 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 19:00:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 19:00:30 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 19:01:04 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 19:01:13 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 03:39:03 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 03:39:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 03:39:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ddf08a980cdecf274decc9996762a7bc2efb4793cee39d33eda999b6188ee1`  
		Last Modified: Fri, 06 Aug 2021 19:50:59 GMT  
		Size: 665.0 KB (665045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd6083e19f39b48d1a24b20e7a9963d7b5d19b1799ef5f9a80795872d39ab85`  
		Last Modified: Fri, 06 Aug 2021 19:52:30 GMT  
		Size: 11.8 MB (11770098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49666f814315e84422d53d516962af81a79458d5acaa50d4c2a9d09b0cc0eacc`  
		Last Modified: Fri, 06 Aug 2021 19:52:28 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096a5c84d6f8eb9f8f1c9f0e16df574f4fd4c583380675115e5aedc894f80063`  
		Last Modified: Fri, 06 Aug 2021 19:52:28 GMT  
		Size: 2.4 MB (2355278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b254f49a2c578d1c84cb9b93a393a3d0665d4e86558db9a770f83b82edd97f`  
		Last Modified: Sat, 07 Aug 2021 03:58:30 GMT  
		Size: 3.1 MB (3095591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:a1897299aa322375702c3755b4138e95fe219d36ad7e9fbde1ecaaff8f1e81ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20566657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950c2bfedff8d7729758cefb26818d9a3ad901ea228c7898438ec2c2307f7e3f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Jun 2021 21:55:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Jun 2021 21:55:22 GMT
ENV LANG=C.UTF-8
# Sat, 26 Jun 2021 21:55:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sun, 27 Jun 2021 01:13:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sun, 27 Jun 2021 01:13:54 GMT
ENV PYTHON_VERSION=3.9.5
# Tue, 29 Jun 2021 06:30:50 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 29 Jun 2021 06:30:51 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 29 Jun 2021 06:30:52 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Tue, 29 Jun 2021 06:30:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Tue, 29 Jun 2021 06:30:52 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Tue, 29 Jun 2021 06:30:59 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Jun 2021 06:31:00 GMT
CMD ["python3"]
# Tue, 29 Jun 2021 11:52:28 GMT
ENV HY_VERSION=1.0a1
# Tue, 29 Jun 2021 11:52:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 29 Jun 2021 11:52:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb495fdd4ed44cfbdc940f19d8911ce5b6c192e1c4d5979a35af8139d5a70320`  
		Last Modified: Sun, 27 Jun 2021 11:32:17 GMT  
		Size: 661.5 KB (661534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2d1ac6f8fdd09a985867664c85eaa501672057a21d5bd16b863c0b80603ec6`  
		Last Modified: Tue, 29 Jun 2021 06:51:06 GMT  
		Size: 11.8 MB (11824777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc0761aea59ede72b849c64c80bb0ef5380f36dea098e1b0e0aa61311660f59`  
		Last Modified: Tue, 29 Jun 2021 06:51:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84830115f53bb654aed6db34f75253c937b61d7f9880a8d0f7dd610c019b6485`  
		Last Modified: Tue, 29 Jun 2021 06:51:05 GMT  
		Size: 2.3 MB (2348407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af0a885f99f951670225172cadc01e7815b2f1d96235d497c9d140f6832bcbd`  
		Last Modified: Tue, 29 Jun 2021 11:58:07 GMT  
		Size: 3.1 MB (3129056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
