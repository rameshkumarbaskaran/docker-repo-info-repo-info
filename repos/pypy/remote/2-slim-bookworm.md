## `pypy:2-slim-bookworm`

```console
$ docker pull pypy@sha256:15b08e82d1e5094b14771fa44e0894127dc8aa421ba75bb9c5e5fcabffe3149b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:c1b8f1ad466007bd838d56223c3e185e11d718842aee0ff59d1c5b73600b772a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65660803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b647bde56080d0e5e87f7840b64771e4dd0053ae0aa23a5ab1d018ae091203`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 19:34:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:34:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 19:34:26 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:34:26 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 21 Nov 2023 19:39:55 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Nov 2023 19:39:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Nov 2023 19:39:55 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Nov 2023 19:40:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Nov 2023 19:40:03 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00593ab81db042d0fd8f9d341746ec14d4b618434584147ccbcf33d98041b26c`  
		Last Modified: Tue, 21 Nov 2023 19:42:11 GMT  
		Size: 3.5 MB (3494711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85ba38c5935d0b59c46ff75f5348c4463b34c2f802d798ff68c767ea5a8730d`  
		Last Modified: Tue, 21 Nov 2023 19:46:31 GMT  
		Size: 30.9 MB (30856759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e821bd40ca4d014daa983fb6dfcee0571e61e6393e2a0c3ef7875514a8a316a`  
		Last Modified: Tue, 21 Nov 2023 19:46:26 GMT  
		Size: 2.2 MB (2159425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:e87784d0765d7b929462408b02a63945099f1752cf048b2a838360c131b9b618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63496177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d494cbba96833436ab2f945e632f743baa1cb2374cf827e03d895c72a0067fbd`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 09:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 09:34:30 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:34:30 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 09:34:30 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 19 Dec 2023 09:37:58 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 19 Dec 2023 09:37:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 19 Dec 2023 09:37:58 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 19 Dec 2023 09:38:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 19 Dec 2023 09:38:06 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9071966d3c5e7a69be8a39f3f1be771af1a624a107b796965302c315cb24729f`  
		Last Modified: Tue, 19 Dec 2023 09:39:26 GMT  
		Size: 3.3 MB (3314321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf40e05f01072382fad9038c1263dacfff3cffff50adc4ff64dfdee632182d4`  
		Last Modified: Tue, 19 Dec 2023 09:41:23 GMT  
		Size: 28.9 MB (28866539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8973baccf073e8d007207d07c67903bf4dedba9928c01495b32120b01199caf7`  
		Last Modified: Tue, 19 Dec 2023 09:41:20 GMT  
		Size: 2.2 MB (2158048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:4d6374f7e38aaae3d14d60b5152ad1238270511f8e71908465f52b96aa84f4db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62774607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9283c2a74c456d59e6d8df5993ab9ba5f61be0a25acab1c0315f6afbe62ad026`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 21 Nov 2023 04:39:53 GMT
ADD file:930e1b9d85b6927c4d3046f7c75de2f3bfc6ec29100c314d0ab2b780ea30e962 in / 
# Tue, 21 Nov 2023 04:39:53 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 15:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 15:44:55 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 15:44:55 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 15:44:55 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 21 Nov 2023 15:52:34 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 21 Nov 2023 15:52:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 21 Nov 2023 15:52:34 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 21 Nov 2023 15:52:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Nov 2023 15:52:46 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:c0734eabce8885d8904dbd11b77aa97c2d2b04bc8e2af9e89d47c4bda590dd8e`  
		Last Modified: Tue, 21 Nov 2023 04:44:34 GMT  
		Size: 30.2 MB (30164109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94e79b6f93c3a648c31a4df1b6fdc61838eb53ddb7cfb80b5f411a22847870b`  
		Last Modified: Tue, 21 Nov 2023 15:55:14 GMT  
		Size: 3.5 MB (3499470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03cb6c84dd943727912e74f6eaf26be7a708eb47e6b0fb60b716d7c9a97f793`  
		Last Modified: Tue, 21 Nov 2023 15:59:12 GMT  
		Size: 27.0 MB (26951619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f581f7738a465c22ff0a460be9c5a798aa59c12b6a64592f845a8e00cf3a22`  
		Last Modified: Tue, 21 Nov 2023 15:59:05 GMT  
		Size: 2.2 MB (2159409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
