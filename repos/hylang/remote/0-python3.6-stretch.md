## `hylang:0-python3.6-stretch`

```console
$ docker pull hylang@sha256:bf76835ff5ee4e16d93f5dc5c27578b23ea88e0675e9fe5d6e1d73846912d94f
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
$ docker pull hylang@sha256:8081e3591cc3bbdf8a228699a2785add455a9259462dd68d26d05b0eb037b2b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39907132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24404638a74d418af9b2eba6323e1862e3f42c9b19c2ee65bdaf157fe4787`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:47 GMT
ADD file:1d706af4169332956a23f3faa02754cb503003812cc1d43ad9b2448f7c26f431 in / 
# Fri, 12 Mar 2021 02:22:48 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 20:29:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 20:29:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 20:29:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 20:29:48 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 12 Mar 2021 21:21:11 GMT
ENV PYTHON_VERSION=3.6.13
# Fri, 12 Mar 2021 21:26:56 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 12 Mar 2021 21:26:57 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Mar 2021 21:26:58 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 12 Mar 2021 21:26:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 12 Mar 2021 21:26:58 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 12 Mar 2021 21:27:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Mar 2021 21:27:12 GMT
CMD ["python3"]
# Sat, 13 Mar 2021 11:50:13 GMT
ENV HY_VERSION=0.20.0
# Sat, 13 Mar 2021 11:50:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Mar 2021 11:50:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a4feded82f54dd43cb68930d190cb6715378fa2aca3ecce0bcac959359f58d2f`  
		Last Modified: Fri, 12 Mar 2021 02:30:28 GMT  
		Size: 22.5 MB (22528907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a62f3d6dc66d2e4296f3490b089ffea99f9a6348d312cd417718ef4dd9cb63`  
		Last Modified: Fri, 12 Mar 2021 21:47:07 GMT  
		Size: 2.5 MB (2486277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2fd80bd1e973381642b50f4b35a825183939d0846e90a3d8f6dac8e09a6869`  
		Last Modified: Fri, 12 Mar 2021 21:48:34 GMT  
		Size: 9.6 MB (9630924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfeb958e1000ff11db76924d043b6c21028c713ded0dfa597ee3fd0fe04f504e`  
		Last Modified: Fri, 12 Mar 2021 21:48:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4011ec7966a2d06c395d27fbbe639589a079e636a03ae4c2b37ca8ab4f1b3f86`  
		Last Modified: Fri, 12 Mar 2021 21:48:33 GMT  
		Size: 2.4 MB (2447343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc47ab40288121f092f3a0f333bde0e1af0e5a2edcadc6b36d95373bb5bd72a`  
		Last Modified: Sat, 13 Mar 2021 11:55:59 GMT  
		Size: 2.8 MB (2813441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-stretch` - linux; arm variant v5

```console
$ docker pull hylang@sha256:57353cf178d63cfa4ae09d3b9dd88b13165759bf3cafac8b928e8297697ce8d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37887541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66387a1dfe9e609471a8f93e80ef17e54a73b26143436131120c1e3662a199c9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 26 Mar 2021 07:56:05 GMT
ADD file:470a3146a29008b0319015ce05eb2ef75f275c3d1bd498a497e5f9d923979149 in / 
# Fri, 26 Mar 2021 07:56:07 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 16:19:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 16:20:00 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 16:20:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 16:20:19 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 26 Mar 2021 16:58:09 GMT
ENV PYTHON_VERSION=3.6.13
# Fri, 26 Mar 2021 17:03:56 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 26 Mar 2021 17:03:59 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 17:04:00 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 17:04:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 17:04:02 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 17:04:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 17:04:36 GMT
CMD ["python3"]
# Sat, 27 Mar 2021 00:15:11 GMT
ENV HY_VERSION=0.20.0
# Sat, 27 Mar 2021 00:15:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 27 Mar 2021 00:15:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803c12310b081195c1e4702515481306ff066aca97b288702f49d3f9bc65d018`  
		Last Modified: Fri, 26 Mar 2021 08:04:36 GMT  
		Size: 21.2 MB (21203931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa3ed229e74409218bd1b973dbcafc24bce53b2a40bdfa8a70b14965cbabd47`  
		Last Modified: Fri, 26 Mar 2021 17:09:39 GMT  
		Size: 2.2 MB (2230989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131dd989e9866d90778a4b9cff37e41ed2203193e597ab31953864d0ffa645bc`  
		Last Modified: Fri, 26 Mar 2021 17:10:59 GMT  
		Size: 9.2 MB (9191003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f8e1d52cc9de5e2713824d96444e738323ba05ed3bac6ce3fe1f50900636f3`  
		Last Modified: Fri, 26 Mar 2021 17:10:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1d7521b5fb842de5949d660e1670ddc3d33f6a828bc7bd1d4799e5ce82177a`  
		Last Modified: Fri, 26 Mar 2021 17:10:57 GMT  
		Size: 2.4 MB (2447462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992dc980dd5cb797437318ae681101dbe5bf589e5d9d1c8ca6cc2a465bf149f`  
		Last Modified: Sat, 27 Mar 2021 00:16:53 GMT  
		Size: 2.8 MB (2813917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-stretch` - linux; arm variant v7

```console
$ docker pull hylang@sha256:559b3b46738ea493986417136f66216acbeb3cdab8ba94eead4c2515ff5d6940
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35670646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e63be793c155a4aee70d1e8a5445961defb77135d4ce01d8fac3f436f88cd01`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:47 GMT
ADD file:b1a5bfd28534bad7b8c5855866772582382ed83f0066f18ee2a8641adfd9ba0c in / 
# Fri, 26 Mar 2021 11:22:49 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 21:56:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 21:56:17 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 21:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 21:56:33 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 26 Mar 2021 22:40:48 GMT
ENV PYTHON_VERSION=3.6.13
# Fri, 26 Mar 2021 22:49:19 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 26 Mar 2021 22:49:22 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 22:49:24 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 22:49:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 22:49:26 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 22:49:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 22:49:58 GMT
CMD ["python3"]
# Sat, 27 Mar 2021 16:17:19 GMT
ENV HY_VERSION=0.20.0
# Sat, 27 Mar 2021 16:17:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 27 Mar 2021 16:17:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f45436284e34e941cb0711d5901be5a1fd36d7b444c793225978d28caa2fe50c`  
		Last Modified: Fri, 26 Mar 2021 11:31:36 GMT  
		Size: 19.3 MB (19315624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bc889cd1811defab10050faf7d8d1e29796b0209b9da143c8dc40f96869317`  
		Last Modified: Fri, 26 Mar 2021 22:54:17 GMT  
		Size: 2.2 MB (2152078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364958f4b85f31a6e0bae62d3bcaed2ae6a92fdded4db35881dbba8b6c9a74ed`  
		Last Modified: Fri, 26 Mar 2021 22:55:09 GMT  
		Size: 8.9 MB (8941410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0ddc8a3da6a02c071d9d421b77de14b3cf6291fedb6564fa9b1ff7dd4a02ef`  
		Last Modified: Fri, 26 Mar 2021 22:55:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408360225fc36e3d877e858032ebad21746354e93641c62c75ddfead8b78b377`  
		Last Modified: Fri, 26 Mar 2021 22:55:08 GMT  
		Size: 2.4 MB (2447458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6330266597b87cd3cf5d9c5ec8b86a0194de77c60f4c573dcd0947e5ade57ba`  
		Last Modified: Sat, 27 Mar 2021 16:20:03 GMT  
		Size: 2.8 MB (2813836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-stretch` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d1bdaa5eab567e4d4eb5c0c6a9a6be6b698a550053a1eb436d11eb12f60252d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37208771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9221181a97192f9277d7711c627526fd8a2e8b7f053b027bb49afa13e94fed9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Mar 2021 01:57:19 GMT
ADD file:cd70de3ff9dab2f20378f87a36ca54171a79fde726291a9c5c7eae7b5435cfa2 in / 
# Fri, 12 Mar 2021 01:57:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 15:47:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 15:48:00 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 15:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 15:48:13 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 12 Mar 2021 16:30:39 GMT
ENV PYTHON_VERSION=3.6.13
# Fri, 12 Mar 2021 16:38:45 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 12 Mar 2021 16:38:48 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Mar 2021 16:38:49 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 12 Mar 2021 16:38:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 12 Mar 2021 16:38:51 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 12 Mar 2021 16:39:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Mar 2021 16:39:20 GMT
CMD ["python3"]
# Sat, 13 Mar 2021 05:15:08 GMT
ENV HY_VERSION=0.20.0
# Sat, 13 Mar 2021 05:15:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Mar 2021 05:15:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9cb8532b12b699d7151babb99e22315d94bfbf317f3c1db01c532a61fc38a748`  
		Last Modified: Fri, 12 Mar 2021 02:04:16 GMT  
		Size: 20.4 MB (20389391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6438ecd1f8d0ad90425db0407e287ff2afb8db5a27995ca7bab6bd66562ad`  
		Last Modified: Fri, 12 Mar 2021 16:43:43 GMT  
		Size: 2.2 MB (2199392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edd9fed168b07561a9d63cde9dafa1852c804ee6e6767c5db0f0251ac4c76ad`  
		Last Modified: Fri, 12 Mar 2021 16:44:42 GMT  
		Size: 9.4 MB (9358907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d5d358f58ffed5fc27fe03b9f75aba5486bd1a11a936ca38472c1a0925e964`  
		Last Modified: Fri, 12 Mar 2021 16:44:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb4760a7274e3444781ebf2e3d9ffd04706d079316968b97a22033ec50f7768`  
		Last Modified: Fri, 12 Mar 2021 16:44:41 GMT  
		Size: 2.4 MB (2446954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0357152ede5c0b2c0b4f9a460ba11acabf990473ef4f3af47e84781e201552`  
		Last Modified: Sat, 13 Mar 2021 05:19:11 GMT  
		Size: 2.8 MB (2813887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-stretch` - linux; 386

```console
$ docker pull hylang@sha256:0bef0da694b855eaf18156c99f879de374618d82efccf98610394a27045f4f48
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40641487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3632e9f651b781cde004dee029a1288bc5c04cd8aea1fc400d6cb2fbc0556c3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 26 Mar 2021 13:56:15 GMT
ADD file:91732be8769ce7a48c8edbcacde510467db8bf638bbaa006e2c16b934db4b194 in / 
# Fri, 26 Mar 2021 13:56:16 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 19:39:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 19:39:14 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 19:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 19:39:23 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 26 Mar 2021 20:07:13 GMT
ENV PYTHON_VERSION=3.6.13
# Fri, 26 Mar 2021 20:14:15 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 26 Mar 2021 20:14:16 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 20:14:17 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 20:14:17 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 20:14:17 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 20:14:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 20:14:35 GMT
CMD ["python3"]
# Sat, 27 Mar 2021 08:08:59 GMT
ENV HY_VERSION=0.20.0
# Sat, 27 Mar 2021 08:09:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 27 Mar 2021 08:09:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a3bf74280798a5f5e64bcdb089e5b7574c9548f225981dcae24575c66cba2af`  
		Last Modified: Fri, 26 Mar 2021 14:07:05 GMT  
		Size: 23.2 MB (23156367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebae4301fda2d4c906f873168ee3e0821034413369ea681e96017dd8da4f6ef4`  
		Last Modified: Fri, 26 Mar 2021 20:20:45 GMT  
		Size: 2.5 MB (2509040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ec051c7bc6c918fe7d9bcc87384dcd61e340feae3551c203b3bd4e434c8d2`  
		Last Modified: Fri, 26 Mar 2021 20:21:57 GMT  
		Size: 9.7 MB (9714950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9346f398344bc34f74940787f8e7b4e25ebd1756d74af8dfad729d99491456`  
		Last Modified: Fri, 26 Mar 2021 20:21:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afbe0e366624181b96703e0d85409dfbc7b7efbc1b61473dd475ebc12cfde04`  
		Last Modified: Fri, 26 Mar 2021 20:21:55 GMT  
		Size: 2.4 MB (2447357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceeafc52930b36b911c0e91a752e5f09217d4c5ac31b604d480de8fb5a9bedc`  
		Last Modified: Sat, 27 Mar 2021 08:17:26 GMT  
		Size: 2.8 MB (2813533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
