## `hylang:0-pypy3.6-buster`

```console
$ docker pull hylang@sha256:b21b82bce3ab4d4baea5cf77562e64d7970d474cbbd757cc9b62fe5468cfd917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `hylang:0-pypy3.6-buster` - linux; amd64

```console
$ docker pull hylang@sha256:c09e9e2f9804e104db60a654620d2ef6e50fdfde9e8b59febc5df9466ad6c320
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70985395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771d86dbcc77c302bcca57cd572bead80073a542673eb1d1392430704ff75937`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:33:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:33:42 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 22:33:42 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 22:33:43 GMT
ENV PYPY_VERSION=7.3.3
# Fri, 12 Mar 2021 22:36:34 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-linux64.tar.bz2'; 			sha256='4fb85fdd516482cab727bb9473b066ff8fb672940dedf7ccc32bf92957d29e0a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-aarch64.tar.bz2'; 			sha256='bc82cf7f0182b942a2cfad4a0d167f364bfbf18f434e100a2fe62bc88547ac9b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-linux32.tar.bz2'; 			sha256='f183c61e66fd2c536a65695bd7ff770748c2884c235a589b9c6ac63690770c69'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-s390x.tar.bz2'; 			sha256='0de9c33ff3500c6e7fd273d0a6d341bc839b0298f697c4d6fe141f2b54c5c3e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		wget -O import.patch 'https://foss.heptapod.net/pypy/pypy/-/commit/16faa2be85839e6ab4fb8ee09298a4d934aab81f.patch'; 	echo '2d4bcc434077685a4ff26c1c1f28109ff67ef7e68f1f831ce0f2d9ddd6a194d0 *import.patch' | sha256sum --check --strict -; 	wget -O crypt-utf8.patch 'https://foss.heptapod.net/pypy/pypy/-/commit/c63da169246ed972fe90e1c289fc2378236fa852.patch'; 	echo 'ab1529948c49fd29fb76b3c20ec7d3d9c50603aa0c549a8a31339eb940e0f4d3 *crypt-utf8.patch' | sha256sum --check --strict -; 	patch --input="$PWD/import.patch" --directory=/opt/pypy --strip=1; 	patch --input="$PWD/crypt-utf8.patch" --directory=/opt/pypy --strip=1; 	rm import.patch crypt-utf8.patch; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 12 Mar 2021 22:36:35 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Fri, 12 Mar 2021 22:36:35 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 12 Mar 2021 22:36:36 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 12 Mar 2021 22:36:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Mar 2021 22:36:53 GMT
CMD ["pypy3"]
# Sat, 13 Mar 2021 11:50:54 GMT
ENV HY_VERSION=0.20.0
# Sat, 13 Mar 2021 11:51:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Mar 2021 11:51:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ba48e4b20850c5500358c75e72b54ecf60fda55f561a907078d5011bbda63a`  
		Last Modified: Fri, 12 Mar 2021 22:40:36 GMT  
		Size: 2.8 MB (2757571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eb4e99d3aae97d1fc75904f49073034e07de53d52d3fccae25c17d3246a205`  
		Last Modified: Fri, 12 Mar 2021 22:42:03 GMT  
		Size: 35.7 MB (35694551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ee5faf0972309e71cdbfca0582b386fdc23ba41433e97d55b1c349b5f9c7a`  
		Last Modified: Fri, 12 Mar 2021 22:41:56 GMT  
		Size: 2.4 MB (2414698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cd37ea6e19a4c4307cfd728883de5ca53490f415a129f8945396cb1e1f292`  
		Last Modified: Sat, 13 Mar 2021 11:57:26 GMT  
		Size: 3.0 MB (3017574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.6-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4ab7699d2ceaa9ca4f9f724dab7a02e0026b0c1cef116bba9370e73b9a8e671a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63387073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da56d42c83541af628710a4bf19e6295e5efc3bdd8c792f1fe393e207ec7e7b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:53 GMT
ADD file:6130ddc0a939dd72c0614de4aa77de47aa16fe211274bacb31995aa1a0526164 in / 
# Fri, 12 Mar 2021 01:53:56 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 13:53:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 13:53:29 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 13:53:30 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 13:53:30 GMT
ENV PYPY_VERSION=7.3.3
# Fri, 12 Mar 2021 13:57:36 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-linux64.tar.bz2'; 			sha256='4fb85fdd516482cab727bb9473b066ff8fb672940dedf7ccc32bf92957d29e0a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-aarch64.tar.bz2'; 			sha256='bc82cf7f0182b942a2cfad4a0d167f364bfbf18f434e100a2fe62bc88547ac9b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-linux32.tar.bz2'; 			sha256='f183c61e66fd2c536a65695bd7ff770748c2884c235a589b9c6ac63690770c69'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-s390x.tar.bz2'; 			sha256='0de9c33ff3500c6e7fd273d0a6d341bc839b0298f697c4d6fe141f2b54c5c3e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		wget -O import.patch 'https://foss.heptapod.net/pypy/pypy/-/commit/16faa2be85839e6ab4fb8ee09298a4d934aab81f.patch'; 	echo '2d4bcc434077685a4ff26c1c1f28109ff67ef7e68f1f831ce0f2d9ddd6a194d0 *import.patch' | sha256sum --check --strict -; 	wget -O crypt-utf8.patch 'https://foss.heptapod.net/pypy/pypy/-/commit/c63da169246ed972fe90e1c289fc2378236fa852.patch'; 	echo 'ab1529948c49fd29fb76b3c20ec7d3d9c50603aa0c549a8a31339eb940e0f4d3 *crypt-utf8.patch' | sha256sum --check --strict -; 	patch --input="$PWD/import.patch" --directory=/opt/pypy --strip=1; 	patch --input="$PWD/crypt-utf8.patch" --directory=/opt/pypy --strip=1; 	rm import.patch crypt-utf8.patch; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 12 Mar 2021 13:57:38 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Fri, 12 Mar 2021 13:57:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 12 Mar 2021 13:57:40 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 12 Mar 2021 13:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Mar 2021 13:58:14 GMT
CMD ["pypy3"]
# Sat, 13 Mar 2021 05:16:18 GMT
ENV HY_VERSION=0.20.0
# Sat, 13 Mar 2021 05:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Mar 2021 05:16:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:706ee5d0a6b53d9257cbea22d8409fb22c867ab3a001c65f6b8bfd37dace0e58`  
		Last Modified: Fri, 12 Mar 2021 02:01:39 GMT  
		Size: 25.9 MB (25856512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6066cc2e1a9243c318aaa83f9a37f6c96902f9d8713f039f255dfbfc74f819`  
		Last Modified: Fri, 12 Mar 2021 14:02:43 GMT  
		Size: 2.6 MB (2626142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff00948a4af650eac7c105767f711594ddc72db9a96d6942a53f19f4c9fb8ece`  
		Last Modified: Fri, 12 Mar 2021 14:03:55 GMT  
		Size: 29.5 MB (29471318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c02588d8e40a1c5d4222373b66b06709efe700e2230d0a45d849d20db634436`  
		Last Modified: Fri, 12 Mar 2021 14:03:46 GMT  
		Size: 2.4 MB (2415332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb9a70c7e6ddbf9de54336df7fdef1cb152621730761bb6134ed5c652cf24ab`  
		Last Modified: Sat, 13 Mar 2021 05:19:40 GMT  
		Size: 3.0 MB (3017769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.6-buster` - linux; 386

```console
$ docker pull hylang@sha256:7f3bd36a48f1ea76d7320ab08d540afa71671a399cb1eeed16be91e0c8895248
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73958963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821313d359d60552811e63cc4fd4dfb415bec09435b248f5d9a04561a7a85fc3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Mar 2021 01:44:27 GMT
ADD file:90c103e04bd6fe0f39733cbf8eb2d8845aed3e4fc3fd1e5c3354df69e40aa615 in / 
# Fri, 12 Mar 2021 01:44:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 21:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:18:54 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 21:18:54 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 21:18:54 GMT
ENV PYPY_VERSION=7.3.3
# Fri, 12 Mar 2021 21:21:44 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-linux64.tar.bz2'; 			sha256='4fb85fdd516482cab727bb9473b066ff8fb672940dedf7ccc32bf92957d29e0a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-aarch64.tar.bz2'; 			sha256='bc82cf7f0182b942a2cfad4a0d167f364bfbf18f434e100a2fe62bc88547ac9b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-linux32.tar.bz2'; 			sha256='f183c61e66fd2c536a65695bd7ff770748c2884c235a589b9c6ac63690770c69'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-s390x.tar.bz2'; 			sha256='0de9c33ff3500c6e7fd273d0a6d341bc839b0298f697c4d6fe141f2b54c5c3e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		wget -O import.patch 'https://foss.heptapod.net/pypy/pypy/-/commit/16faa2be85839e6ab4fb8ee09298a4d934aab81f.patch'; 	echo '2d4bcc434077685a4ff26c1c1f28109ff67ef7e68f1f831ce0f2d9ddd6a194d0 *import.patch' | sha256sum --check --strict -; 	wget -O crypt-utf8.patch 'https://foss.heptapod.net/pypy/pypy/-/commit/c63da169246ed972fe90e1c289fc2378236fa852.patch'; 	echo 'ab1529948c49fd29fb76b3c20ec7d3d9c50603aa0c549a8a31339eb940e0f4d3 *crypt-utf8.patch' | sha256sum --check --strict -; 	patch --input="$PWD/import.patch" --directory=/opt/pypy --strip=1; 	patch --input="$PWD/crypt-utf8.patch" --directory=/opt/pypy --strip=1; 	rm import.patch crypt-utf8.patch; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 12 Mar 2021 21:21:44 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Fri, 12 Mar 2021 21:21:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 12 Mar 2021 21:21:45 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 12 Mar 2021 21:22:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Mar 2021 21:22:03 GMT
CMD ["pypy3"]
# Sat, 13 Mar 2021 00:29:06 GMT
ENV HY_VERSION=0.20.0
# Sat, 13 Mar 2021 00:29:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 13 Mar 2021 00:29:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0898aa7472f57f223652846337cf862f142e109d0c039b41886e7f20c345f85e`  
		Last Modified: Fri, 12 Mar 2021 01:52:08 GMT  
		Size: 27.8 MB (27760948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c875064fad6d2298c98cda6cc9ae19e78ba1d8bcc7a895090af0b1e99f522f`  
		Last Modified: Fri, 12 Mar 2021 21:27:50 GMT  
		Size: 2.8 MB (2769467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac110df9efcf7fcb3bde998b985fb2719117566db417a6c91af7e95723403c81`  
		Last Modified: Fri, 12 Mar 2021 21:29:57 GMT  
		Size: 38.0 MB (37996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bca94bc60d68a4f11fd795b540264a293de1e4d354b7113bdb0d9d0ebbd045`  
		Last Modified: Fri, 12 Mar 2021 21:29:46 GMT  
		Size: 2.4 MB (2414472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9535174d1b3a2b8199519d39eb7e23009f8381cc5ff2ca6a8b626e58d7f7fd`  
		Last Modified: Sat, 13 Mar 2021 00:41:10 GMT  
		Size: 3.0 MB (3017685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.6-buster` - linux; s390x

```console
$ docker pull hylang@sha256:9d4cb3efc6c2a8f6e08449f5e7d9ea96afe2bf1629f9b3619ab75595ca917fa9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66245560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4c8da8be8d4bd4ea1f40d1f793218936f1105259f8d49fafa2fe1f6f535d25`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Mar 2021 01:46:04 GMT
ADD file:afec039adf230a9186a38b57eed85262696f8d178ac649a445657066f16fe806 in / 
# Fri, 12 Mar 2021 01:46:07 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 04:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 04:53:27 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 04:53:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 04:53:28 GMT
ENV PYPY_VERSION=7.3.3
# Fri, 12 Mar 2021 04:55:46 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-linux64.tar.bz2'; 			sha256='4fb85fdd516482cab727bb9473b066ff8fb672940dedf7ccc32bf92957d29e0a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-aarch64.tar.bz2'; 			sha256='bc82cf7f0182b942a2cfad4a0d167f364bfbf18f434e100a2fe62bc88547ac9b'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-linux32.tar.bz2'; 			sha256='f183c61e66fd2c536a65695bd7ff770748c2884c235a589b9c6ac63690770c69'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.6-v7.3.3-s390x.tar.bz2'; 			sha256='0de9c33ff3500c6e7fd273d0a6d341bc839b0298f697c4d6fe141f2b54c5c3e2'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		wget -O import.patch 'https://foss.heptapod.net/pypy/pypy/-/commit/16faa2be85839e6ab4fb8ee09298a4d934aab81f.patch'; 	echo '2d4bcc434077685a4ff26c1c1f28109ff67ef7e68f1f831ce0f2d9ddd6a194d0 *import.patch' | sha256sum --check --strict -; 	wget -O crypt-utf8.patch 'https://foss.heptapod.net/pypy/pypy/-/commit/c63da169246ed972fe90e1c289fc2378236fa852.patch'; 	echo 'ab1529948c49fd29fb76b3c20ec7d3d9c50603aa0c549a8a31339eb940e0f4d3 *crypt-utf8.patch' | sha256sum --check --strict -; 	patch --input="$PWD/import.patch" --directory=/opt/pypy --strip=1; 	patch --input="$PWD/crypt-utf8.patch" --directory=/opt/pypy --strip=1; 	rm import.patch crypt-utf8.patch; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 12 Mar 2021 04:55:49 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Fri, 12 Mar 2021 04:55:49 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 12 Mar 2021 04:55:50 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 12 Mar 2021 04:56:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Mar 2021 04:56:04 GMT
CMD ["pypy3"]
# Fri, 12 Mar 2021 12:50:35 GMT
ENV HY_VERSION=0.20.0
# Fri, 12 Mar 2021 12:50:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 12 Mar 2021 12:50:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d41215965c091534e809ab2e8f4a2c1cebee3de536c2c74a7bc8302bbc8af7e1`  
		Last Modified: Fri, 12 Mar 2021 01:50:30 GMT  
		Size: 25.7 MB (25716294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d910d2cdc8d3e1f74022262fc8995940046c1397abb26a9436ae0e942f198f`  
		Last Modified: Fri, 12 Mar 2021 04:57:02 GMT  
		Size: 2.5 MB (2452237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f001ce4b32dc0671b7fef517bc4db120652128e4857e0ac620d2a9c8be42a207`  
		Last Modified: Fri, 12 Mar 2021 04:57:49 GMT  
		Size: 32.6 MB (32644835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34500713d6916510a8fd6daee05f0354f2f09cf5894bd0ddd7b22609acba406`  
		Last Modified: Fri, 12 Mar 2021 04:57:43 GMT  
		Size: 2.4 MB (2414662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76dc86ae5ff4ce1c8b3e49a864c28db289239606b76a7c9cdbf760ce1e6c01d`  
		Last Modified: Fri, 12 Mar 2021 12:53:07 GMT  
		Size: 3.0 MB (3017532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
