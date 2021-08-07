## `hylang:python3.7-stretch`

```console
$ docker pull hylang@sha256:afcbcd053b73dbf3af5a8787f5c95d6f31fef124f9a77384b62f91e9b44aa493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:python3.7-stretch` - linux; amd64

```console
$ docker pull hylang@sha256:35fbdea65403350c913051d0c59a8c50ea137440dae0d8a88590f3ea2be5e3c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40728182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4df0ce340b7e772b159e6f96426497f0bf0b528896c0ac28bc12bf951cd1bd`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:17 GMT
ADD file:55a25b93e8f2940a796f3cbf1e78bddf5f49c46b1b89b63b9b5673cbed9483ca in / 
# Thu, 22 Jul 2021 00:47:17 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 16:08:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 16:08:30 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 16:08:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 16:08:37 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 22 Jul 2021 16:08:38 GMT
ENV PYTHON_VERSION=3.7.11
# Thu, 22 Jul 2021 16:15:43 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 16:15:44 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 21:38:09 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 21:38:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 21:38:10 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 21:38:22 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 21:38:23 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 02:32:25 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 02:32:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 02:32:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:778066204fb734c2fb80cb8127cb35d67d742806a4eaf1aba0b5393c4ae6f2a4`  
		Last Modified: Thu, 22 Jul 2021 00:53:22 GMT  
		Size: 22.5 MB (22527428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0036158cfada887e9e472c44b22307e0b37f084c2ab602660a4cf0d12ca8003c`  
		Last Modified: Thu, 22 Jul 2021 16:45:21 GMT  
		Size: 2.5 MB (2506159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4641e3c54218af3381125ac68b20f61e549f2806036b497cd046a6d99ae2d48f`  
		Last Modified: Thu, 22 Jul 2021 16:45:22 GMT  
		Size: 10.0 MB (10004968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63de095ae3f46f99183b10d1c1518c7d55565bf70d7d1065ef4b403f4cb05b7`  
		Last Modified: Thu, 22 Jul 2021 16:45:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d703690f5e0ac5776a5b6b69b00fb6825f1199c30cccda93c9cb4ef4c97e1ae`  
		Last Modified: Fri, 06 Aug 2021 22:04:30 GMT  
		Size: 2.6 MB (2638504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b6140b4d0fd78a11741f8191482870fa2122aa7a4d122eb3cb508bb715e7c`  
		Last Modified: Sat, 07 Aug 2021 02:37:15 GMT  
		Size: 3.1 MB (3050883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-stretch` - linux; arm variant v5

```console
$ docker pull hylang@sha256:fe05ec76a85af7b9a1b3e7932d55812c96cbb5eb64c9cbc209cf2d9ecb593e0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38476218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ef59414c5873562589ca80cbace107960d5d443993ac024b04a90df2ff7e7c`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:53:35 GMT
ADD file:15b3f2121b39bbc6e8b5dae83180128e0dbf1c86ea4d9f81533ed493efcc6dc8 in / 
# Thu, 22 Jul 2021 00:53:36 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:54:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 04:54:16 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 04:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:54:43 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 22 Jul 2021 04:54:43 GMT
ENV PYTHON_VERSION=3.7.11
# Thu, 22 Jul 2021 05:07:19 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 05:07:21 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 19:45:44 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 19:45:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 19:45:45 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 19:46:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 19:46:24 GMT
CMD ["python3"]
# Fri, 06 Aug 2021 20:58:14 GMT
ENV HY_VERSION=1.0a3
# Fri, 06 Aug 2021 20:58:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 06 Aug 2021 20:58:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7900ccce3a65cf4889d5e7618644bba320a4667d14e5987da7b26a95ccc8e1f3`  
		Last Modified: Thu, 22 Jul 2021 01:07:10 GMT  
		Size: 21.2 MB (21204360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7b68ee7f81a28e0f6337f75cd72c899f562a59e667c1e32dee3cb10d78cda1`  
		Last Modified: Thu, 22 Jul 2021 05:57:41 GMT  
		Size: 2.2 MB (2231137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c630420323ef5ef654a4f1397df306e8c52359694ed721bcd478f18046bcc66d`  
		Last Modified: Thu, 22 Jul 2021 05:57:47 GMT  
		Size: 9.4 MB (9351019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a87142f7d00a1bf785bdd9523a67261bfedc2a1e71376995f237a739a943da`  
		Last Modified: Thu, 22 Jul 2021 05:57:40 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97dbe725c71570aada3e3e16f5630da9ebaf0cab733f59a11d612fc35fe7671`  
		Last Modified: Fri, 06 Aug 2021 19:57:46 GMT  
		Size: 2.6 MB (2638321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4ad5c7c5c0e010f18592ad00417484b411799af399c01204215933059c7161`  
		Last Modified: Fri, 06 Aug 2021 21:02:43 GMT  
		Size: 3.1 MB (3051141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-stretch` - linux; arm variant v7

```console
$ docker pull hylang@sha256:ed3f923db64e956dac5a3094c34d9b6f90cc1cb26f4c841edaef711b086fdafa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36453036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a8a7a2792a39e0d9dee4047f648543b6ddb10261fec64467fd99b263a16cb5`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 00:16:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 00:16:43 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 00:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:17:05 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 23 Jul 2021 00:17:06 GMT
ENV PYTHON_VERSION=3.7.11
# Fri, 23 Jul 2021 00:32:39 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 23 Jul 2021 00:32:40 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 07 Aug 2021 00:19:05 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Sat, 07 Aug 2021 00:19:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Sat, 07 Aug 2021 00:19:06 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Sat, 07 Aug 2021 00:19:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 07 Aug 2021 00:19:36 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 07:28:17 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 07:28:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 07:28:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caeb0c74bcecd47668d97740cb028f398bfcfb13e02c6eb17649357dcd77ad8f`  
		Last Modified: Fri, 23 Jul 2021 01:38:10 GMT  
		Size: 2.2 MB (2152136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624620d306c546b17507810ac42a8f849e57061e361868e99b4cfed062113280`  
		Last Modified: Fri, 23 Jul 2021 01:38:15 GMT  
		Size: 9.3 MB (9295395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab8f6df99007a4c01b1925c87e47b2d1c75beadca139d41432503804eabfdaa`  
		Last Modified: Fri, 23 Jul 2021 01:38:09 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7665bbe1fe709cf50818949bbadf4ea9e8ef4d522b85dc1b34daf55ee27f9ba`  
		Last Modified: Sat, 07 Aug 2021 01:04:31 GMT  
		Size: 2.6 MB (2638228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d60ae52026075b1d7576120900d947fd4ea4a968855689bfabfdd01176006e`  
		Last Modified: Sat, 07 Aug 2021 07:39:04 GMT  
		Size: 3.1 MB (3051082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-stretch` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:bde032ed893a5f8ae265d8960dd362063d75e845df60fcac5eae2f587d1016de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38015945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa74f403991159ada6df4381d76138feec336ac33b85fd1b88f9a3c06290028f`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:40 GMT
ADD file:b39a01b3af7a531df3592571b7f6eaa7efd20919858f7f0cd2ddf1c1eceb078d in / 
# Thu, 22 Jul 2021 00:41:40 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 11:34:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 11:34:24 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 11:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 11:34:31 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 22 Jul 2021 11:34:31 GMT
ENV PYTHON_VERSION=3.7.11
# Thu, 22 Jul 2021 11:41:16 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 11:41:17 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 23:50:41 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 23:50:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 23:50:41 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 23:50:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 23:50:55 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 04:09:35 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 04:09:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 04:09:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9e7a560784c85cb9624bff5b6e479fbb95d5e265873987014f8aec75d509a530`  
		Last Modified: Thu, 22 Jul 2021 00:48:50 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f106dd115c60608b983fe2f2d8a76d91f00d8ceecee4b904961b7b86d75b4ad0`  
		Last Modified: Thu, 22 Jul 2021 12:11:31 GMT  
		Size: 2.2 MB (2215145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aee2dccafc08f75ac6d3b7077d617206eded33ce5a4aa260dfe9fbc1a2d70b`  
		Last Modified: Thu, 22 Jul 2021 12:11:32 GMT  
		Size: 9.7 MB (9722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d34799f5133dd79fa5c8813b4ad83ab1ec3c61cec10e596f02e7addd2678e1`  
		Last Modified: Thu, 22 Jul 2021 12:11:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5401036c33ac3b95f5c168bb47d8319314ffe66199983087f20d73de199c77e`  
		Last Modified: Sat, 07 Aug 2021 00:16:26 GMT  
		Size: 2.6 MB (2637672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164b5d27e9f409dc6c0f95ddc74a02ae39aaf12bfcb63e02fcc275ee41cb50f9`  
		Last Modified: Sat, 07 Aug 2021 04:16:02 GMT  
		Size: 3.1 MB (3050992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-stretch` - linux; 386

```console
$ docker pull hylang@sha256:b6c3b193b5308bd47b0867fa2f61741597c14d9ad1ef35c7274d8fa8681daf85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41447108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b00a6037b8cf317d3be179ccb321594dcb00151105243a6c1e7136f6194cac`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:45 GMT
ADD file:031e0099f6d9f77a3c2cc04e510e38072e1deb4394692b02cee9689e30a4286a in / 
# Thu, 22 Jul 2021 00:41:45 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 14:30:58 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:31:07 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 22 Jul 2021 14:31:07 GMT
ENV PYTHON_VERSION=3.7.11
# Thu, 22 Jul 2021 14:39:05 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 14:39:06 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 22:59:32 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 22:59:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 22:59:32 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 22:59:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 22:59:48 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 05:10:17 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 05:10:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 05:10:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:92ef0ad3e2e4c31244fba7bdf4771ee5d90b4a815d9ac530ac555e1b83dc93d8`  
		Last Modified: Thu, 22 Jul 2021 00:49:52 GMT  
		Size: 23.2 MB (23156226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf198c4e78cd8f26010727b1c4df0a65d4b050c38c9ad334c4316c975f521214`  
		Last Modified: Thu, 22 Jul 2021 15:21:06 GMT  
		Size: 2.5 MB (2509075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b9ea5402436fe6155c21566948af9ba50d43e4511b73566ce8f100c1ffd10`  
		Last Modified: Thu, 22 Jul 2021 15:21:07 GMT  
		Size: 10.1 MB (10092354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ea922423804c6e53e7d05f42ee39a3894c71d56c5d3b30184e31f3a9068fe2`  
		Last Modified: Thu, 22 Jul 2021 15:21:05 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b705983e36ed6e9aef6e32a059996e3c2f6516aba0d79158a38411e5d78ee15`  
		Last Modified: Sat, 07 Aug 2021 02:23:36 GMT  
		Size: 2.6 MB (2638349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303ef42710a99486cc84bb656e380261341ed5710f1408360bcc2f205b699807`  
		Last Modified: Sat, 07 Aug 2021 05:16:49 GMT  
		Size: 3.1 MB (3050863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
