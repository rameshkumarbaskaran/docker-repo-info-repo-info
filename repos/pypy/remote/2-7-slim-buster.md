## `pypy:2-7-slim-buster`

```console
$ docker pull pypy@sha256:9dc86d27f92b08999ccd87780ec0e7f924c5206ab433930084e3fe05722c8c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-7-slim-buster` - linux; amd64

```console
$ docker pull pypy@sha256:68fcde3b6c38b89b17419607753a8f22198615e8fc63a81619d9d24441e395c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63204602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bc29eb61972d4894e857aaa3506149d6edc3b53c18d71f15df9b37416cc571`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:25 GMT
ADD file:e614539607055bdbde0cc1a94ef9783fe3627c8553ef1b21071ecb5c27ea27e4 in / 
# Wed, 12 Apr 2023 00:20:26 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 06:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 06:01:47 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 06:01:47 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 06:01:47 GMT
ENV PYPY_VERSION=7.3.11
# Wed, 12 Apr 2023 06:04:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux64.tar.bz2'; 			sha256='ba8ed958a905c0735a4cfff2875c25089954dc020e087d982b0ffa5b9da316cd'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-aarch64.tar.bz2'; 			sha256='ea924da1defe9325ef760e288b04f984614e405580f5321eb6a5c8f539bd415a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux32.tar.bz2'; 			sha256='30fd245fab7068c96a75b9ff1323ac55174c64fc8c4751cceb4b7a9bedc1851e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-s390x.tar.bz2'; 			sha256='8fe9481c473178e53266983678684a70fe0c42bafc95f1807bf3ef28770316d4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 12 Apr 2023 06:05:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 Apr 2023 06:05:00 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 Apr 2023 06:05:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 12 Apr 2023 06:05:09 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:9fbefa3370776b7ec7633cf07efc14cc24e0c0cd53893ad0e7e3f44ffdc1bedb`  
		Last Modified: Wed, 12 Apr 2023 00:24:22 GMT  
		Size: 27.1 MB (27138920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6e180a0db428c8363aed838b89d2c0f1da8073db9859e54c1eea436fe1b8bb`  
		Last Modified: Wed, 12 Apr 2023 06:06:50 GMT  
		Size: 2.8 MB (2770909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c45fcae8cb1852c42d7cb74823045e75b1aa32d51f3b790ed91505c8aee3bc8`  
		Last Modified: Wed, 12 Apr 2023 06:08:49 GMT  
		Size: 31.1 MB (31125278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423408154ebb6d11d9f66a2f21c6ae650bac9aac30ca20c6b1e9cce09e615731`  
		Last Modified: Wed, 12 Apr 2023 06:08:45 GMT  
		Size: 2.2 MB (2169495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-buster` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:579c95fcf21dbf590d0e0a4b0df78044e9b954f0010a3c13556cc39ad1f2752f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59883214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ce6512d34e71d039cff0f1588851e64966f097fd202717201117540e2ce3a4`
-	Default Command: `["pypy"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:23 GMT
ADD file:44e400cc6a1bc5df5a57bda478c9accf9b58950fa2fd069cc7620128fe786770 in / 
# Thu, 23 Mar 2023 00:45:23 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:03:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:03:43 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 06:03:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 06:03:44 GMT
ENV PYPY_VERSION=7.3.11
# Thu, 23 Mar 2023 06:06:24 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux64.tar.bz2'; 			sha256='ba8ed958a905c0735a4cfff2875c25089954dc020e087d982b0ffa5b9da316cd'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-aarch64.tar.bz2'; 			sha256='ea924da1defe9325ef760e288b04f984614e405580f5321eb6a5c8f539bd415a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux32.tar.bz2'; 			sha256='30fd245fab7068c96a75b9ff1323ac55174c64fc8c4751cceb4b7a9bedc1851e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-s390x.tar.bz2'; 			sha256='8fe9481c473178e53266983678684a70fe0c42bafc95f1807bf3ef28770316d4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 23 Mar 2023 06:06:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 23 Mar 2023 06:06:24 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 23 Mar 2023 06:06:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Mar 2023 06:06:33 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:cfe0f778e53ce031ef449bc02975a07f2568716dea807ed2f390d352c0001972`  
		Last Modified: Thu, 23 Mar 2023 00:48:45 GMT  
		Size: 25.9 MB (25922660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0d50ef88e56b84543df38964895f37a73d560769988f3b2b30cdaa491dbda5`  
		Last Modified: Thu, 23 Mar 2023 06:08:00 GMT  
		Size: 2.6 MB (2637273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01df074feec1bf0ba2f64bf48aa4b2c38e76398670e041b876b7a76aa215b3df`  
		Last Modified: Thu, 23 Mar 2023 06:09:45 GMT  
		Size: 29.2 MB (29153883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c07622ba3f21bef1cd0ae145ff6968f407632378f06aabbdbe5e413090b7c3`  
		Last Modified: Thu, 23 Mar 2023 06:09:42 GMT  
		Size: 2.2 MB (2169398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-buster` - linux; 386

```console
$ docker pull pypy@sha256:7221e869e8270820ce36ee004ce2a41050f7ed9e19b8e3a006973ff2dc837eea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59950371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c24317c923176b0bba68b8b9e1dd1cc129487f8e9bed6c390e918de82bc2699`
-	Default Command: `["pypy"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:40 GMT
ADD file:5743625b778ab9036f4eae3e44da6b59db355d7d6d7b8f42fbb71f2b8c428dd7 in / 
# Thu, 23 Mar 2023 00:39:40 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:29:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 19:29:54 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 19:29:54 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 19:29:54 GMT
ENV PYPY_VERSION=7.3.11
# Thu, 23 Mar 2023 19:35:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux64.tar.bz2'; 			sha256='ba8ed958a905c0735a4cfff2875c25089954dc020e087d982b0ffa5b9da316cd'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-aarch64.tar.bz2'; 			sha256='ea924da1defe9325ef760e288b04f984614e405580f5321eb6a5c8f539bd415a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux32.tar.bz2'; 			sha256='30fd245fab7068c96a75b9ff1323ac55174c64fc8c4751cceb4b7a9bedc1851e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-s390x.tar.bz2'; 			sha256='8fe9481c473178e53266983678684a70fe0c42bafc95f1807bf3ef28770316d4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 23 Mar 2023 19:35:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 23 Mar 2023 19:35:06 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 23 Mar 2023 19:35:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Mar 2023 19:35:16 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:0a3d55947c3a2af51034409d456cfd83f620450381a4b036d86b0db1b8b0aaf8`  
		Last Modified: Thu, 23 Mar 2023 00:43:56 GMT  
		Size: 27.8 MB (27798660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dd89d89ccfd7a7e554caf325dc2bc0e539cadee2c9acf708295577014862fd`  
		Last Modified: Thu, 23 Mar 2023 19:37:43 GMT  
		Size: 2.8 MB (2783732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7b4cb89e34148518c521d3340a380ec28b7b46b7ad389a54ccc55cbd19afeb`  
		Last Modified: Thu, 23 Mar 2023 19:41:10 GMT  
		Size: 27.2 MB (27198527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def854340895b791e6f7c8c62925169a36c92b1b4d1fafe1b007a18de6c023a0`  
		Last Modified: Thu, 23 Mar 2023 19:41:04 GMT  
		Size: 2.2 MB (2169452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
