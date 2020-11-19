## `hylang:0-python3.6-stretch`

```console
$ docker pull hylang@sha256:673900f50e1260d959c378789e83dc4a7e0a9696b0e98010806179c774261fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-python3.6-stretch` - linux; amd64

```console
$ docker pull hylang@sha256:2d0001c8dde2a428e9517c0570495d9695d954cd34fbe37c18a9455bcb9f2a3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39820583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b28e9dc798e13e365e9532c2ee2b9807e853e61806daa4bb47834cf6844400`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:29 GMT
ADD file:02294bc9e72a3f3314955f0b5e0e728cd75321e88a1fae9bfbac77c76bfaf05d in / 
# Tue, 17 Nov 2020 20:24:29 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 14:30:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 14:30:49 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 14:30:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 14:30:57 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 18 Nov 2020 15:03:59 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 18 Nov 2020 15:11:09 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 18 Nov 2020 15:11:11 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 18 Nov 2020 15:11:12 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 15:11:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 15:11:12 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 15:11:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 15:11:37 GMT
CMD ["python3"]
# Thu, 19 Nov 2020 05:38:14 GMT
ENV HY_VERSION=0.19.0
# Thu, 19 Nov 2020 05:38:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 19 Nov 2020 05:38:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4297e02295585beb3f148a5740b644ce87e059455f8d98a5adb7bf95105e011c`  
		Last Modified: Tue, 17 Nov 2020 20:30:42 GMT  
		Size: 22.5 MB (22527663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bfea12ab8f7795f335db711d42f08b6859102eeb3bacbb155fc4ab71931a7f`  
		Last Modified: Wed, 18 Nov 2020 15:15:04 GMT  
		Size: 2.5 MB (2485492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62175f2f172df64ad97f84c398f5340ae79fbd72232bd69485579f38db50b621`  
		Last Modified: Wed, 18 Nov 2020 15:15:42 GMT  
		Size: 9.6 MB (9635768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f36e2c0e8260f27bc37045752154c72a3f6d33f7df4a75ddd43c68465886a9`  
		Last Modified: Wed, 18 Nov 2020 15:15:40 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bbd4b9185acced9aac51df2c714337252b0d4e17b359d9fb702d53f3a25a7`  
		Last Modified: Wed, 18 Nov 2020 15:15:40 GMT  
		Size: 2.4 MB (2403793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f775d8020f08570b4153e3be14385009113a2fffb19d852a64e1a692fed650f4`  
		Last Modified: Thu, 19 Nov 2020 05:40:58 GMT  
		Size: 2.8 MB (2767627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-stretch` - linux; arm variant v5

```console
$ docker pull hylang@sha256:a38842337aa542c3f0ecfba96377857f74f42e62256e5e95b80c18cbb4bf599a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37788760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1f5a6418bedb398230457a606d5e0f20181b9b3500467bd28958be8154990d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:25:42 GMT
ADD file:4b15e8e11181891542668a0a93beec0ef2d10d06bf813588d697bf2aae6d5301 in / 
# Tue, 17 Nov 2020 20:25:56 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 00:23:35 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 00:23:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:23:53 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 18 Nov 2020 01:05:40 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 18 Nov 2020 01:12:09 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 18 Nov 2020 01:12:15 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 18 Nov 2020 01:12:17 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 01:12:18 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 01:12:20 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 01:12:58 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 01:12:58 GMT
CMD ["python3"]
# Wed, 18 Nov 2020 10:58:44 GMT
ENV HY_VERSION=0.19.0
# Wed, 18 Nov 2020 10:58:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 18 Nov 2020 10:58:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:382487580b44ddc72314007ebce0b542eea5cfc9708c8adc57904b41e3dea712`  
		Last Modified: Tue, 17 Nov 2020 20:34:54 GMT  
		Size: 21.2 MB (21202085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bf2198b941c7afb393009eaa4513322e3d3483100a8835bb52e53e7a7490c3`  
		Last Modified: Wed, 18 Nov 2020 01:16:06 GMT  
		Size: 2.2 MB (2216222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07729c905ec01d31b6d0db4d973520838d743c94221ca74b4c33c30aab7c91aa`  
		Last Modified: Wed, 18 Nov 2020 01:16:59 GMT  
		Size: 9.2 MB (9198316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2743c712102c772a7442a54763f3b26c9d13b88baa3e2e7d8639aec2f55c52`  
		Last Modified: Wed, 18 Nov 2020 01:16:55 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80ac68cac65f28ab3808b71c076ad46db0b3fd7d750f39b147648c5ed2f38d3`  
		Last Modified: Wed, 18 Nov 2020 01:16:56 GMT  
		Size: 2.4 MB (2403912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5135952b97309eebfbfa2dd712d41cade2255b7120fc1016ea0f6906a27017e9`  
		Last Modified: Wed, 18 Nov 2020 11:00:18 GMT  
		Size: 2.8 MB (2767982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-stretch` - linux; arm variant v7

```console
$ docker pull hylang@sha256:72c6d3b941a2b5fc9ffd1b4f791686754b7e09d4cae44528bac161e17818c4f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35560692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3b975773b9a650c5409b0c34a4b9babeace618433208adcc2244a81f6b7d7a`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:23 GMT
ADD file:de081793a94d15fb89877812e1c838c9e3836070e36a6fb7f01b858a884b6680 in / 
# Tue, 17 Nov 2020 20:27:24 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 06:05:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 06:05:56 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 06:06:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 06:06:09 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 18 Nov 2020 06:50:52 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 18 Nov 2020 07:00:20 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 18 Nov 2020 07:00:22 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 18 Nov 2020 07:00:23 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 07:00:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 07:00:24 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 07:01:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 07:01:41 GMT
CMD ["python3"]
# Wed, 18 Nov 2020 23:04:36 GMT
ENV HY_VERSION=0.19.0
# Wed, 18 Nov 2020 23:05:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 18 Nov 2020 23:05:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a97dc136886474245bdc5c70c58e70e18fc55d193dae8225f0543e0b500b484a`  
		Last Modified: Tue, 17 Nov 2020 20:35:46 GMT  
		Size: 19.3 MB (19313228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd71f119f1eac78351079d13b0012aeed9f55e588257718295d6c8ff6e45064`  
		Last Modified: Wed, 18 Nov 2020 07:05:14 GMT  
		Size: 2.1 MB (2137391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be5fda875e778262bf6e13d72a0a0ad9279c6581ad476e7b988a7789ccc7d7`  
		Last Modified: Wed, 18 Nov 2020 07:06:10 GMT  
		Size: 8.9 MB (8937650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df05d3af1db18c5a288372d84f4a9c7c8e4f45bd3966c974abb0fcfe7c13f63`  
		Last Modified: Wed, 18 Nov 2020 07:06:07 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec2baf8a8bb167b80b40fc7d8e049a5591ebe418ab115143dbc13b8a50cbb63`  
		Last Modified: Wed, 18 Nov 2020 07:06:08 GMT  
		Size: 2.4 MB (2404009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968dcd7e0a4181cb9867ca7e16aac56f04c49218139c7cd4596deb2440b04f3`  
		Last Modified: Wed, 18 Nov 2020 23:08:15 GMT  
		Size: 2.8 MB (2768173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-stretch` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:84def3c07552d1556c093883280c68a1024e8c082007054e3d5a895d61ab9bd8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37116258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9955af375a659f63ba7259fbff22d5ce0658e2d2824e41aa8e0efaef7e94a00`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:28:08 GMT
ADD file:b5b22f625d299254bffe6243b53eb5867cecdaab5c226e41411fa55763587755 in / 
# Tue, 17 Nov 2020 20:28:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:08:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 08:08:46 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 08:09:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:09:03 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 18 Nov 2020 08:49:40 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 18 Nov 2020 08:58:00 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 18 Nov 2020 08:58:02 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 18 Nov 2020 08:58:03 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 08:58:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 08:58:04 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 08:58:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 08:58:30 GMT
CMD ["python3"]
# Thu, 19 Nov 2020 02:51:52 GMT
ENV HY_VERSION=0.19.0
# Thu, 19 Nov 2020 02:52:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 19 Nov 2020 02:52:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f37c1cd284d6b059670ae5ae080ea2b30b095b4328a6580f4f0d90ef0da06b9a`  
		Last Modified: Tue, 17 Nov 2020 20:34:38 GMT  
		Size: 20.4 MB (20387780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17ce0dacce6719728179018a24c395796525112e8f0bbd874e8c8bb2e92b830`  
		Last Modified: Wed, 18 Nov 2020 09:02:36 GMT  
		Size: 2.2 MB (2199095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114d2a474b05e1c6203152e955c348cb801e08718c2d82236d998db0de064cde`  
		Last Modified: Wed, 18 Nov 2020 09:03:34 GMT  
		Size: 9.4 MB (9357501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5430f6b957d7268183fcb13a350fac8501fef5b831482391a566cc07ed859e`  
		Last Modified: Wed, 18 Nov 2020 09:03:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c57ed09bdda45bde76bf8caeeee859d84de19437c2b7eb3efdf3f96502058e`  
		Last Modified: Wed, 18 Nov 2020 09:03:32 GMT  
		Size: 2.4 MB (2403603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed19a07609ed2e48cb6764793ef529f382f5da05f94876e99be186b99f15bd3b`  
		Last Modified: Thu, 19 Nov 2020 02:55:43 GMT  
		Size: 2.8 MB (2768039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-stretch` - linux; 386

```console
$ docker pull hylang@sha256:9840bf342abc10f81e226bc10212481805af71c85ccb0007a16e1f43aecc1e15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40531260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfeee0a0820cefc202649858e69aef9262bb986c0d583cca71ac7111faebaa6`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:25 GMT
ADD file:6d0d227a50cb77b9603ef598794fe0f583312a776daf61e7cd7e5493260354c9 in / 
# Tue, 17 Nov 2020 20:23:25 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 14:45:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 14:45:41 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 14:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 14:45:49 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 18 Nov 2020 15:32:11 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 18 Nov 2020 15:42:13 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 18 Nov 2020 15:42:14 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 18 Nov 2020 15:42:14 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 15:42:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 15:42:15 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 15:42:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 15:42:39 GMT
CMD ["python3"]
# Wed, 18 Nov 2020 16:41:42 GMT
ENV HY_VERSION=0.19.0
# Wed, 18 Nov 2020 16:41:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 18 Nov 2020 16:41:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:657537e4548aa71eaa79344d36c62360306a66e11486f3d90ce21ecef49a62cb`  
		Last Modified: Tue, 17 Nov 2020 20:30:22 GMT  
		Size: 23.2 MB (23154739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbffcc6adc18c796e73842dee3c39506d398abcd674265b247a8945aa46a86aa`  
		Last Modified: Wed, 18 Nov 2020 15:46:09 GMT  
		Size: 2.5 MB (2490168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4c33e2d94a433016cd0e3450a182ffd12d403d88d173fe029f4410af45a936`  
		Last Modified: Wed, 18 Nov 2020 15:46:54 GMT  
		Size: 9.7 MB (9714873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49b64e83f820a596ffd84bb9ae7d6afa1682df38d79835ef0906c8fdc69b083`  
		Last Modified: Wed, 18 Nov 2020 15:46:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3af7928c5e4d7fc3598ea4e69b2c64d65659bb9f761db00fdc7d7f5a4ee1e7`  
		Last Modified: Wed, 18 Nov 2020 15:46:52 GMT  
		Size: 2.4 MB (2403668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e71eb54d7ac8c695a30b90c24747bb9d6e0e16c1bd21ea2144053a9bc602a0`  
		Last Modified: Wed, 18 Nov 2020 16:44:10 GMT  
		Size: 2.8 MB (2767572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
