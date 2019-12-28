## `python:3-buster`

```console
$ docker pull python@sha256:fd09b750778e2cd7818ca8a067dd65e5a09d7d2a7d1f420c8b7b3744b8b26358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `python:3-buster` - linux; amd64

```console
$ docker pull python@sha256:e4edf0e471dcfef26d847f519d1bc37f3dc7b9dfe5d9d61b14586295fbdb71cd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349248822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038a832804a024017b7a8ce216415217abe8da628e659af37490793b8aeae95a`
-	Default Command: `["python3"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:08 GMT
ADD file:d6d0bdf8cb07a7a0dc32e9df50ac80ca1a524c3fa48136892ded195061f2194c in / 
# Sat, 28 Dec 2019 04:21:09 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:47:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:47:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:47:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:48:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:13:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 05:13:53 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 05:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:14:00 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 28 Dec 2019 05:23:32 GMT
ENV PYTHON_VERSION=3.8.1
# Sat, 28 Dec 2019 05:32:16 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Sat, 28 Dec 2019 05:32:17 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 28 Dec 2019 05:32:18 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 05:32:18 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 05:32:19 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 05:32:25 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 05:32:25 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:8f0fdd3eaac017684c880d836abdaf02f9db7ac8ecca970356482e3d8e315650`  
		Last Modified: Sat, 28 Dec 2019 04:25:39 GMT  
		Size: 50.4 MB (50379720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d918eaefd9de8a1595f56900fdb8ab65a03d64b1da1078da7c0b0bf6f7552a14`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 7.8 MB (7811715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf3e3107f525b7dea5b3cdfd15f62666066202105a0aaddbab2a02aefad1f7`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 10.0 MB (9996202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27622921edb2aae9e0cb64f71a81b4a7cfef8f6a6c766514a018815834ba4e14`  
		Last Modified: Sat, 28 Dec 2019 05:02:00 GMT  
		Size: 51.8 MB (51790562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa0aa1ae2c54d0de4b6ad0ee4d9f795c93368ae7d87801784c1f8ae624ac33`  
		Last Modified: Sat, 28 Dec 2019 05:02:36 GMT  
		Size: 192.0 MB (192044395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6840af9e7046c642925fe6522155e1a165a456a6c470ba573599e2a1807f5f`  
		Last Modified: Sat, 28 Dec 2019 08:17:59 GMT  
		Size: 5.8 MB (5792130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f900120cf5daab5e2f955420f6174a83fff7f9caf3a782751154d4bf2ac9df`  
		Last Modified: Sat, 28 Dec 2019 08:18:24 GMT  
		Size: 29.6 MB (29563452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644b4ceca849574793555383a667efb248bc82714cd5df59ae10b8cedd052958`  
		Last Modified: Sat, 28 Dec 2019 08:18:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f0ac11639addb41cb07beefd2a7de3861d1a09ccf5d3dbf4151d392728efbe`  
		Last Modified: Sat, 28 Dec 2019 08:18:16 GMT  
		Size: 1.9 MB (1870413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-buster` - linux; arm variant v5

```console
$ docker pull python@sha256:a4f05f133a484f7a415a875fb94c26d425c44d01b1c4eff1c1ef48971fcee1a4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320189593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c875ffa43a7cc33beb59b65c6eb335dbab10e36f927a136e3421493b23e1fcaf`
-	Default Command: `["python3"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:30 GMT
ADD file:dd72fb82d87c4594d064818aab5020766a85e76bd85305fea5eaf6dfd20a97fb in / 
# Sat, 28 Dec 2019 04:49:32 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:23:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:23:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:24:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:29:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:12:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:12:59 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:13:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:13:19 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 28 Dec 2019 08:25:08 GMT
ENV PYTHON_VERSION=3.8.1
# Sat, 28 Dec 2019 08:36:32 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Sat, 28 Dec 2019 08:36:36 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 28 Dec 2019 08:36:37 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 08:36:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 08:36:40 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 08:36:53 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 08:36:54 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3bf27a5276936429fef3702e21a1cfcfde88ef96196749cdf3e1b7576af5af38`  
		Last Modified: Sat, 28 Dec 2019 04:56:08 GMT  
		Size: 48.1 MB (48092858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bbc9740afdaf5d761dc8d69c82dc5e7fc1f1bcdd19849bd2c6ad632959b19f`  
		Last Modified: Sat, 28 Dec 2019 05:50:24 GMT  
		Size: 7.4 MB (7358639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac01bbcc7211cc192a2700f12cd017f4d1848837cb4a6984c74d2f4786d14f`  
		Last Modified: Sat, 28 Dec 2019 05:50:24 GMT  
		Size: 9.7 MB (9686940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555d9ff28c9f638fbe6d7a4498c2c1a3ef46b1fb710a2ac820f984ba88483c9a`  
		Last Modified: Sat, 28 Dec 2019 05:50:54 GMT  
		Size: 49.5 MB (49532533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c7d57b96ac8f4ec7ce82e0428a4fb211136d7a0efb4de3afc722adcb81bf7`  
		Last Modified: Sat, 28 Dec 2019 05:51:52 GMT  
		Size: 171.0 MB (171003316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39aa7ee6ee2abb5c15e1c730b1d92d39bb4643320a6109ce4160fd3009b883`  
		Last Modified: Sat, 28 Dec 2019 11:40:33 GMT  
		Size: 5.5 MB (5490267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2772738fb21cd53e566f0a8f1e85d935f21decba77361aa6af5d3a54d859702`  
		Last Modified: Sat, 28 Dec 2019 11:41:00 GMT  
		Size: 27.2 MB (27154086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c3fdff07155158c7d0cb0de05226aa5a71f691b5df5cb289201e6b5a442ab6`  
		Last Modified: Sat, 28 Dec 2019 11:40:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06adc07a71b9b7d807d8b8b09ba0f05fc7dd1ae7ed096ffe2077616a95dbd6d`  
		Last Modified: Sat, 28 Dec 2019 11:40:52 GMT  
		Size: 1.9 MB (1870720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-buster` - linux; arm variant v7

```console
$ docker pull python@sha256:4545d931b33bf10139de81fd4a8404b087b52784aae37edb70f27fd2a7da87b0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311676537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a3158323dd87af40f5163d1f75ee683a64b6c9dd34f1bf3e03f9c96f43809a`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:47:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 00:47:19 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 00:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:47:35 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 20 Dec 2019 22:02:29 GMT
ENV PYTHON_VERSION=3.8.1
# Fri, 20 Dec 2019 22:14:11 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 20 Dec 2019 22:14:14 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 20 Dec 2019 22:14:15 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 20 Dec 2019 22:14:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 20 Dec 2019 22:14:17 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 20 Dec 2019 22:14:28 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 20 Dec 2019 22:14:29 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69590e0d6b359167e2d103e39617e28e2d5da74e7327194e72a2a0b4828107`  
		Last Modified: Fri, 22 Nov 2019 23:31:41 GMT  
		Size: 168.2 MB (168243234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839c43046833dc87303eef175734beaf61a985a5e570bc0f920fa03a201f45c2`  
		Last Modified: Sat, 23 Nov 2019 04:21:53 GMT  
		Size: 5.2 MB (5196232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76a4d03b287bc8a1889f3de258fad9ffb296c8ce953623d96b1527697b2bd90`  
		Last Modified: Sat, 21 Dec 2019 03:03:55 GMT  
		Size: 26.8 MB (26766333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff7aa0fdbd804fd775206ba993424b6d20bab48cbafe16d620d555769983ace`  
		Last Modified: Sat, 21 Dec 2019 03:03:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f11030c81e13633ae95098ae6d7260976c61d85c440d47db2ff82e5d2cd0424`  
		Last Modified: Sat, 21 Dec 2019 03:03:46 GMT  
		Size: 1.9 MB (1870689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-buster` - linux; arm64 variant v8

```console
$ docker pull python@sha256:a32098940b088a477518a0ea7174d32c69c7011cef2dd2862cd92319d8c2ac20
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338862243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78fa2ffaa4fa39ae6428c74f7bdec7cc1d9599ae555505da7dd040dcf3c96d2`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:25 GMT
ADD file:9f9eea5881797502bfab12007544d80607c25d2748eeeba94c931d9e83b82ca9 in / 
# Fri, 22 Nov 2019 13:41:29 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 20:12:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:12:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 20:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 20:16:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 08:03:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 08:03:46 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 08:04:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 08:05:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 20 Dec 2019 20:58:45 GMT
ENV PYTHON_VERSION=3.8.1
# Fri, 20 Dec 2019 21:08:24 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 20 Dec 2019 21:08:27 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 20 Dec 2019 21:08:27 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 20 Dec 2019 21:08:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 20 Dec 2019 21:08:29 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 20 Dec 2019 21:08:41 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 20 Dec 2019 21:08:42 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:af4800279257e4522b03ad0d6d0aa937a2761fe0e54758127ec7fd14fc1715d0`  
		Last Modified: Fri, 22 Nov 2019 13:49:29 GMT  
		Size: 49.2 MB (49172037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae2ec46cd5af1ce11d246b5b7bea023991c857cbf131fc2b4f80a42c7abb5c`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 7.7 MB (7680704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8718b9412e0a23370b0877b007da88210a2408dd572782050dcdd233e1f19e`  
		Last Modified: Fri, 22 Nov 2019 20:27:44 GMT  
		Size: 10.0 MB (9983756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908f8b447250af91341f8f3a1741b2c8d6432714e885746c4afd227eed1be7b`  
		Last Modified: Fri, 22 Nov 2019 20:28:07 GMT  
		Size: 52.1 MB (52079377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0fac9e6c6a4a40a22bab46b85791dc7a34b25219d893a5c2690273437194e`  
		Last Modified: Fri, 22 Nov 2019 20:29:00 GMT  
		Size: 183.6 MB (183567555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1da11f97bb2014cee3adefc29d8eeab67c59e39e9f93239eabdc80885fb1e9`  
		Last Modified: Sat, 23 Nov 2019 11:55:11 GMT  
		Size: 5.9 MB (5909459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b05002aa816bb155ab5a4b2b9c6007d19be1df771cb2f1a1adf442dcfe0d35`  
		Last Modified: Sat, 21 Dec 2019 01:40:34 GMT  
		Size: 28.6 MB (28598397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584c495f4e0f339efac09f622b7480490af8c4030bc22c15d42b4e220e7c67`  
		Last Modified: Sat, 21 Dec 2019 01:40:23 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ee9fba577341055f78d59b2ae17195224ab6aec38e50a23d786443fecd460f`  
		Last Modified: Sat, 21 Dec 2019 01:40:23 GMT  
		Size: 1.9 MB (1870724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-buster` - linux; 386

```console
$ docker pull python@sha256:5315331a403d82fd5128739bf3e0ff8bd6e29012af466473a7523d959679ad01
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357172815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668fece73977639b69a759f40c460d282f05db026a31ff1caae06dd12019c3e`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 22 Nov 2019 16:49:50 GMT
ADD file:637dd256233b11c890b47c64e1116a873db07060c542d65ed8c5e1f1692b93c5 in / 
# Fri, 22 Nov 2019 16:49:51 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:40:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:41:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 08:48:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 08:48:35 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 08:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 08:48:49 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 21 Dec 2019 00:49:35 GMT
ENV PYTHON_VERSION=3.8.1
# Sat, 21 Dec 2019 01:00:38 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Sat, 21 Dec 2019 01:00:39 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 21 Dec 2019 01:00:39 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 21 Dec 2019 01:00:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 21 Dec 2019 01:00:39 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 21 Dec 2019 01:00:45 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 21 Dec 2019 01:00:45 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d34dc3661e80ce84b97704f402da563467559a0af488425969a76a38a8761a63`  
		Last Modified: Fri, 22 Nov 2019 16:58:09 GMT  
		Size: 51.1 MB (51141757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a002a28e7af0825b2efeca76651a2e3e98ba4d0ee10eed07b3d1495cc86a50`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 8.0 MB (7981294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521d3b916711e34309354077f7f65c55009c0845fcce1b34ec7de57e3d97435`  
		Last Modified: Sat, 23 Nov 2019 01:01:39 GMT  
		Size: 10.3 MB (10338436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a5cecf8b6e164d82cc59bf21e9316e3e5e98d21dab1a969d690c117d83ae2`  
		Last Modified: Sat, 23 Nov 2019 01:02:01 GMT  
		Size: 53.4 MB (53358180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04d7f177748111a9f0984420d86be7db6e1583a9a71bf27b890d0034907e8c`  
		Last Modified: Sat, 23 Nov 2019 01:03:05 GMT  
		Size: 198.6 MB (198593521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234bfef9f740aa5b0b1e4071705bf47a9ff727aea2a8ae5547f71b75addfe6e7`  
		Last Modified: Sat, 23 Nov 2019 12:09:33 GMT  
		Size: 6.1 MB (6139184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356538a3147bc7af108166adcb994cba19d85b73cb10a6b32ffb33574892c2c9`  
		Last Modified: Sat, 21 Dec 2019 04:50:49 GMT  
		Size: 27.7 MB (27749667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e570b4b038b8046797ea0f815f46385f1472b1613b765ac7c0e916e627525fda`  
		Last Modified: Sat, 21 Dec 2019 04:50:42 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef11f219517a6580244ef703687c8daf35c941990e44a2a6085e9457c06da25`  
		Last Modified: Sat, 21 Dec 2019 04:50:42 GMT  
		Size: 1.9 MB (1870541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-buster` - linux; ppc64le

```console
$ docker pull python@sha256:2d3ecaed338f9596950406dd6a9d3e82c3e1c3c95a5be998d871c27794b6109e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.0 MB (372041339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1690ceb38a7429546c1cc7b835ff98209859467044e949a9bdfb94bc3ef394f9`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:52 GMT
ADD file:7ea1f6679a4179527d68a59a76ad469bf07b8ce30b1288b4b6437bba9982b896 in / 
# Fri, 22 Nov 2019 14:54:56 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:01:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:01:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:03:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:08:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 08:53:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 08:53:06 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 08:53:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 08:53:47 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 20 Dec 2019 23:04:16 GMT
ENV PYTHON_VERSION=3.8.1
# Fri, 20 Dec 2019 23:13:02 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 20 Dec 2019 23:13:08 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 20 Dec 2019 23:13:10 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 20 Dec 2019 23:13:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 20 Dec 2019 23:13:16 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 20 Dec 2019 23:13:29 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 20 Dec 2019 23:13:31 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:127c50d67aec36464937a4593797286304a844c7b8ca8263bbbdd8967229cf5a`  
		Last Modified: Fri, 22 Nov 2019 15:03:30 GMT  
		Size: 54.1 MB (54132225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f59bd6a64d30e2f2a4a62e9589199153ddb61c2f77cc445945b67cd56d87db`  
		Last Modified: Sat, 23 Nov 2019 00:26:54 GMT  
		Size: 8.3 MB (8252166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8328c28b5029be40abe47ebb260b0dab06a48ca9afdbd9a04b1d91fe6480f`  
		Last Modified: Sat, 23 Nov 2019 00:26:53 GMT  
		Size: 10.7 MB (10727041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a63bd0de74997185aa941953104c26c47babd2334ce4ebc507eefbd72b724`  
		Last Modified: Sat, 23 Nov 2019 00:27:38 GMT  
		Size: 57.4 MB (57400619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7f7cbd4299e83d6173d1cd36c3636a5dc569334823a99166f1a3eeea2e8302`  
		Last Modified: Sat, 23 Nov 2019 00:29:24 GMT  
		Size: 202.8 MB (202845331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdab507a591b99fa7825e6f3dcecb59e1a130a2c59e2105d2a9604b2c7ab178`  
		Last Modified: Sat, 23 Nov 2019 12:13:48 GMT  
		Size: 6.5 MB (6527543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af559db68a2195dc83cba2d8e6d6dfa7fef388ae362176d1f5987318c5a6773`  
		Last Modified: Sat, 21 Dec 2019 03:57:36 GMT  
		Size: 30.3 MB (30285502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4919716d0d03997e46aedcdb32254ed2449e100d815722aa2479d1ebd7cf5f`  
		Last Modified: Sat, 21 Dec 2019 03:57:25 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbe63d8f8664f9735cc9f5d437ca468578db4785a0dc5e83e51fee74cc51e32`  
		Last Modified: Sat, 21 Dec 2019 03:57:25 GMT  
		Size: 1.9 MB (1870678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-buster` - linux; s390x

```console
$ docker pull python@sha256:3f574b226aeb51cac5446e67aa8d050dd4adc5c1a439aa46388f08e791e692a5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330963596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dab45d917bf4040a461501381f8d30a884e8d3211a7592e13f31ea5c1d7eba`
-	Default Command: `["python3"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:51 GMT
ADD file:aeaf0b11195b2ba7eb7890ce128ad93c114a8e183a516cf2e4ea42da324c57ea in / 
# Sat, 28 Dec 2019 04:41:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:44:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:45:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:45:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:46:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 10:58:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 10:58:56 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 10:59:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 10:59:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 28 Dec 2019 11:03:35 GMT
ENV PYTHON_VERSION=3.8.1
# Sat, 28 Dec 2019 11:07:48 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Sat, 28 Dec 2019 11:07:49 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 28 Dec 2019 11:07:49 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 11:07:49 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 11:07:50 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 11:07:54 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 11:07:54 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3596c5a237f76c32832c1879a3d0c763989cb13fac0024673b03e9b549b868ea`  
		Last Modified: Sat, 28 Dec 2019 04:44:54 GMT  
		Size: 49.0 MB (48954508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a87e4c2949f278ec7636f6762169d70bd2588ed301cc3e2721aa830a9227fc`  
		Last Modified: Sat, 28 Dec 2019 05:53:25 GMT  
		Size: 7.4 MB (7380503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b91142ed28640cd70826a84025844f0fa1e7bc50f10b67f6ee03ed2f013ae`  
		Last Modified: Sat, 28 Dec 2019 05:53:25 GMT  
		Size: 9.9 MB (9880177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23386745bcbf27928754e130693faba015951a5923f1fcf54478337f15c7e06`  
		Last Modified: Sat, 28 Dec 2019 05:53:39 GMT  
		Size: 51.3 MB (51318842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a13278ceba853c41dcae8d4377f9ea4a1d146ab81715352808ca875984f87c`  
		Last Modified: Sat, 28 Dec 2019 05:54:04 GMT  
		Size: 176.6 MB (176585184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b768d3946a3fe87237f25dd45fe17ff1bc9ee3245daa2f9ed3d6587ec9b3d7`  
		Last Modified: Sat, 28 Dec 2019 11:44:33 GMT  
		Size: 5.7 MB (5705045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe445ca32bca0ec07c5ac1b0c22f4a84bc320c524e1d3c6315c55708750e6d9`  
		Last Modified: Sat, 28 Dec 2019 11:44:49 GMT  
		Size: 29.3 MB (29268749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c974f60ea7802d05922898d5851a7df6e23c9251df408886c075255b8809c967`  
		Last Modified: Sat, 28 Dec 2019 11:44:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e618be2c91c06d738157ae1b3bb58df5fa3f284473785a3bb6042d080b0e0c`  
		Last Modified: Sat, 28 Dec 2019 11:44:44 GMT  
		Size: 1.9 MB (1870355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
