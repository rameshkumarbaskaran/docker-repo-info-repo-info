## `hylang:pypy3.7-buster`

```console
$ docker pull hylang@sha256:61cbee564df3d443c33a90fc62458db0c06b659058acc6684e51743f7b76cd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `hylang:pypy3.7-buster` - linux; amd64

```console
$ docker pull hylang@sha256:d8c929d7eaf6840532ab2dcb2fedc5c9aa8c1385fbef385b0bb7a14dff083499
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72198338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c4759ac3c346d90e69451c9a063cd1a97b75ea67ce4ef4e6000e0cb3277cd9`
-	Default Command: `["hy"]`

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
# Tue, 21 Dec 2021 03:08:35 GMT
ENV PYPY_VERSION=7.3.7
# Tue, 21 Dec 2021 03:12:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux64.tar.bz2'; 			sha256='8332f923755441fedfe4767a84601c94f4d6f8475384406cb5f259ad8d0b2002'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-aarch64.tar.bz2'; 			sha256='a1a84882525dd574c4b051b66e9b7ef0e132392acc2f729420d7825f96835216'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux32.tar.bz2'; 			sha256='0ab9e2e8ae1ac463bb811b9d3ba24d138f41f7378c17ca9e2d8dee51bf151d19'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-s390x.tar.bz2'; 			sha256='7f91efc65a69e727519cc885ca6351f4bfdd6b90580dced2fdcc9ae1bf10013b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Dec 2021 03:12:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Dec 2021 03:12:51 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Dec 2021 03:13:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Dec 2021 03:13:03 GMT
CMD ["pypy3"]
# Wed, 22 Dec 2021 09:35:31 GMT
ENV HY_VERSION=1.0a3
# Wed, 22 Dec 2021 09:35:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 22 Dec 2021 09:35:40 GMT
CMD ["hy"]
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
	-	`sha256:40668b105069d1d95ea395aeeec9998fb8d5a2e539d1781771722c4ceeb354a9`  
		Last Modified: Tue, 21 Dec 2021 03:22:25 GMT  
		Size: 36.9 MB (36852776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762b3ff0af940345222bf423da0eb487c2de7ac548556e035c4d687de56f944f`  
		Last Modified: Tue, 21 Dec 2021 03:22:18 GMT  
		Size: 2.4 MB (2367097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e35733d23773f5e52983450d17a8728581c2fa4abd24dcf448688ae9c4947e`  
		Last Modified: Wed, 22 Dec 2021 09:40:00 GMT  
		Size: 3.1 MB (3066826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:7a581685c1642680be1b982593bcd3a5742a334f3feb15b2a04addc0851cd206
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66874996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688591a209a72e396d810a8e3965709ec6fdb54e0b1da0551aa7d7453efdcc2a`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 08:33:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 08:33:34 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 08:33:35 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 08:33:36 GMT
ENV PYPY_VERSION=7.3.7
# Tue, 21 Dec 2021 08:37:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux64.tar.bz2'; 			sha256='8332f923755441fedfe4767a84601c94f4d6f8475384406cb5f259ad8d0b2002'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-aarch64.tar.bz2'; 			sha256='a1a84882525dd574c4b051b66e9b7ef0e132392acc2f729420d7825f96835216'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux32.tar.bz2'; 			sha256='0ab9e2e8ae1ac463bb811b9d3ba24d138f41f7378c17ca9e2d8dee51bf151d19'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-s390x.tar.bz2'; 			sha256='7f91efc65a69e727519cc885ca6351f4bfdd6b90580dced2fdcc9ae1bf10013b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Dec 2021 08:37:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Dec 2021 08:37:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Dec 2021 08:37:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Dec 2021 08:37:42 GMT
CMD ["pypy3"]
# Wed, 22 Dec 2021 02:47:22 GMT
ENV HY_VERSION=1.0a3
# Wed, 22 Dec 2021 02:47:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 22 Dec 2021 02:47:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce98105ec7bcb69bd5ea43acc2a74e652c869999b7c2a6c6f8904d46f8a66f5`  
		Last Modified: Tue, 21 Dec 2021 08:45:04 GMT  
		Size: 2.6 MB (2626721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a502c454021e68a743d7cfbc07fb6d3e4d183a28ea1e28fed2b4bfe3df6b9f9`  
		Last Modified: Tue, 21 Dec 2021 08:47:49 GMT  
		Size: 33.1 MB (33104091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb3f48ffbcd47664ed3c59053e7435d6628e25e27463ae10b55802b09930d63`  
		Last Modified: Tue, 21 Dec 2021 08:47:44 GMT  
		Size: 2.2 MB (2154685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c181cf3f3556981462b2d2204642aaa2cc2feae859aa6faa43818804c32996`  
		Last Modified: Wed, 22 Dec 2021 02:54:03 GMT  
		Size: 3.1 MB (3066350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7-buster` - linux; 386

```console
$ docker pull hylang@sha256:0ffa4f0c106ea128fcc3d611dd617a23dccf1438db1405a4b799c30e203c2f39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74759439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c62aa55c66f3b5d8d3a01e1f7786b7a9c211c1133ffc699e48f4b58260f0650`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:45 GMT
ADD file:78342a77df22ca22804ea5aec6415ce10c1fdc35687f1b25c5f86850f41d3905 in / 
# Tue, 21 Dec 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:26:24 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:26:24 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 19:26:25 GMT
ENV PYPY_VERSION=7.3.7
# Tue, 21 Dec 2021 19:30:46 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux64.tar.bz2'; 			sha256='8332f923755441fedfe4767a84601c94f4d6f8475384406cb5f259ad8d0b2002'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-aarch64.tar.bz2'; 			sha256='a1a84882525dd574c4b051b66e9b7ef0e132392acc2f729420d7825f96835216'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux32.tar.bz2'; 			sha256='0ab9e2e8ae1ac463bb811b9d3ba24d138f41f7378c17ca9e2d8dee51bf151d19'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-s390x.tar.bz2'; 			sha256='7f91efc65a69e727519cc885ca6351f4bfdd6b90580dced2fdcc9ae1bf10013b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Dec 2021 19:30:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Dec 2021 19:30:46 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Dec 2021 19:30:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Dec 2021 19:30:58 GMT
CMD ["pypy3"]
# Wed, 22 Dec 2021 09:47:32 GMT
ENV HY_VERSION=1.0a3
# Wed, 22 Dec 2021 09:47:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 22 Dec 2021 09:47:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:16e3a221bce3a5f7f4a71f72926f381ff9c6141ccb5918b7ea924ff7f7f09d06`  
		Last Modified: Tue, 21 Dec 2021 01:49:46 GMT  
		Size: 27.8 MB (27804573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1c7323eed82cc9a890412560fff7b2d1e599404b4eb90bd6a952b3f130f8d3`  
		Last Modified: Tue, 21 Dec 2021 19:42:15 GMT  
		Size: 2.8 MB (2769497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dac1e7210c67e1a934f68fc23b691cc31e696966e41a134d14fa00eda39a4c`  
		Last Modified: Tue, 21 Dec 2021 19:46:17 GMT  
		Size: 38.8 MB (38751563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6b69c28a56601f912b6a6a614285f2f6ac6b6cd62ee8f8c0427f7dda900391`  
		Last Modified: Tue, 21 Dec 2021 19:46:02 GMT  
		Size: 2.4 MB (2366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f9e50f18c29a17634a7c204c01432f1d0210f3494ae1edf0156f68490f6c57`  
		Last Modified: Wed, 22 Dec 2021 09:54:38 GMT  
		Size: 3.1 MB (3066916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7-buster` - linux; s390x

```console
$ docker pull hylang@sha256:4c1c00cdef88a1602a25fc42880c65f03a3c27f12ae03995fe271b0079b95fd1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68095729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528df2b1489bbc718c7d2ab38c7c9109874e8f44888d0631096fdcb1dd785f28`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:57 GMT
ADD file:33e37861eefa46f6e5f7f4967ce8ae3167e28bc817c3c71ff90a3d51e2376a0f in / 
# Tue, 21 Dec 2021 01:42:59 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 08:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 08:13:03 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 08:13:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 08:13:03 GMT
ENV PYPY_VERSION=7.3.7
# Tue, 21 Dec 2021 08:14:41 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux64.tar.bz2'; 			sha256='8332f923755441fedfe4767a84601c94f4d6f8475384406cb5f259ad8d0b2002'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-aarch64.tar.bz2'; 			sha256='a1a84882525dd574c4b051b66e9b7ef0e132392acc2f729420d7825f96835216'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-linux32.tar.bz2'; 			sha256='0ab9e2e8ae1ac463bb811b9d3ba24d138f41f7378c17ca9e2d8dee51bf151d19'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.7-s390x.tar.bz2'; 			sha256='7f91efc65a69e727519cc885ca6351f4bfdd6b90580dced2fdcc9ae1bf10013b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Dec 2021 08:14:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Dec 2021 08:14:43 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Dec 2021 08:14:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Dec 2021 08:14:52 GMT
CMD ["pypy3"]
# Tue, 21 Dec 2021 18:38:31 GMT
ENV HY_VERSION=1.0a3
# Tue, 21 Dec 2021 18:38:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 21 Dec 2021 18:38:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:10979941d091693f28e3dc033cc6ca88996acf42a0aace27ad85fbd894945e20`  
		Last Modified: Tue, 21 Dec 2021 01:48:51 GMT  
		Size: 25.8 MB (25769051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41ab1397a6870c639751bc7c1dd0964c8ed355c1f6ecd3c374a1c5f32b1deed`  
		Last Modified: Tue, 21 Dec 2021 08:16:12 GMT  
		Size: 2.5 MB (2452718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76314228fa4246e3ac73de1a5190c6b5a19957bafc8a8fbe96f9283612b77fef`  
		Last Modified: Tue, 21 Dec 2021 08:17:00 GMT  
		Size: 34.4 MB (34439692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdeaf27ffcaab8153c6c6076066581896aabca4f53da1d82b54549d3f48af99`  
		Last Modified: Tue, 21 Dec 2021 08:16:54 GMT  
		Size: 2.4 MB (2367385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610dc1923b0da0901a66c1bc88092d5c0914683ff7c1d02d1ad0c2b52833d22b`  
		Last Modified: Tue, 21 Dec 2021 18:44:24 GMT  
		Size: 3.1 MB (3066883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
