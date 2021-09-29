## `hylang:pypy-bullseye`

```console
$ docker pull hylang@sha256:7248a1d7f6ef318dd2a0e7524c52b0f966c3022a5dc5400ba8bed17e38057684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:pypy-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:3e8bdb441ac4739048dca56c89e8490aca27a284f7492a664eca8e666b64c670
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75378186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fa4fc4f64ebaaa6a842226ed843e8e3bd04bbfb9c254597c272e8acec6633f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:40 GMT
ADD file:3c520ad50b13b922356e0a5e4f7c12b202e09584acf332a65d5603dacd4a9380 in / 
# Tue, 28 Sep 2021 01:22:41 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 17:36:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 17:37:00 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 17:37:00 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 17:37:00 GMT
ENV PYPY_VERSION=7.3.5
# Tue, 28 Sep 2021 17:37:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 28 Sep 2021 17:37:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 28 Sep 2021 17:37:30 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 28 Sep 2021 17:37:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 28 Sep 2021 17:37:43 GMT
CMD ["pypy3"]
# Wed, 29 Sep 2021 15:31:55 GMT
ENV HY_VERSION=1.0a3
# Wed, 29 Sep 2021 15:32:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Sep 2021 15:32:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bd897bb914af2ec64f1cff5856aefa1ae99b072e38db0b7d801f9679b04aad74`  
		Last Modified: Tue, 28 Sep 2021 01:29:00 GMT  
		Size: 31.4 MB (31368912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd9d3ec718210872a6f18ef672054055f038261ebd32aa4df7775f1565bc1b9`  
		Last Modified: Tue, 28 Sep 2021 17:44:19 GMT  
		Size: 1.1 MB (1065963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec1e8d9ab4b995a74d31e5a234db378c14774c7a7c6ac267540c22ff1301da6`  
		Last Modified: Tue, 28 Sep 2021 17:44:26 GMT  
		Size: 37.5 MB (37507866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0d78b380c6622d993eace26b4389266f24f82b6e652154d5ee0436f344dc7c`  
		Last Modified: Tue, 28 Sep 2021 17:44:19 GMT  
		Size: 2.4 MB (2370060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca34c14e118c47c7db42e4c6596b45b68e668f13da5bfa78d640dbdc3615fb4`  
		Last Modified: Wed, 29 Sep 2021 15:35:58 GMT  
		Size: 3.1 MB (3065385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:68c6b25a42e0a73f4bdd6ba10c0937e0bc66819b2dc7233ac929768a9448c74f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71242126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e8750641bf4e1c87e1391f3b611f763902138078a592e39e21dd55174ea0d4`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:43 GMT
ADD file:6472ab63529e688735f77634402740e08fdbd5bfa788c150915027993df7e8ec in / 
# Tue, 28 Sep 2021 01:40:44 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 12:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:02:00 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 12:02:00 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 12:02:00 GMT
ENV PYPY_VERSION=7.3.5
# Tue, 28 Sep 2021 12:02:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 28 Sep 2021 12:02:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 28 Sep 2021 12:02:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 28 Sep 2021 12:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 28 Sep 2021 12:02:43 GMT
CMD ["pypy3"]
# Wed, 29 Sep 2021 08:27:53 GMT
ENV HY_VERSION=1.0a3
# Wed, 29 Sep 2021 08:28:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Sep 2021 08:28:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2f8871a8654eb1158cb626f8dc69992dba7e4bd8796fae6aa7cf967f951f5fe9`  
		Last Modified: Tue, 28 Sep 2021 01:48:25 GMT  
		Size: 30.1 MB (30055408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94099b465737cd09959ba4ad22539303d55aa2988ade117a6a70f45ef56cd7c`  
		Last Modified: Tue, 28 Sep 2021 12:11:19 GMT  
		Size: 1.1 MB (1054036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928ae88c6df42dc43a638a151209228eba9d7d058426262f09dc67441f5878c2`  
		Last Modified: Tue, 28 Sep 2021 12:11:26 GMT  
		Size: 34.7 MB (34697315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d027d9abe74dfdbc6e8c37c1550298159af943aa8f3264fc4f52e2dfeb2527ca`  
		Last Modified: Tue, 28 Sep 2021 12:11:20 GMT  
		Size: 2.4 MB (2369980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4dde2796ca8f269ff64b76e59382e91660cedbba6df1882f67bb90cd1a35`  
		Last Modified: Wed, 29 Sep 2021 08:34:08 GMT  
		Size: 3.1 MB (3065387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:b1c6b48f5dab172b121e9e4510dc76128b9337a41391e33f7130633effc72956
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75725782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c396ff5f16e4d9f2d114fe041269e15a8b9b9ca7a1a97d08e633aa7c821bf8`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:08 GMT
ADD file:8466bd8df052ea7fa26e49575ac95fd4934ddafdad54a9736ac2bd8e7fc6e735 in / 
# Tue, 28 Sep 2021 01:40:08 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 18:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 18:51:06 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 18:51:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 18:51:07 GMT
ENV PYPY_VERSION=7.3.5
# Tue, 28 Sep 2021 18:51:42 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 28 Sep 2021 18:51:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 28 Sep 2021 18:51:43 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 28 Sep 2021 18:52:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 28 Sep 2021 18:52:03 GMT
CMD ["pypy3"]
# Wed, 29 Sep 2021 06:18:52 GMT
ENV HY_VERSION=1.0a3
# Wed, 29 Sep 2021 06:19:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Sep 2021 06:19:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e79fce1f6442094a82dc5f6b4d1aa352e04aae39bba821c9021f6da08b1cacaf`  
		Last Modified: Tue, 28 Sep 2021 01:49:07 GMT  
		Size: 32.4 MB (32380160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83f7871b19aaf1dd169900512e21509617a34ee22f63b05f59482201c81615`  
		Last Modified: Tue, 28 Sep 2021 19:02:34 GMT  
		Size: 1.1 MB (1078350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833528e397fbbbef4b7cdadb8e3d0e8acb26c08d9f953381ef83b3f97a14dec4`  
		Last Modified: Tue, 28 Sep 2021 19:02:44 GMT  
		Size: 36.8 MB (36832097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de8ff2c323b98b193ec31865815854784f2341858c5a3b24b66b3ad5ec7c967`  
		Last Modified: Tue, 28 Sep 2021 19:02:34 GMT  
		Size: 2.4 MB (2369817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1561fd6e1ad8c4f12fc2274e17fa197651a3ffcdc430e83e69c43e3bbb0f83`  
		Last Modified: Wed, 29 Sep 2021 06:25:22 GMT  
		Size: 3.1 MB (3065358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
