## `hylang:pypy3.9-buster`

```console
$ docker pull hylang@sha256:86e185fcfb17534972cc57b8165e2d528d7ff7124b5d5afd84ad96ab5afcb1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `hylang:pypy3.9-buster` - linux; amd64

```console
$ docker pull hylang@sha256:c0e78557398292ab4106721b0ba30f339ca001d3d56208c9bc73b1811ab0cbfd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74359265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7867aaa9128c1536bbd4fbf824b5da273081de5f465c0059d8161b130d7823`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 10:05:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 10:05:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 10:05:42 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 10:05:42 GMT
ENV PYPY_VERSION=7.3.9
# Sat, 28 May 2022 10:06:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-linux64.tar.bz2'; 			sha256='46818cb3d74b96b34787548343d266e2562b531ddbaf330383ba930ff1930ed5'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-aarch64.tar.bz2'; 			sha256='2e1ae193d98bc51439642a7618d521ea019f45b8fb226940f7e334c548d2b4b9'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-linux32.tar.bz2'; 			sha256='0de4b9501cf28524cdedcff5052deee9ea4630176a512bdc408edfa30914bae7'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-s390x.tar.bz2'; 			sha256='774dca83bcb4403fb99b3d155e7bd572ef8c52b9fe87a657109f64e75ad71732'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 28 May 2022 10:06:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Sat, 28 May 2022 10:06:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Sat, 28 May 2022 10:06:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 May 2022 10:06:25 GMT
CMD ["pypy3"]
# Sun, 29 May 2022 04:30:34 GMT
ENV HY_VERSION=1.0a4
# Sun, 29 May 2022 04:30:34 GMT
ENV HYRULE_VERSION=0.1
# Sun, 29 May 2022 04:30:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sun, 29 May 2022 04:30:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3b68ff260cdbc73da579f62c78922333daa2bf2ab5e10ffdb4f7cdf17d90a1`  
		Last Modified: Sat, 28 May 2022 10:16:56 GMT  
		Size: 2.8 MB (2765419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab08f3692f0fbb76f7d75f29febe952d010beb609bd58fc3911e02a701a5e88`  
		Last Modified: Sat, 28 May 2022 10:17:03 GMT  
		Size: 38.0 MB (38048375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0417a288a09188a92b315ac93d8dc23f50045868021a04dda5f2695cfad06a8`  
		Last Modified: Sat, 28 May 2022 10:16:56 GMT  
		Size: 3.2 MB (3166834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0353f8b85b6dee9f5c872bc6462a8378b4da9536a48916dabd03333d6aa5c48`  
		Last Modified: Sun, 29 May 2022 04:34:32 GMT  
		Size: 3.2 MB (3238493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.9-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:dd017fba4874314f1bca0179840b2ece881c8797e7bf2f30c2f868d1d1e4d2a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69670517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905ff21509824c29f802fd46e4fa1cd64311bbb799c870529d95efb952a7ccee`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:19:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 07:19:14 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 07:19:15 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 07:19:16 GMT
ENV PYPY_VERSION=7.3.9
# Sat, 28 May 2022 07:19:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-linux64.tar.bz2'; 			sha256='46818cb3d74b96b34787548343d266e2562b531ddbaf330383ba930ff1930ed5'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-aarch64.tar.bz2'; 			sha256='2e1ae193d98bc51439642a7618d521ea019f45b8fb226940f7e334c548d2b4b9'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-linux32.tar.bz2'; 			sha256='0de4b9501cf28524cdedcff5052deee9ea4630176a512bdc408edfa30914bae7'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-s390x.tar.bz2'; 			sha256='774dca83bcb4403fb99b3d155e7bd572ef8c52b9fe87a657109f64e75ad71732'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 28 May 2022 07:19:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Sat, 28 May 2022 07:19:52 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Sat, 28 May 2022 07:20:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 May 2022 07:20:15 GMT
CMD ["pypy3"]
# Sun, 29 May 2022 00:09:32 GMT
ENV HY_VERSION=1.0a4
# Sun, 29 May 2022 00:09:32 GMT
ENV HYRULE_VERSION=0.1
# Sun, 29 May 2022 00:09:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sun, 29 May 2022 00:09:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce05c34f1947a9b7dfea84ea400dfa3c309f10ef6b5452c1e7cee5c8f7b7404`  
		Last Modified: Sat, 28 May 2022 07:31:45 GMT  
		Size: 2.6 MB (2634726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bec87a107531bdc24747606d195ad1dd9dadb07a194bcc3f71f5a4e13b7921e`  
		Last Modified: Sat, 28 May 2022 07:31:51 GMT  
		Size: 34.9 MB (34933721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c4d2a170f723cb03600fe8a6f4fec9ed521c0860714623204fa73a5b1584a`  
		Last Modified: Sat, 28 May 2022 07:31:45 GMT  
		Size: 3.0 MB (2951104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0518ba6ed47eeeb79b78f11f3568fa5ebc4b9b3ee0247a5c3ed59045cdfd8ab2`  
		Last Modified: Sun, 29 May 2022 00:15:19 GMT  
		Size: 3.2 MB (3236933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.9-buster` - linux; 386

```console
$ docker pull hylang@sha256:ceec082542434ae098381892cd5caad712417a02de460e9f7c52e27a63ad8c7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77324355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495b7446d538751a71d3aca4708a89ae90e61adcdc56441f0224150c7b7ae03c`
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
# Thu, 23 Jun 2022 13:54:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-linux64.tar.bz2'; 			sha256='46818cb3d74b96b34787548343d266e2562b531ddbaf330383ba930ff1930ed5'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-aarch64.tar.bz2'; 			sha256='2e1ae193d98bc51439642a7618d521ea019f45b8fb226940f7e334c548d2b4b9'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-linux32.tar.bz2'; 			sha256='0de4b9501cf28524cdedcff5052deee9ea4630176a512bdc408edfa30914bae7'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-s390x.tar.bz2'; 			sha256='774dca83bcb4403fb99b3d155e7bd572ef8c52b9fe87a657109f64e75ad71732'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 23 Jun 2022 13:54:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 23 Jun 2022 13:54:07 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 23 Jun 2022 13:54:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Jun 2022 13:54:22 GMT
CMD ["pypy3"]
# Thu, 23 Jun 2022 19:37:28 GMT
ENV HY_VERSION=0.24.0
# Thu, 23 Jun 2022 19:37:28 GMT
ENV HYRULE_VERSION=0.2
# Thu, 23 Jun 2022 19:38:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 23 Jun 2022 19:38:05 GMT
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
	-	`sha256:523114677d0f99f81287d2bfbfa631375df3d0ce8ffa51cd74502b2d154e70c6`  
		Last Modified: Thu, 23 Jun 2022 14:09:47 GMT  
		Size: 39.8 MB (39827551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e980b42c4fad5e58778fae73e771f54e42839f4ce59afa09f65cb058652470c9`  
		Last Modified: Thu, 23 Jun 2022 14:09:41 GMT  
		Size: 3.0 MB (2951149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e67328bafe10d299b2ab5bf2ec98593de421f21c1e56a8c95a6e6d9c2390173`  
		Last Modified: Thu, 23 Jun 2022 19:51:34 GMT  
		Size: 4.0 MB (3968340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.9-buster` - linux; s390x

```console
$ docker pull hylang@sha256:56d22e179974091caf49145f88423d1af3d308e908a0b686e77cf686a66d2486
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70987472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f892bc256eb08af86a41a71b57e84a9e289b7d02f6a4fa8676290ae6a017f1`
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
# Thu, 23 Jun 2022 09:21:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-linux64.tar.bz2'; 			sha256='46818cb3d74b96b34787548343d266e2562b531ddbaf330383ba930ff1930ed5'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-aarch64.tar.bz2'; 			sha256='2e1ae193d98bc51439642a7618d521ea019f45b8fb226940f7e334c548d2b4b9'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-linux32.tar.bz2'; 			sha256='0de4b9501cf28524cdedcff5052deee9ea4630176a512bdc408edfa30914bae7'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.9-s390x.tar.bz2'; 			sha256='774dca83bcb4403fb99b3d155e7bd572ef8c52b9fe87a657109f64e75ad71732'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 23 Jun 2022 09:21:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 23 Jun 2022 09:21:39 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 23 Jun 2022 09:21:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Jun 2022 09:21:52 GMT
CMD ["pypy3"]
# Thu, 23 Jun 2022 22:03:12 GMT
ENV HY_VERSION=0.24.0
# Thu, 23 Jun 2022 22:03:13 GMT
ENV HYRULE_VERSION=0.2
# Thu, 23 Jun 2022 22:03:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 23 Jun 2022 22:03:44 GMT
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
	-	`sha256:07c4dad743bb4d419a5df5903b969ae3c8107d5efb2b2de392fbdced5df50f18`  
		Last Modified: Thu, 23 Jun 2022 09:29:57 GMT  
		Size: 35.6 MB (35636329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cbef538c2ca0eee0fff7c1564b30f045c9ff3585df752dde022b7866c7ec74`  
		Last Modified: Thu, 23 Jun 2022 09:29:51 GMT  
		Size: 3.2 MB (3166666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0420ad8b4c55a2b1658fa8d01021ffc3c7717d6b89875753713fe66d306837b`  
		Last Modified: Thu, 23 Jun 2022 22:12:29 GMT  
		Size: 4.0 MB (3968290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
