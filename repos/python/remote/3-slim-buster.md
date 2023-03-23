## `python:3-slim-buster`

```console
$ docker pull python@sha256:6cc3e51b24c91809e9f7abf8391c8fc56c1bcfef9bf64745ea05c23852f3d67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `python:3-slim-buster` - linux; amd64

```console
$ docker pull python@sha256:5b287042a6150052420e6a7fb7c1606b6403740880897ae9610faf434da28693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45282610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa00e43d978bd2a11f1a27a3217ee5ae19b3821c540703c8ea5b027806096c8`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:50 GMT
ADD file:52316aa7d631242cd16337be337e57187ef07d3965e6284321fbdcd5b4f92b64 in / 
# Thu, 23 Mar 2023 01:30:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 01:30:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 01:30:51 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 01:30:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Mar 2023 01:30:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 23 Mar 2023 01:30:51 GMT
ENV PYTHON_VERSION=3.11.2
# Thu, 23 Mar 2023 01:30:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 23 Mar 2023 01:30:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 23 Mar 2023 01:30:51 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 23 Mar 2023 01:30:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 23 Mar 2023 01:30:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Thu, 23 Mar 2023 01:30:51 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Thu, 23 Mar 2023 01:30:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 23 Mar 2023 01:30:51 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3689b8de819b48387712c6d4d62d26a52a04c9e88afc68fb9d1dbe48bfa9e21d`  
		Last Modified: Thu, 23 Mar 2023 01:35:01 GMT  
		Size: 27.1 MB (27139869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8cd5f36469921b82be5c046d0fe82365de8fcee96a4caa8259939d06d99bef`  
		Last Modified: Thu, 23 Mar 2023 05:41:22 GMT  
		Size: 2.8 MB (2782122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80384e04044fa9b6493f2c9012fd1aa7035ab741147248930b5a2b72136198b1`  
		Last Modified: Thu, 23 Mar 2023 05:42:48 GMT  
		Size: 12.0 MB (11990866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe06c6a3fe34fe65c406b3dfcd8f504972ef83a65287a88d2be3bbe81eeaf56`  
		Last Modified: Thu, 23 Mar 2023 05:42:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0712d0bdb159c54d5bdce952fbb72c5a5d2a4399654d7f55b004d9fc01e189e`  
		Last Modified: Thu, 23 Mar 2023 05:42:46 GMT  
		Size: 3.4 MB (3369508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-slim-buster` - linux; arm variant v7

```console
$ docker pull python@sha256:87002c6854b75538719b7dc537445040b3101ebb0228a5be8a7caab19942a33f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39739811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0b54f95548a6527380cffe142351a3e625972c443c2392bf91cca93319cfd8`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 01 Mar 2023 01:58:13 GMT
ADD file:421c3f57223e760f56f68a9d1c272feaf8239dd72494fc3ef8e9896758e503c8 in / 
# Wed, 01 Mar 2023 01:58:13 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:00:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:00:48 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 13:00:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 01 Mar 2023 14:03:03 GMT
ENV PYTHON_VERSION=3.11.2
# Fri, 17 Mar 2023 04:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Fri, 17 Mar 2023 04:51:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Fri, 17 Mar 2023 04:51:21 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Fri, 17 Mar 2023 04:51:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 17 Mar 2023 04:51:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Fri, 17 Mar 2023 04:51:21 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Fri, 17 Mar 2023 04:51:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 17 Mar 2023 04:51:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:7138f15de53476a9a56af46eac63ea2f39c78b20aa9ad61ce3018e0eddb748f8`  
		Last Modified: Wed, 01 Mar 2023 02:03:50 GMT  
		Size: 22.7 MB (22748560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3263bcfdfa8cf12a4cdb3701ea31c7cc9e9b61291cbf7f31c3412cb6a1ea737e`  
		Last Modified: Wed, 01 Mar 2023 15:47:12 GMT  
		Size: 2.4 MB (2369991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba765922919cd0d6f9cddeaf4885a3e036a0173cf3492ef0dcf0add5dab2352`  
		Last Modified: Fri, 17 Mar 2023 05:39:28 GMT  
		Size: 11.3 MB (11252231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9bf163d42301e7e2a9fe126e4b93ed605b3433f2a5012980216d74edae2680`  
		Last Modified: Fri, 17 Mar 2023 05:39:26 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb793fa84d798ffe61a3fba23049317f3590505ef8198ab490e83e7f88f30d0`  
		Last Modified: Fri, 17 Mar 2023 05:39:27 GMT  
		Size: 3.4 MB (3368796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull python@sha256:8ad1ea21d7a1684635267de303d4a2d7e2b04353b7748b28adc2fbdcaafec880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44023133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9fb8cfd51a0c66d852b41c67521df41cd08d96be478812a98857a2c885e0c8`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:23 GMT
ADD file:44e400cc6a1bc5df5a57bda478c9accf9b58950fa2fd069cc7620128fe786770 in / 
# Thu, 23 Mar 2023 00:45:23 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:45:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 00:45:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 00:45:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Mar 2023 00:45:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 23 Mar 2023 00:45:23 GMT
ENV PYTHON_VERSION=3.11.2
# Thu, 23 Mar 2023 00:45:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 23 Mar 2023 00:45:23 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 23 Mar 2023 00:45:23 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 23 Mar 2023 00:45:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 23 Mar 2023 00:45:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Thu, 23 Mar 2023 00:45:23 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Thu, 23 Mar 2023 00:45:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 23 Mar 2023 00:45:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:cfe0f778e53ce031ef449bc02975a07f2568716dea807ed2f390d352c0001972`  
		Last Modified: Thu, 23 Mar 2023 00:48:45 GMT  
		Size: 25.9 MB (25922660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e11a7826c6ce9b3366e1d2c4dfbdec39133e62fe15bca830f2947fd1064b6c`  
		Last Modified: Thu, 23 Mar 2023 05:31:52 GMT  
		Size: 2.6 MB (2648728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a79e484c85524a9518ed521a6da01406628e5c55cec47c59102370156207769`  
		Last Modified: Thu, 23 Mar 2023 05:33:13 GMT  
		Size: 12.1 MB (12082369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512300f3f60f5881c40788691060131b98ea2ddd1218c3d40ecaf8257728cc2`  
		Last Modified: Thu, 23 Mar 2023 05:33:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d0b90d56060877b3e214d3d7d820594f685a18d1d659e14d0b5d03e8fdce1d`  
		Last Modified: Thu, 23 Mar 2023 05:33:12 GMT  
		Size: 3.4 MB (3369132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-slim-buster` - linux; 386

```console
$ docker pull python@sha256:80f113f57696b903a407f152fe660752fa14cbd93055cd6a81ecd1d183fe0347
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46032063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084036f3b833474a9ebd0b653c18253405d7dbede797ff15b88af444eb435568`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:35 GMT
ADD file:d90e1c78fceb91ea00c9b00cdf477b7254e3d4d37b561698e90b75c62d84320c in / 
# Wed, 01 Mar 2023 01:39:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:03:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 04:03:32 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 04:03:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:20:02 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 01 Mar 2023 05:20:02 GMT
ENV PYTHON_VERSION=3.11.2
# Fri, 17 Mar 2023 05:09:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Fri, 17 Mar 2023 05:09:37 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Fri, 17 Mar 2023 05:09:37 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Fri, 17 Mar 2023 05:09:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 17 Mar 2023 05:09:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Fri, 17 Mar 2023 05:09:38 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Fri, 17 Mar 2023 05:09:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 17 Mar 2023 05:09:51 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5dd0dee7d259a761fe8021e1fd6a2a9a8590880098b27d4f97cfbda4e50bc631`  
		Last Modified: Wed, 01 Mar 2023 01:45:36 GMT  
		Size: 27.8 MB (27798766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a978f2d70c03ae2b43d6ea17659a095336d76126c4de2176f6a4db9f0c68ef7`  
		Last Modified: Wed, 01 Mar 2023 07:44:22 GMT  
		Size: 2.8 MB (2790284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a6d17afc11922ff8e3d8eb766474c93eff8bc357b2c35f6b0dcbecced2237e`  
		Last Modified: Fri, 17 Mar 2023 06:18:00 GMT  
		Size: 12.1 MB (12073599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151e1f4ac7d559418704df42785d95fc6a64ba5b0211400b93bd37269a2f2483`  
		Last Modified: Fri, 17 Mar 2023 06:17:58 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d1361c84a7469ac1a8c74a270502fc61d965fe23e9ebda19ec81d0b066bab9`  
		Last Modified: Fri, 17 Mar 2023 06:17:59 GMT  
		Size: 3.4 MB (3369180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
