## `pypy:3-7-slim`

```console
$ docker pull pypy@sha256:e4a842f7a8e8df793d08c8ffc47b9ea75c9ba7aabe0ae91a63b4744242afd1ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-7-slim` - linux; amd64

```console
$ docker pull pypy@sha256:63a9bf3705bcfa15f913dce6d34bf6a978547afa4665445c0490b6edaabd60a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71823606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8334261fba06307d714249dcbd8264fefbca2beb0f1db3e8009ccc704d56c55d`
-	Default Command: `["pypy3"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37584419173c47a2b5771c7fea9113c7b2bb6f5b91b48013526fb07956c31d4d`  
		Last Modified: Fri, 05 Jan 2024 18:54:26 GMT  
		Size: 863.2 KB (863186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a588bcb7efeb736716a44b0695d04d366ae37b75979f7503048dfa0b0d231f8b`  
		Last Modified: Fri, 05 Jan 2024 18:54:26 GMT  
		Size: 36.2 MB (36240606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0230ee44a086f5419baeaf3a08e9cedbc41dfb27c6b679f7e6ae736d0619a808`  
		Last Modified: Fri, 05 Jan 2024 18:54:26 GMT  
		Size: 3.3 MB (3301941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:dfa0d0a66605c4b42ffa8cbc4ee3852ff42e5c48043077e876b0a882eb7396b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3258952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e136b32b4d467269229b39325bb1e8e9951710eab0bcf75ee329fc1a545682b`

```dockerfile
```

-	Layers:
	-	`sha256:7eeee886362cf3f1d734b04868ea9c67a7d6b12c014402686a53ab9362c135f6`  
		Last Modified: Fri, 05 Jan 2024 18:54:26 GMT  
		Size: 3.2 MB (3230318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391ef9ee389de1a9a53af5fcc541c9fa4421d29252eba3e87b4e72a6103521b1`  
		Last Modified: Fri, 05 Jan 2024 18:54:26 GMT  
		Size: 28.6 KB (28634 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:8edcce9583f32ab86c1879b551a76f8d35125a95c7f28ef9dbe8f6855d49c5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68077409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6068cf0bae9d05e120fa289323669b09f6ce2a2c82a85595861a6b61d1ea7af`
-	Default Command: `["pypy3"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420960ab036904ce670019905624e65cd0a2badab83d0a7c934820a784f459c9`  
		Last Modified: Fri, 05 Jan 2024 19:28:29 GMT  
		Size: 850.6 KB (850551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7212fe75cc995400db83106e053c1da8b82ec6cfdc488c7af1eef6a82e934d`  
		Last Modified: Fri, 05 Jan 2024 19:28:30 GMT  
		Size: 33.9 MB (33861079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb9251b8fdbc9a8a02af15bb995c3d257b9b6a1d2b3dd4ef0b57a1f482fe2c5`  
		Last Modified: Fri, 05 Jan 2024 19:28:29 GMT  
		Size: 3.3 MB (3301727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:70fff4237fdc6ce71d9140f87690821b8b30e809e584ac0ea18598ecb466c2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3236766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b56e82cb36a08df8569dd434e51db7a3668632af206ee686f127c08bd1bf7e0`

```dockerfile
```

-	Layers:
	-	`sha256:979aed1476a177c2406dd33716e14e398e0d47e089382db68fc25ed210d73e91`  
		Last Modified: Fri, 05 Jan 2024 19:28:29 GMT  
		Size: 3.2 MB (3208262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986de435962b8c10b39d33ed6265544d73e65bf567cb624b6d09e15d5114679f`  
		Last Modified: Fri, 05 Jan 2024 19:28:28 GMT  
		Size: 28.5 KB (28504 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim` - linux; 386

```console
$ docker pull pypy@sha256:d16edf8178a4f10e692e9c472ce4874c8e675e34ae89187db3c21cbe59ba6d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71033754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166b3b28620b91946759687daa534ba8f1e5c5517e3d43e4b3b76242e8b7046e`
-	Default Command: `["pypy3"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:30 GMT
ADD file:e9c344f1bffba57e46b30e3c70e4247dcf2e9d3e0484b2768f83ffd789bf3686 in / 
# Tue, 19 Dec 2023 01:39:30 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:e5808d881ded1b1deb8675903e6776c5a725d22c8a5c1061a96c74338f07591f`  
		Last Modified: Tue, 19 Dec 2023 01:44:31 GMT  
		Size: 32.4 MB (32402688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424a65d211c0817ca064c36924959c5e921715f9409eab720c89f775a00f8073`  
		Last Modified: Fri, 05 Jan 2024 18:54:36 GMT  
		Size: 875.5 KB (875480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebef074704be88ae98c5194eae8c3079fac3b4e72242b0f66a78262225438b5`  
		Last Modified: Fri, 05 Jan 2024 18:54:37 GMT  
		Size: 34.5 MB (34453919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b02651853e3a2d2f5127d1cdd22c08f235ee80a619758a6415c11ffe544b9f`  
		Last Modified: Fri, 05 Jan 2024 18:54:37 GMT  
		Size: 3.3 MB (3301667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:a0f01cffe3aced2f58f3cf9e167b2c7d00d8c9ee05a8d8ab588a2888dac0f833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129adaf1322ec5d3f3d0332ff2a9aeca89b96535cb1c67c655d7a4f6e1978989`

```dockerfile
```

-	Layers:
	-	`sha256:6fd13367a81f93d521e115c8082e523d6454b93603369ebb2d153c09c9b363dd`  
		Last Modified: Fri, 05 Jan 2024 18:54:36 GMT  
		Size: 3.2 MB (3233564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e02d6bdaf3e18e231fe94af0498dffdcb2f20d82f90e0823429def7c23ac74`  
		Last Modified: Fri, 05 Jan 2024 18:54:36 GMT  
		Size: 28.5 KB (28531 bytes)  
		MIME: application/vnd.in-toto+json
