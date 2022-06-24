## `hylang:0-pypy-buster`

```console
$ docker pull hylang@sha256:3e00587fcc189b6c9b8a479c2c6b9d7a2f8da78d1d4e7d01b9af8e6736f4f61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `hylang:0-pypy-buster` - linux; amd64

```console
$ docker pull hylang@sha256:782c08992e003ce5e58d0b38fbb6a6a1d6e5f4734de102cac1d507a917496946
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74147913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d1a774d61b03d8a8f03b172a959cc16fc9be98d21e814c63339294eb57dddf`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 14:53:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 14:53:43 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 14:53:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 14:53:43 GMT
ENV PYPY_VERSION=7.3.4
# Sat, 10 Apr 2021 14:54:09 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux64.tar.bz2'; 			sha256='09d7298b44a38648a87995ec06e1e093761644e50f547c8bb0b2d7f4fe433548'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-aarch64.tar.bz2'; 			sha256='a4148fa73b74a091e004e1f378b278c0b8830984cbcb91e10fa31fd915c43efe'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-linux32.tar.bz2'; 			sha256='04de1a2e80530f3d74abcf133ec046a0fb12d81956bc043dee8ab4799f3b77eb'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.4-s390x.tar.bz2'; 			sha256='7d6fb180c359a66a158ef6e81eeca88fbabbb62656a1700f425a70db18de2a0f'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 10 Apr 2021 14:54:10 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Sat, 10 Apr 2021 14:54:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Sat, 10 Apr 2021 14:54:10 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Sat, 10 Apr 2021 14:54:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 10 Apr 2021 14:54:23 GMT
CMD ["pypy3"]
# Sun, 11 Apr 2021 06:25:59 GMT
ENV HY_VERSION=0.20.0
# Sun, 11 Apr 2021 06:26:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 11 Apr 2021 06:26:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3da5fcf5fa7542a53548bf7e7c8a6b703cce1920fbfd5e30a79641a1047c04`  
		Last Modified: Sat, 10 Apr 2021 14:57:13 GMT  
		Size: 2.8 MB (2757654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71dcb35be3554efe9eb06a6058f7ab16efd20c2ebbdab0904f03dc179b70e58`  
		Last Modified: Sat, 10 Apr 2021 14:57:23 GMT  
		Size: 38.6 MB (38598611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e771f6c47637605bf43be1997efb24f0a4f76ba789042de94048eea563685`  
		Last Modified: Sat, 10 Apr 2021 14:57:13 GMT  
		Size: 2.6 MB (2565634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62a145b82e9b7faeb1ba4f016709c8452a1607499e9e6537835113f2e35a57`  
		Last Modified: Sun, 11 Apr 2021 06:29:33 GMT  
		Size: 3.1 MB (3086641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:15487a63b8ad79538c76e2629bfbf7d741d99a90192ded0a8fe33dc8cc550d0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70134910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff8f760fdd61dca718925be73b650504194e970b03b1f6dc8ca1fa6986b420f`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 09:20:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 09:20:19 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 09:20:20 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 09:20:21 GMT
ENV PYPY_VERSION=7.3.9
# Thu, 23 Jun 2022 09:24:25 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-linux64.tar.bz2'; 			sha256='08be25ec82fc5d23b78563eda144923517daba481a90af0ace7a047c9c9a3c34'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-aarch64.tar.bz2'; 			sha256='5e124455e207425e80731dff317f0432fa0aba1f025845ffca813770e2447e32'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-linux32.tar.bz2'; 			sha256='4b261516c6c59078ab0c8bd7207327a1b97057b4ec1714ed5e79a026f9efd492'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-s390x.tar.bz2'; 			sha256='c6177a0016c9145c7b99fddb5d74cc2e518ccdb216a6deb51ef6a377510cc930'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 23 Jun 2022 09:24:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 23 Jun 2022 09:24:27 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 23 Jun 2022 09:24:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Jun 2022 09:24:43 GMT
CMD ["pypy3"]
# Thu, 23 Jun 2022 23:53:05 GMT
ENV HY_VERSION=0.24.0
# Thu, 23 Jun 2022 23:53:06 GMT
ENV HYRULE_VERSION=0.2
# Thu, 23 Jun 2022 23:53:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 23 Jun 2022 23:53:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65e9a35d6e11417897c8299f476e7807b507ed5f922f33987823ec3e79b3e02`  
		Last Modified: Thu, 23 Jun 2022 09:36:03 GMT  
		Size: 2.6 MB (2634720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6983efcd8f6895638225991f180ee70bb0872b3230ae6e09d4a30619390a7183`  
		Last Modified: Thu, 23 Jun 2022 09:38:50 GMT  
		Size: 34.7 MB (34679320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861a89c7f347308077a8721d62a3693b703c74fba3af32418c3a96b828e8d390`  
		Last Modified: Thu, 23 Jun 2022 09:38:44 GMT  
		Size: 3.0 MB (2951074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f3e52b012f909fb9af1f940d6728651292b86f8997cd0ad53f126df112068b`  
		Last Modified: Fri, 24 Jun 2022 00:06:13 GMT  
		Size: 4.0 MB (3955767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy-buster` - linux; 386

```console
$ docker pull hylang@sha256:4b2880a5b3f1b71d388837f15ca6fda15fd45ebd2a030678b2fb2dbb4df74028
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77045479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e7178e03d21cd1f6e412ea35af1420bb5c8123539feb8e585fac727bf2b6ca`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 13:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:53:31 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 13:53:32 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 13:53:33 GMT
ENV PYPY_VERSION=7.3.9
# Thu, 23 Jun 2022 13:57:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-linux64.tar.bz2'; 			sha256='08be25ec82fc5d23b78563eda144923517daba481a90af0ace7a047c9c9a3c34'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-aarch64.tar.bz2'; 			sha256='5e124455e207425e80731dff317f0432fa0aba1f025845ffca813770e2447e32'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-linux32.tar.bz2'; 			sha256='4b261516c6c59078ab0c8bd7207327a1b97057b4ec1714ed5e79a026f9efd492'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-s390x.tar.bz2'; 			sha256='c6177a0016c9145c7b99fddb5d74cc2e518ccdb216a6deb51ef6a377510cc930'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 23 Jun 2022 13:57:35 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 23 Jun 2022 13:57:36 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 23 Jun 2022 13:57:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Jun 2022 13:57:51 GMT
CMD ["pypy3"]
# Thu, 23 Jun 2022 19:39:05 GMT
ENV HY_VERSION=0.24.0
# Thu, 23 Jun 2022 19:39:05 GMT
ENV HYRULE_VERSION=0.2
# Thu, 23 Jun 2022 19:39:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 23 Jun 2022 19:39:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8e14a8c7e7d97fd835436948877c3f64ad665d78309b6b0160943c3680d184`  
		Last Modified: Thu, 23 Jun 2022 14:09:41 GMT  
		Size: 2.8 MB (2777773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212e78050e46d20494f411c84cde91515c0785c51049758eb76493e3108cfd40`  
		Last Modified: Thu, 23 Jun 2022 14:12:37 GMT  
		Size: 39.6 MB (39561412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2505ee00d6268dbf06bcf5014e2d11171a85ec69fc10d468c289cd8ee1737f1`  
		Last Modified: Thu, 23 Jun 2022 14:12:31 GMT  
		Size: 3.0 MB (2951076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233676be419e0218691c2f30bc22e4499e893af0946bb9d4c7135dd81a35ee60`  
		Last Modified: Thu, 23 Jun 2022 19:52:20 GMT  
		Size: 4.0 MB (3955676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy-buster` - linux; s390x

```console
$ docker pull hylang@sha256:623661fefd04eabef7e428bc1b791efc4c193e0f36fda756d50cebd680eb790e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70682230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76cb6a6560750e2b410c6acad4389d07b0018bffa3d1e9dc565741355014ce18`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jun 2022 00:44:04 GMT
ADD file:b5735387132c5d35278da27339d76ef4a166c7ea012cfe13bd542fd5f0055fb4 in / 
# Thu, 23 Jun 2022 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 09:21:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 09:21:06 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 09:21:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 09:21:06 GMT
ENV PYPY_VERSION=7.3.9
# Thu, 23 Jun 2022 09:23:46 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-linux64.tar.bz2'; 			sha256='08be25ec82fc5d23b78563eda144923517daba481a90af0ace7a047c9c9a3c34'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-aarch64.tar.bz2'; 			sha256='5e124455e207425e80731dff317f0432fa0aba1f025845ffca813770e2447e32'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-linux32.tar.bz2'; 			sha256='4b261516c6c59078ab0c8bd7207327a1b97057b4ec1714ed5e79a026f9efd492'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.9-s390x.tar.bz2'; 			sha256='c6177a0016c9145c7b99fddb5d74cc2e518ccdb216a6deb51ef6a377510cc930'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 23 Jun 2022 09:23:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 23 Jun 2022 09:23:53 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 23 Jun 2022 09:24:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Jun 2022 09:24:11 GMT
CMD ["pypy3"]
# Thu, 23 Jun 2022 22:03:56 GMT
ENV HY_VERSION=0.24.0
# Thu, 23 Jun 2022 22:03:56 GMT
ENV HYRULE_VERSION=0.2
# Thu, 23 Jun 2022 22:04:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 23 Jun 2022 22:04:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:34b063f6640cedaaed5292721bedcce5039c2e2c11d3168badb2d90259505d49`  
		Last Modified: Thu, 23 Jun 2022 00:52:35 GMT  
		Size: 25.8 MB (25758710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0957c95514edbb113040dded7bef91d1946472ff52e89cc0074be66c5a40f1b`  
		Last Modified: Thu, 23 Jun 2022 09:29:51 GMT  
		Size: 2.5 MB (2457477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77623fa2dbd15202a30566478723f165bb0364d4224d07d1c6ecd10644f3e9d5`  
		Last Modified: Thu, 23 Jun 2022 09:30:43 GMT  
		Size: 35.3 MB (35343762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899413d8230db9b2d534b7213408598a0f69f807181bf0bf1d12749c57a6570c`  
		Last Modified: Thu, 23 Jun 2022 09:30:37 GMT  
		Size: 3.2 MB (3166665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbfe52dbdca167b42ecd43a8911b3a3b1698e7d49cea1d85408f2386ae32195`  
		Last Modified: Thu, 23 Jun 2022 22:12:40 GMT  
		Size: 4.0 MB (3955616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
