## `hylang:0-python2.7`

```console
$ docker pull hylang@sha256:2167f648e1c115fa98bf390652e9b9a83f7a127ca127f858fb61620c97e65fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `hylang:0-python2.7` - linux; amd64

```console
$ docker pull hylang@sha256:3910d15b5329219ef8ca57411033b2acba9f40ed3a0318f4597a1fbaa50489bd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54126167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb1c78a0550f337d3462e7a53e007b7a9f3746e5b5475695fe5add8a5faf6e3`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:32:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 05:32:37 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 07:50:43 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 28 Dec 2019 07:50:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:50:54 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 28 Dec 2019 07:50:54 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 28 Dec 2019 07:59:44 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 28 Dec 2019 07:59:44 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 07:59:44 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 07:59:44 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 08:00:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 08:00:04 GMT
CMD ["python2"]
# Sun, 29 Dec 2019 07:46:50 GMT
ENV HY_VERSION=0.17.0
# Sun, 29 Dec 2019 07:46:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 29 Dec 2019 07:46:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfa5cc2566c576cdbcf72895fdb6eb3fae273dc3002c46d2e27d6bf464c9f0f`  
		Last Modified: Sat, 28 Dec 2019 08:21:39 GMT  
		Size: 2.7 MB (2749021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642c5fbdca36faa68ab1edfb9031510a5a31e23c03953c75a0cd18518adc9b0c`  
		Last Modified: Sat, 28 Dec 2019 08:21:44 GMT  
		Size: 19.7 MB (19662520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c0590866d6bbd9785b7514e178b97bde6dd6f4816f7249459892ac1c4a92b4`  
		Last Modified: Sat, 28 Dec 2019 08:21:39 GMT  
		Size: 2.2 MB (2154812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd94a03459518deeede79f5f876f0027ac40c5d22e0c378418ced85717b6ee5`  
		Last Modified: Sun, 29 Dec 2019 07:48:56 GMT  
		Size: 2.5 MB (2467540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7` - linux; arm variant v5

```console
$ docker pull hylang@sha256:73d8caf706600aae87485e499c06dacf63f5dc3d443760e9027a1373f3c1b37c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50398376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecaa5d07614a308b894b6d0703d8010ba3df223759f2d134696164fc67c06a0`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:37:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:37:03 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 11:06:13 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 28 Dec 2019 11:06:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:06:29 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 28 Dec 2019 11:06:29 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 28 Dec 2019 11:16:57 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 28 Dec 2019 11:16:59 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 11:17:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 11:17:01 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 11:17:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 11:17:32 GMT
CMD ["python2"]
# Sat, 28 Dec 2019 20:31:14 GMT
ENV HY_VERSION=0.17.0
# Sat, 28 Dec 2019 20:31:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 28 Dec 2019 20:31:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6191b5dfe393695b7c5e32c3e0d5bf655863d7844fb24bc63de72b7ccb811192`  
		Last Modified: Sat, 28 Dec 2019 11:44:51 GMT  
		Size: 2.4 MB (2448143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b9a214c91c847d27232510a9ed80c94722e7f1a439943c41254e78a04dc8ad`  
		Last Modified: Sat, 28 Dec 2019 11:44:56 GMT  
		Size: 18.5 MB (18497609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c87c0efd2b33476a1488167ca786093887d3a0b98b87f28172692ade3afff15`  
		Last Modified: Sat, 28 Dec 2019 11:44:51 GMT  
		Size: 2.2 MB (2154610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b653265544b2abc6522a8ebbc30983c574d9fd961ca32a6262f5bfa20588c436`  
		Last Modified: Sat, 28 Dec 2019 20:33:11 GMT  
		Size: 2.5 MB (2468396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7` - linux; arm variant v7

```console
$ docker pull hylang@sha256:4bedaf73f2272ef80d45715c7da568ceeea00f9357c032f97c96c8102b095ba8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf5e08030e219d03ecaf5baf639ebc31397a00f04f5a673d559767f1bce6bda`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 17:43:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 17:43:24 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 20:22:42 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 28 Dec 2019 20:23:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:23:07 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 28 Dec 2019 20:23:10 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 28 Dec 2019 20:35:54 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 28 Dec 2019 20:35:56 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 20:35:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 20:35:58 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 20:36:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 20:36:24 GMT
CMD ["python2"]
# Sun, 29 Dec 2019 07:02:39 GMT
ENV HY_VERSION=0.17.0
# Sun, 29 Dec 2019 07:03:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 29 Dec 2019 07:03:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca529d843b190cbc0724f89ffca340a02597013cef444a4c314715a4e587f296`  
		Last Modified: Sat, 28 Dec 2019 21:02:25 GMT  
		Size: 2.3 MB (2345939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7241d6e34cc5459befc74377b8fdf09e8789c45e62304749d8417d9aeb2d5564`  
		Last Modified: Sat, 28 Dec 2019 21:02:31 GMT  
		Size: 18.1 MB (18102357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7082e06ab2371beb8cecdae133a61482487b138958b40d0830a4ff03c60b76`  
		Last Modified: Sat, 28 Dec 2019 21:02:26 GMT  
		Size: 2.2 MB (2155030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39366da04a05412d66b06966f780c6bf247d541a660b150cd13f1f0c3fc30f2f`  
		Last Modified: Sun, 29 Dec 2019 07:06:37 GMT  
		Size: 2.5 MB (2468672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c3a0304f1737ce0c166ec47270ca4633379b2dfe4435b44aef3dbad4f07b64e2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52425178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68417800a474d9602f13464a722c91c04ec2eacf80406d56f3541ec8257f57df`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 19:11:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 19:11:54 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 21:38:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 28 Dec 2019 21:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 21:39:01 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 28 Dec 2019 21:39:02 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 28 Dec 2019 21:49:08 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 28 Dec 2019 21:49:10 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 21:49:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 21:49:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 21:49:36 GMT
CMD ["python2"]
# Sun, 29 Dec 2019 07:12:32 GMT
ENV HY_VERSION=0.17.0
# Sun, 29 Dec 2019 07:12:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 29 Dec 2019 07:12:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d80d03fcf145baaff1a1cab742c80815d6dcf5b9c44b1ed34bd4d3fc7a8236c`  
		Last Modified: Sat, 28 Dec 2019 22:15:22 GMT  
		Size: 2.6 MB (2622317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03afbca7e1c0d4609b0cbaf0dd64e34d00be03a10705a381bb2d7fd54231eb17`  
		Last Modified: Sat, 28 Dec 2019 22:15:33 GMT  
		Size: 19.3 MB (19328915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2e7cd1be180bf7b0f101e4335c43a40453069aceb4fa10e62792318cda3242`  
		Last Modified: Sat, 28 Dec 2019 22:15:22 GMT  
		Size: 2.2 MB (2154925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc55fa01ecdb574d37ed7d655ac1b01b522bf3547fddc02f9cb43128b878ecf7`  
		Last Modified: Sun, 29 Dec 2019 07:16:49 GMT  
		Size: 2.5 MB (2468319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7` - linux; 386

```console
$ docker pull hylang@sha256:ff3a6be0de422a650a1f059821b3124e8e5673706a4c7325836efd1d7d11fbe4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53740887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055211d093159da069a901b01e05d2ee79130143a0779d7851ef1f0a8f27c156`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:17:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 20:17:48 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 23:14:04 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 28 Dec 2019 23:14:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 23:14:12 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 28 Dec 2019 23:14:12 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 28 Dec 2019 23:22:39 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 28 Dec 2019 23:22:40 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 23:22:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 23:22:40 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 23:22:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 23:22:54 GMT
CMD ["python2"]
# Sun, 29 Dec 2019 00:14:45 GMT
ENV HY_VERSION=0.17.0
# Sun, 29 Dec 2019 00:14:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 29 Dec 2019 00:14:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b92e3aaabe29052a5d7f6dddbbb7fd0305c00db484fe16868181b4b7830e986`  
		Last Modified: Sat, 28 Dec 2019 23:41:51 GMT  
		Size: 2.8 MB (2762483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d22486741d1ddd3cccf83a53bd85f0c021a7dc1d594d551add9428b774b5075`  
		Last Modified: Sat, 28 Dec 2019 23:41:55 GMT  
		Size: 18.6 MB (18608964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2f659b5499920a98229fd8d34a7d5650c0291476eb69e1b2f88e5014bc5712`  
		Last Modified: Sat, 28 Dec 2019 23:41:51 GMT  
		Size: 2.2 MB (2154409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a44c32e87fc34c45acae44758ea5534a74f7c4b55800fad3a2d9e62b083544`  
		Last Modified: Sun, 29 Dec 2019 00:17:49 GMT  
		Size: 2.5 MB (2468011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7` - linux; ppc64le

```console
$ docker pull hylang@sha256:f201b2d21f097340db4f57c3696b4399d9412e632e85f8837ac212043d87423c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58316028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28194edad3b60ea2da323e61a4951a2102e07eedecf56bff3e38f9978e4ac6`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:50:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 14:50:21 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 17:26:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 28 Dec 2019 17:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 17:27:07 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 28 Dec 2019 17:27:10 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 28 Dec 2019 17:38:31 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 28 Dec 2019 17:38:34 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 17:38:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 17:38:37 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 17:39:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 17:39:03 GMT
CMD ["python2"]
# Sun, 29 Dec 2019 01:45:02 GMT
ENV HY_VERSION=0.17.0
# Sun, 29 Dec 2019 01:45:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 29 Dec 2019 01:45:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef741e3ac2a7cc74f9d2cf5201bfb50b554610dcf0f3fff6a1ce161b837a98`  
		Last Modified: Sat, 28 Dec 2019 18:05:10 GMT  
		Size: 2.9 MB (2871733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0de8e8a8a4363542a30c6b3935365fc508525a592f3a08c3d934c92f61026d7`  
		Last Modified: Sat, 28 Dec 2019 18:05:12 GMT  
		Size: 20.3 MB (20302562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4183e4f70c6aceee106b32ac42431596244abfd52265eb67e5304cfaff8d9f08`  
		Last Modified: Sat, 28 Dec 2019 18:05:06 GMT  
		Size: 2.2 MB (2155748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e93d308221573ddf6bde080ac3caf38461f88e0a04a59cc1bd069e06023b47`  
		Last Modified: Sun, 29 Dec 2019 01:50:29 GMT  
		Size: 2.5 MB (2468456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7` - linux; s390x

```console
$ docker pull hylang@sha256:eca02106725542ca6aecad77f3555c74b999c518860d967b5daae4501a6a619c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51078046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d5f6017ef83df1c60f5ace5db719fa268b20d84c1ab52bebad690986a8ce96`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 16 Oct 2019 23:42:48 GMT
ADD file:4bf0501a845ff525e4edaa88b6641f72b2f2df61d0ebf4ef03222cf79feee915 in / 
# Wed, 16 Oct 2019 23:42:48 GMT
CMD ["bash"]
# Thu, 17 Oct 2019 08:39:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2019 08:39:37 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2019 10:23:46 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 17 Oct 2019 10:23:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2019 10:23:58 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Thu, 24 Oct 2019 00:50:31 GMT
ENV PYTHON_VERSION=2.7.17
# Fri, 15 Nov 2019 03:48:33 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Fri, 15 Nov 2019 03:48:33 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 15 Nov 2019 03:48:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 15 Nov 2019 03:48:34 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 15 Nov 2019 03:48:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 15 Nov 2019 03:48:50 GMT
CMD ["python2"]
# Fri, 15 Nov 2019 04:20:52 GMT
ENV HY_VERSION=0.17.0
# Fri, 15 Nov 2019 04:20:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 15 Nov 2019 04:20:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ad1fb1a183ba14bd1dc12e9413867f1b9b9687c6ba30209f34777d4cee3bcba8`  
		Last Modified: Wed, 16 Oct 2019 23:48:34 GMT  
		Size: 25.7 MB (25718301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac417b901c23ad41a28964017401e79dc68e938807d2d2808b560b02a2e22d3d`  
		Last Modified: Thu, 17 Oct 2019 10:39:56 GMT  
		Size: 2.4 MB (2442023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03904ebf4332813688dcfced1ceb548454cd90016a99bea98a97113acde891aa`  
		Last Modified: Fri, 15 Nov 2019 04:02:11 GMT  
		Size: 18.3 MB (18298836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fa13ca45ee4d52d3c80dab65492f3369bc76354cef568055ea9164e25f8684`  
		Last Modified: Fri, 15 Nov 2019 04:02:06 GMT  
		Size: 2.2 MB (2153293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2b50adc96bed52bccbeff13c73b3a9103e5a662405e66bab734d3702cee4ae`  
		Last Modified: Fri, 15 Nov 2019 04:24:31 GMT  
		Size: 2.5 MB (2465593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7` - windows version 10.0.17763.973; amd64

```console
$ docker pull hylang@sha256:909a817a926392ca4a58e492a2c95417e68536e2380caa1123544b94879ff25f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2266082535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d05c8db7d2cc0477170e6d2fd359d8ec331f605f089c491a98fbd44ad3921f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:31:45 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 15 Jan 2020 18:31:46 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 15 Jan 2020 18:33:53 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Wed, 15 Jan 2020 18:33:54 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Wed, 15 Jan 2020 18:33:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Wed, 15 Jan 2020 18:33:57 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Wed, 15 Jan 2020 18:35:09 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 15 Jan 2020 18:35:40 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 15 Jan 2020 18:35:41 GMT
CMD ["python"]
# Wed, 15 Jan 2020 22:32:03 GMT
ENV HY_VERSION=0.17.0
# Wed, 15 Jan 2020 23:03:11 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 15 Jan 2020 23:03:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991e8bf1fe43fb6d1b926596157fec820f98e6bf95f7d87c5037c6a9d454ee94`  
		Last Modified: Wed, 15 Jan 2020 18:44:46 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3061269fafccc2b8dbc758f49ebd8556e388f724ca6c14b7274e2c96eeb5b9`  
		Last Modified: Wed, 15 Jan 2020 18:44:44 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8b29109525c4a2b28a2790a4cf8dcf3e323f9aabee0ae266fe15eef2b42f3`  
		Last Modified: Wed, 15 Jan 2020 18:45:09 GMT  
		Size: 38.9 MB (38905595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b7bfb2d410b4d47d61cf996c62c9637e0f4b2e1d90b0a3ca5855c112fd6d00`  
		Last Modified: Wed, 15 Jan 2020 18:44:44 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192de2a494e89995023b5156ec82ed366e015319750d3b5e211b8062d5c42538`  
		Last Modified: Wed, 15 Jan 2020 18:44:42 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caf5da95386bcefa79b3cc670968232ced9d71ca6136efd6245a17915e548b9`  
		Last Modified: Wed, 15 Jan 2020 18:44:41 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb3aae3dd398502395d0956f801737486c9cfc1da3eede725d3418f1b3d9385`  
		Last Modified: Wed, 15 Jan 2020 18:44:56 GMT  
		Size: 4.9 MB (4948373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2742b7e16a95d9f7ed91fd2c9fffc8235b42fe2e5944c13cc4de210cc4c6c9e6`  
		Last Modified: Wed, 15 Jan 2020 18:44:43 GMT  
		Size: 3.8 MB (3754849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69f57f4de5c03a4f26868d02504e3fab37650dde5e23ed7b12a06422183b726`  
		Last Modified: Wed, 15 Jan 2020 18:44:41 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fe6eef30950c2b31d313eaaf69b52befcd98b27e7243128c25748974b5839`  
		Last Modified: Wed, 15 Jan 2020 23:08:42 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bb429315ed051b97b3740abc9c23eb43fc50307cf0833a510114e5ea3aabed`  
		Last Modified: Wed, 15 Jan 2020 23:08:45 GMT  
		Size: 1.1 MB (1051776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ce95ec8c57cd96247b3607173e386bd9c754418d893a8f9bee674b0c19f565`  
		Last Modified: Wed, 15 Jan 2020 23:08:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python2.7` - windows version 10.0.14393.3443; amd64

```console
$ docker pull hylang@sha256:5849c841f6aed3a34412c7852679a1858649d890025c935bfdf5789fc4fd116f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5789158380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372af682e404f89eaac50ea5bb2f3838a4c1b6fab2c97ece47f4a63c36b1dbb7`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:25:25 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 15 Jan 2020 18:25:26 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 15 Jan 2020 18:28:02 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Wed, 15 Jan 2020 18:28:04 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Wed, 15 Jan 2020 18:28:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Wed, 15 Jan 2020 18:28:07 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Wed, 15 Jan 2020 18:30:08 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 15 Jan 2020 18:31:18 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 15 Jan 2020 18:31:20 GMT
CMD ["python"]
# Wed, 15 Jan 2020 23:03:30 GMT
ENV HY_VERSION=0.17.0
# Wed, 15 Jan 2020 23:04:57 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 15 Jan 2020 23:04:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4287864358145220d2cb16b67268467546ff8efdf51507ec81129f122708a47b`  
		Last Modified: Wed, 15 Jan 2020 18:43:19 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c883f7ca435fbdfe46efa0a8699443e235080d73c839cadb563b2f6da76d4002`  
		Last Modified: Wed, 15 Jan 2020 18:43:16 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53b74241deb5632f2a489ac1f65935c6f2981dcb2346a46c2010417f601b2ce`  
		Last Modified: Wed, 15 Jan 2020 18:44:09 GMT  
		Size: 39.7 MB (39688129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bbb69d71bd7d8c4bce020511ef1a1c68920198114d500bbeb97e89557ad5a2`  
		Last Modified: Wed, 15 Jan 2020 18:43:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b419ebcd9cd371e2821c3b5229642cdb1c784981b540b5e0438e8fe8eb1193`  
		Last Modified: Wed, 15 Jan 2020 18:43:13 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f0b6b0538bb42acc53bb9ad3a6b6583c7a30581e7d009e081e029203861d88`  
		Last Modified: Wed, 15 Jan 2020 18:43:13 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86db542d352e04f16f8e739f92174825e15e4c160de933610d8c71e52b77ba1`  
		Last Modified: Wed, 15 Jan 2020 18:43:32 GMT  
		Size: 10.0 MB (10001215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec875652d4334e97e839f7d39bbf1229598439f7f369205e3aad8a4f80a1589`  
		Last Modified: Wed, 15 Jan 2020 18:43:23 GMT  
		Size: 8.8 MB (8781934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ad02b3229b501b227ac86d09928703af078d9f25308c1bda083272b7d73180`  
		Last Modified: Wed, 15 Jan 2020 18:43:13 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164e87e9af3f1a6bfd9c71a204056ef0057eabf6c232e59bb234654e2efb4d8c`  
		Last Modified: Wed, 15 Jan 2020 23:09:29 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c7b1abe1b3792fe55d7d0d757a82b743dcc6202aa17062235dbecb3007559b`  
		Last Modified: Wed, 15 Jan 2020 23:09:32 GMT  
		Size: 6.1 MB (6077110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcb00bc666e76b0b28b93cd27a89899b480135ff78495d72cb9d6230130c9e1`  
		Last Modified: Wed, 15 Jan 2020 23:09:29 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
