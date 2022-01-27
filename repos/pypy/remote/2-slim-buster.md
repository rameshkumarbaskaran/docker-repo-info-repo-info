## `pypy:2-slim-buster`

```console
$ docker pull pypy@sha256:efb1e3e30db39e2f22d994f2cd9db6b251b35e05ed03d49f46a1ea853278bfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-slim-buster` - linux; amd64

```console
$ docker pull pypy@sha256:4273ffdae4ae1c7d0dadc6547b547cc3b694e751fab8fc19f297a55fb463409f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64934851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fe925e1c242bf7429ea52d469f7e583514ba65eb4aff5985aaa6758d08f86e`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:08:35 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 03:08:35 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:15:12 GMT
ENV PYPY_VERSION=7.3.6
# Tue, 21 Dec 2021 03:15:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.6-linux64.tar.bz2'; 			sha256='82127f43fae6ce75d47d6c4539f8c1ea372e9c2dbfa40fae8b58351d522793a4'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.6-aarch64.tar.bz2'; 			sha256='90e9aafb310314938f54678d4d6d7db1163b57c9343e640b447112f74d7f9151'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.6-linux32.tar.bz2'; 			sha256='7a1145f3a278ffab4da0e2d4c4bd024ab8d67106a502e4bb7f6d67337e7af2b7'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Dec 2021 03:15:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Dec 2021 03:15:32 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Dec 2021 03:15:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Dec 2021 03:15:44 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9042c4fc606d343774abe31f261f6cc338214f41a992f15ef03e2cd915decfdb`  
		Last Modified: Tue, 21 Dec 2021 03:19:41 GMT  
		Size: 2.8 MB (2757916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35fe67f88a3e82a800161aeaedaec59ae300c9d577032a286b7a6ad18a1c64b`  
		Last Modified: Tue, 21 Dec 2021 03:25:03 GMT  
		Size: 32.9 MB (32854861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625c9c47324690302045e2efeeeb4a458c4998f1aa5727c4aa5caebb92d506c7`  
		Last Modified: Tue, 21 Dec 2021 03:24:57 GMT  
		Size: 2.2 MB (2168351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:f7abb0df117689080db881b14432f26c86971f64e4a2c88d222e680cccd93b2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60720644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f2c1b6582892e03d3d4abdb6837da3aa473833f2d1175841608b76c6343d7a`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 07:18:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 07:18:25 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 07:18:26 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 07:24:46 GMT
ENV PYPY_VERSION=7.3.6
# Wed, 26 Jan 2022 07:25:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.6-linux64.tar.bz2'; 			sha256='82127f43fae6ce75d47d6c4539f8c1ea372e9c2dbfa40fae8b58351d522793a4'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.6-aarch64.tar.bz2'; 			sha256='90e9aafb310314938f54678d4d6d7db1163b57c9343e640b447112f74d7f9151'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.6-linux32.tar.bz2'; 			sha256='7a1145f3a278ffab4da0e2d4c4bd024ab8d67106a502e4bb7f6d67337e7af2b7'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 26 Jan 2022 07:25:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Jan 2022 07:25:02 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Jan 2022 07:25:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Jan 2022 07:25:14 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb9bd4618813bb4cc63b8b9568068380b3faffa783988a338e688fd67defdee`  
		Last Modified: Wed, 26 Jan 2022 07:30:10 GMT  
		Size: 2.6 MB (2626740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea7e7a0ba115f27888cf4dcde2154c738373478cf22ae12bb9913768ab10724`  
		Last Modified: Wed, 26 Jan 2022 07:35:39 GMT  
		Size: 30.2 MB (30216188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b234346889417ff2ff7b51751a01f45561ea526f891371662a0de6195ed74552`  
		Last Modified: Wed, 26 Jan 2022 07:35:34 GMT  
		Size: 2.0 MB (1954500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-buster` - linux; 386

```console
$ docker pull pypy@sha256:fbd0a51f90b0ad6324a885732902ba811eb7ea9b47aa0a760ceff988990cd77d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63024934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ebeeb20c92482bbca72a658b80b1fe6d9c0dda0aa780135fb152bb6b4bc09b`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:30 GMT
ADD file:0d3811120feb1258b2cbe48be0a91ae3389643fb759b10b83b6534ebca8cf795 in / 
# Wed, 26 Jan 2022 01:40:31 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 21:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 21:18:09 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 21:18:09 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 21:25:37 GMT
ENV PYPY_VERSION=7.3.6
# Wed, 26 Jan 2022 21:25:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.6-linux64.tar.bz2'; 			sha256='82127f43fae6ce75d47d6c4539f8c1ea372e9c2dbfa40fae8b58351d522793a4'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.6-aarch64.tar.bz2'; 			sha256='90e9aafb310314938f54678d4d6d7db1163b57c9343e640b447112f74d7f9151'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.6-linux32.tar.bz2'; 			sha256='7a1145f3a278ffab4da0e2d4c4bd024ab8d67106a502e4bb7f6d67337e7af2b7'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 26 Jan 2022 21:25:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Jan 2022 21:25:59 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Jan 2022 21:26:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Jan 2022 21:26:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:79e14f2e0ab2370ab81617ee0b4757c6c2e55d326ad5c7b5290a5068e50176df`  
		Last Modified: Wed, 26 Jan 2022 01:50:05 GMT  
		Size: 27.8 MB (27804600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cb884b98f263b1de2aced2aed126582e71db9d6a378fa06c40f9feda03e727`  
		Last Modified: Wed, 26 Jan 2022 21:32:40 GMT  
		Size: 2.8 MB (2769426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e35403edec927d600b54a3093c41ae7d3ec3601f58b9991f06a97f39e577e8`  
		Last Modified: Wed, 26 Jan 2022 21:39:54 GMT  
		Size: 30.3 MB (30282539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d4b082ed7b141a93eff333ab1b091b9f17a2d3f63e3e6591748001f5234e6d`  
		Last Modified: Wed, 26 Jan 2022 21:39:45 GMT  
		Size: 2.2 MB (2168369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
