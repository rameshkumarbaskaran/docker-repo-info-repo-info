## `hylang:0-python3.9-buster`

```console
$ docker pull hylang@sha256:4cb408c0e9307b7982dd2a4fe5866a647daa28577788708444ea7c6268843c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-python3.9-buster` - linux; amd64

```console
$ docker pull hylang@sha256:2dd64503a9d66bd8f2363749170dab2bc08f31751fef4328428fd4cf067e8c5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48302784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f1c2d22d9387a39a8975619cc304fdeeeccb0108a1851c90da7c5114024c80`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:10:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 14:10:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 14:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 15:29:58 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 13 Oct 2022 23:57:06 GMT
ENV PYTHON_VERSION=3.9.15
# Fri, 14 Oct 2022 00:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Fri, 14 Oct 2022 00:04:13 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Fri, 14 Oct 2022 00:04:13 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Fri, 14 Oct 2022 00:04:13 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 25 Oct 2022 01:00:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6d265be7a6b5bc4e9c5c07646aee0bf0394be03d/public/get-pip.py
# Tue, 25 Oct 2022 01:00:39 GMT
ENV PYTHON_GET_PIP_SHA256=36c6f6214694ef64cc70f4127ac0ccec668408a93825359d998fb31d24968d67
# Tue, 25 Oct 2022 01:00:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 25 Oct 2022 01:00:51 GMT
CMD ["python3"]
# Tue, 25 Oct 2022 01:56:49 GMT
ENV HY_VERSION=0.24.0
# Tue, 25 Oct 2022 01:56:49 GMT
ENV HYRULE_VERSION=0.2
# Tue, 25 Oct 2022 01:57:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 25 Oct 2022 01:57:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87859229fd406f0033ac497a9bb939b7ebb8ab800b3ce31a240a9c8943761d2`  
		Last Modified: Wed, 05 Oct 2022 16:34:27 GMT  
		Size: 2.8 MB (2779341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbc880019f4040b4b02df966f5fb412fd2c65f9897a16ec7fb5529f4434c1ef`  
		Last Modified: Fri, 14 Oct 2022 00:54:12 GMT  
		Size: 11.6 MB (11567880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb7a8166c756e014bf74924443cc4606b46293f1958948560ab1b9cc5ff913d`  
		Last Modified: Fri, 14 Oct 2022 00:54:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae12f69a8fe33427209e8b00c816b8a75286731fd464d002e7186805d16b991`  
		Last Modified: Tue, 25 Oct 2022 01:08:52 GMT  
		Size: 3.2 MB (3171932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d43dc9f5456f4027da8b18441591b2cefc73b11dcabd59ed046c62ead096b17`  
		Last Modified: Tue, 25 Oct 2022 02:03:32 GMT  
		Size: 3.6 MB (3645354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.9-buster` - linux; arm variant v7

```console
$ docker pull hylang@sha256:3bd81e81505da80d625eb14c8c56d6adc47ceebb3d0ad1a7c8153e062c1d8532
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42700676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade44a295b477f18c5c5f244f577bbf3fe1b45a33551ea64cb87b20bb1ae0332`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Oct 2022 23:59:18 GMT
ADD file:3cde948f83f960927e2aa8be792b46726d7c3cb7a5250167816f138165e1ed3f in / 
# Tue, 04 Oct 2022 23:59:18 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 00:26:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 00:26:14 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 00:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 02:28:42 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 14 Oct 2022 09:09:28 GMT
ENV PYTHON_VERSION=3.9.15
# Fri, 14 Oct 2022 09:24:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Fri, 14 Oct 2022 09:24:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Fri, 14 Oct 2022 09:24:03 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Fri, 14 Oct 2022 09:24:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Fri, 14 Oct 2022 09:24:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5eaac1050023df1f5c98b173b248c260023f2278/public/get-pip.py
# Fri, 14 Oct 2022 09:24:04 GMT
ENV PYTHON_GET_PIP_SHA256=5aefe6ade911d997af080b315ebcb7f882212d070465df544e1175ac2be519b4
# Fri, 14 Oct 2022 09:24:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 14 Oct 2022 09:24:20 GMT
CMD ["python3"]
# Fri, 14 Oct 2022 22:18:32 GMT
ENV HY_VERSION=0.24.0
# Fri, 14 Oct 2022 22:18:32 GMT
ENV HYRULE_VERSION=0.2
# Fri, 14 Oct 2022 22:18:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 14 Oct 2022 22:18:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4d0206a59e12f0afd97e080863f8788c54ecd251e26b9e6dd5d6db4d56cef8cd`  
		Last Modified: Wed, 05 Oct 2022 00:06:03 GMT  
		Size: 22.7 MB (22746557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8167eca2bd056152abc78bd2fbae532b7b6fe92cdfbd2b16cf2e2f3d3de4b8c`  
		Last Modified: Thu, 06 Oct 2022 03:58:02 GMT  
		Size: 2.4 MB (2366866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016e1e9db1e7ec0bb08853386d7793747cf51ecb4f22c586e6caf8eaac224da3`  
		Last Modified: Fri, 14 Oct 2022 11:28:43 GMT  
		Size: 10.8 MB (10770340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba23cda677e0748563140dc6c8b2bea6e07b5ec5dd209d560a6b79ad5209b75`  
		Last Modified: Fri, 14 Oct 2022 11:28:39 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1761e90908c973138ca853ba14de09b6f6893e848361202087b03c8f65189479`  
		Last Modified: Fri, 14 Oct 2022 11:28:42 GMT  
		Size: 3.2 MB (3171300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c5841313b8e61efed83bd75d6f335f95fb19ac0b4a48cc60e37a65980878d3`  
		Last Modified: Fri, 14 Oct 2022 22:30:02 GMT  
		Size: 3.6 MB (3645379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.9-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:66e51011859d237d562cf5519dbc05a43429f6950e2e9440ab870c420259d84d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46990637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac77d54bca5db1dae9004bad1cc2582f272fb5b9ee3959e4262fc99645825a60`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:11:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 06:11:51 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:11:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:48:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 25 Oct 2022 06:48:55 GMT
ENV PYTHON_VERSION=3.9.15
# Tue, 25 Oct 2022 06:53:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 25 Oct 2022 06:53:45 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 25 Oct 2022 06:53:46 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 25 Oct 2022 06:53:46 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 25 Oct 2022 06:53:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6d265be7a6b5bc4e9c5c07646aee0bf0394be03d/public/get-pip.py
# Tue, 25 Oct 2022 06:53:46 GMT
ENV PYTHON_GET_PIP_SHA256=36c6f6214694ef64cc70f4127ac0ccec668408a93825359d998fb31d24968d67
# Tue, 25 Oct 2022 06:53:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 25 Oct 2022 06:53:56 GMT
CMD ["python3"]
# Tue, 25 Oct 2022 07:28:57 GMT
ENV HY_VERSION=0.24.0
# Tue, 25 Oct 2022 07:28:57 GMT
ENV HYRULE_VERSION=0.2
# Tue, 25 Oct 2022 07:29:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 25 Oct 2022 07:29:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9353727c2c340da2074ff7954456841315eaa1c1db324a467cc2cdb3d9af7c35`  
		Last Modified: Tue, 25 Oct 2022 07:18:39 GMT  
		Size: 2.6 MB (2646671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048bbe3f205c74d99edf1ddcbf294e825da8970150496abad54fa08a495b104a`  
		Last Modified: Tue, 25 Oct 2022 07:19:48 GMT  
		Size: 11.6 MB (11584381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5242b2e92738bb0fb903856b541af3245499e1434cab0ffc93d545839e42ca93`  
		Last Modified: Tue, 25 Oct 2022 07:19:46 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c62048a8e1cdea8d371209fbde3cbeadd52a6ef42398dfa6e4960e8403f2267`  
		Last Modified: Tue, 25 Oct 2022 07:19:47 GMT  
		Size: 3.2 MB (3172530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f0b544af73c9c7216fee22b2fa68337d3b11bcddd4c8b05a2c1e0a97d3d9c4`  
		Last Modified: Tue, 25 Oct 2022 07:38:50 GMT  
		Size: 3.7 MB (3671938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.9-buster` - linux; 386

```console
$ docker pull hylang@sha256:e8f55831bfceb0772c5ee872ec820d8dc9be62f2e1c2938713ab17bf4fb10cbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48921743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f322c4234718b5fd4f601e5b76c7eba60bfc62903827c531283992ebe85e5b26`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 25 Oct 2022 02:23:02 GMT
ADD file:49981fa4bc36bce6e4fdd74b2c4429cc4faef5498c3d8fb20fb98b426bbf8c4d in / 
# Tue, 25 Oct 2022 02:23:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:56:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 02:56:01 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 03:50:58 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 25 Oct 2022 03:50:59 GMT
ENV PYTHON_VERSION=3.9.15
# Tue, 25 Oct 2022 03:58:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 25 Oct 2022 03:58:04 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 25 Oct 2022 03:58:05 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 25 Oct 2022 03:58:06 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 25 Oct 2022 03:58:07 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6d265be7a6b5bc4e9c5c07646aee0bf0394be03d/public/get-pip.py
# Tue, 25 Oct 2022 03:58:08 GMT
ENV PYTHON_GET_PIP_SHA256=36c6f6214694ef64cc70f4127ac0ccec668408a93825359d998fb31d24968d67
# Tue, 25 Oct 2022 03:58:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 25 Oct 2022 03:58:23 GMT
CMD ["python3"]
# Tue, 25 Oct 2022 04:39:58 GMT
ENV HY_VERSION=0.24.0
# Tue, 25 Oct 2022 04:39:58 GMT
ENV HYRULE_VERSION=0.2
# Tue, 25 Oct 2022 04:40:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 25 Oct 2022 04:40:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:32caca2e9abac2a8ffc2b083d202d57e1970d8adc212be17451a992441fad01b`  
		Last Modified: Tue, 25 Oct 2022 02:29:19 GMT  
		Size: 27.8 MB (27799224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b76fbf13d4fc0083f4fb8571e3d89a1b8a6b8bdfeed8cab34bbaaf466696b9`  
		Last Modified: Tue, 25 Oct 2022 04:33:33 GMT  
		Size: 2.8 MB (2788348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f60e14580a653b220156fa63b3cd74d4ced9052b44d1c4ee6c932d50946ddfe`  
		Last Modified: Tue, 25 Oct 2022 04:35:01 GMT  
		Size: 11.7 MB (11705174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dec964910603a0c4a0c5eb34e805d2dc81ecb19597e775eb0cc7427014a4270`  
		Last Modified: Tue, 25 Oct 2022 04:34:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb970481b146414a286b5364e598d86476750a1ee27a689c5eec19336c2b90b`  
		Last Modified: Tue, 25 Oct 2022 04:35:00 GMT  
		Size: 3.0 MB (2959108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7899617e4f4380f8c602f80677f334c0a6ffb065d13594c6d48e373968f546`  
		Last Modified: Tue, 25 Oct 2022 04:51:01 GMT  
		Size: 3.7 MB (3669656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
