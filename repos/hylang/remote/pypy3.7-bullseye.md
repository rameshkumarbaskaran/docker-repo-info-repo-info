## `hylang:pypy3.7-bullseye`

```console
$ docker pull hylang@sha256:251ccd7e718bb23e5256dd969084c30d64cebe54ef85e93933f2a2d23353a62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:pypy3.7-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:b01a3fa5a605d8395b883590844c5455c7e0f8381e6918bce14248fbf8941708
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73636587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1257a482d3e6b76a2ba0fd7f0aaaaa6d5042bc5413d9669de404a78de5eb45`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:06:24 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 03:06:25 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:06:25 GMT
ENV PYPY_VERSION=7.3.7
# Tue, 21 Dec 2021 03:11:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux64.tar.bz2'; 			sha256='8332f923755441fedfe4767a84601c94f4d6f8475384406cb5f259ad8d0b2002'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-aarch64.tar.bz2'; 			sha256='a1a84882525dd574c4b051b66e9b7ef0e132392acc2f729420d7825f96835216'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux32.tar.bz2'; 			sha256='0ab9e2e8ae1ac463bb811b9d3ba24d138f41f7378c17ca9e2d8dee51bf151d19'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-s390x.tar.bz2'; 			sha256='7f91efc65a69e727519cc885ca6351f4bfdd6b90580dced2fdcc9ae1bf10013b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Dec 2021 03:11:17 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Dec 2021 03:11:18 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Dec 2021 03:11:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Dec 2021 03:11:31 GMT
CMD ["pypy3"]
# Wed, 22 Dec 2021 09:35:18 GMT
ENV HY_VERSION=1.0a3
# Wed, 22 Dec 2021 09:35:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 22 Dec 2021 09:35:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4932d9ac796414ba200427eaa3a16cfe6654c1b039a6e2bf3ceaa5848b225f`  
		Last Modified: Tue, 21 Dec 2021 03:18:43 GMT  
		Size: 1.1 MB (1066001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33c432aa6896d933f7cb26d0d523001af2cf2fc9413446dba7042a95a0c5cb2`  
		Last Modified: Tue, 21 Dec 2021 03:20:49 GMT  
		Size: 35.8 MB (35774795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3371f61f669fe4fe5c4ed2193c450f71bab72ad307497a023e97e23952576cb`  
		Last Modified: Tue, 21 Dec 2021 03:20:41 GMT  
		Size: 2.4 MB (2371261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02042000088dc9df6510a47430a2fbe7c3f2ef3cff0325c02f235c418583b852`  
		Last Modified: Wed, 22 Dec 2021 09:39:50 GMT  
		Size: 3.1 MB (3066906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:6cb39deb2ea56a10b78840a6899ea229c515f378f5d30b50cd298c5530daf4a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68777563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890aea8370ddcfb34cbc19c0a37544f145ad57b81a2d4bb45b7cbb76b04bc5b9`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:23 GMT
ADD file:986f91febed4aa8e2072081ff8419d52ba2060510822e717086d3b3d9469e4d7 in / 
# Tue, 21 Dec 2021 01:42:24 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 08:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 08:31:41 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 08:31:42 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 08:31:43 GMT
ENV PYPY_VERSION=7.3.7
# Tue, 21 Dec 2021 08:35:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux64.tar.bz2'; 			sha256='8332f923755441fedfe4767a84601c94f4d6f8475384406cb5f259ad8d0b2002'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-aarch64.tar.bz2'; 			sha256='a1a84882525dd574c4b051b66e9b7ef0e132392acc2f729420d7825f96835216'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux32.tar.bz2'; 			sha256='0ab9e2e8ae1ac463bb811b9d3ba24d138f41f7378c17ca9e2d8dee51bf151d19'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-s390x.tar.bz2'; 			sha256='7f91efc65a69e727519cc885ca6351f4bfdd6b90580dced2fdcc9ae1bf10013b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Dec 2021 08:35:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Dec 2021 08:35:46 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Dec 2021 08:35:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Dec 2021 08:35:59 GMT
CMD ["pypy3"]
# Wed, 22 Dec 2021 02:47:03 GMT
ENV HY_VERSION=1.0a3
# Wed, 22 Dec 2021 02:47:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 22 Dec 2021 02:47:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:927a35006d93ea08499b57046904046d7926cd76fb17be193e3e74f56d634a08`  
		Last Modified: Tue, 21 Dec 2021 01:48:54 GMT  
		Size: 30.0 MB (30043793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487cc47b6db3d708ad04f3f9f424c4ca0f3f0a85687001043f1e1e90bb6d9789`  
		Last Modified: Tue, 21 Dec 2021 08:44:07 GMT  
		Size: 1.1 MB (1053973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d9e461af2da744d806f3a39a00f53ca59488092af2f7872ca08bdcaf0dde95`  
		Last Modified: Tue, 21 Dec 2021 08:46:09 GMT  
		Size: 32.5 MB (32457857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbac1a7347fa32417089463fb230765901d3377d0c44bcbcb139cfc7c6658c5e`  
		Last Modified: Tue, 21 Dec 2021 08:46:03 GMT  
		Size: 2.2 MB (2155623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc86be9360d4568ed795b2bcd175c91cd29116bf42f18e9dee479064338ce477`  
		Last Modified: Wed, 22 Dec 2021 02:53:51 GMT  
		Size: 3.1 MB (3066317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:9068802de95a4a5fa423850e63854324f085445d53d5d1c1bfe109fa7781ad83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73886783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552603685fb9ff8c0a42d2d30aef99107978085f71db9509ebf0a32a6039e01c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:06 GMT
ADD file:6b67a0d4d176747cc8cefbd105facde82f1795467bf02eb45e8385c91cdc9c41 in / 
# Tue, 21 Dec 2021 01:40:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:24:04 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:24:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 19:24:04 GMT
ENV PYPY_VERSION=7.3.7
# Tue, 21 Dec 2021 19:28:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux64.tar.bz2'; 			sha256='8332f923755441fedfe4767a84601c94f4d6f8475384406cb5f259ad8d0b2002'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-aarch64.tar.bz2'; 			sha256='a1a84882525dd574c4b051b66e9b7ef0e132392acc2f729420d7825f96835216'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux32.tar.bz2'; 			sha256='0ab9e2e8ae1ac463bb811b9d3ba24d138f41f7378c17ca9e2d8dee51bf151d19'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-s390x.tar.bz2'; 			sha256='7f91efc65a69e727519cc885ca6351f4bfdd6b90580dced2fdcc9ae1bf10013b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Dec 2021 19:28:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Dec 2021 19:28:58 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Dec 2021 19:29:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Dec 2021 19:29:13 GMT
CMD ["pypy3"]
# Wed, 22 Dec 2021 09:47:16 GMT
ENV HY_VERSION=1.0a3
# Wed, 22 Dec 2021 09:47:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 22 Dec 2021 09:47:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9b9a100d632569e96aeb2d7b0bc45bc436609bb61335815f207994f3b557f0f7`  
		Last Modified: Tue, 21 Dec 2021 01:48:45 GMT  
		Size: 32.4 MB (32370850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e665f9ad46214f4b0d93397c46596c9e51650092c273889e956bc5206feb933`  
		Last Modified: Tue, 21 Dec 2021 19:40:54 GMT  
		Size: 1.1 MB (1078403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c28d2cd38c0bff6330dfede59e07daa731b05b9d255c7371235d8c8f7233e96`  
		Last Modified: Tue, 21 Dec 2021 19:43:46 GMT  
		Size: 35.0 MB (34999647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e27422296432f00f7fb77cf03fac0b5919bfb6cef79e62428109d9d72aca760`  
		Last Modified: Tue, 21 Dec 2021 19:43:33 GMT  
		Size: 2.4 MB (2370916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ce85fcca98d1a3318ba0bbbe6f15b0c2846f14e100258cb738462807cc29c0`  
		Last Modified: Wed, 22 Dec 2021 09:54:26 GMT  
		Size: 3.1 MB (3066967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
