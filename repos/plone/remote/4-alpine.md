## `plone:4-alpine`

```console
$ docker pull plone@sha256:37cb21932e0d9e5de69dc37946a08d30ccc203b104c13760c114ccd434f3d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `plone:4-alpine` - linux; amd64

```console
$ docker pull plone@sha256:8b7825e710aae27c817e893f1f7b61f529925889bd17dbd016695c5e25a7cdf2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108893697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c5cdff24300bdce962c07f0618840091f2f50d3eb55912b12bdeed24e43dea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 01:42:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Jan 2020 02:37:13 GMT
ENV LANG=C.UTF-8
# Sat, 18 Jan 2020 03:05:17 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 18 Jan 2020 03:05:18 GMT
RUN apk add --no-cache ca-certificates
# Sat, 18 Jan 2020 03:05:18 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 18 Jan 2020 03:05:18 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 18 Jan 2020 03:10:20 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 18 Jan 2020 03:10:20 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 18 Jan 2020 03:10:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 18 Jan 2020 03:10:21 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 18 Jan 2020 03:10:25 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 18 Jan 2020 03:10:26 GMT
CMD ["python2"]
# Sat, 18 Jan 2020 05:10:11 GMT
ENV PIP=9.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=40.8.0 WHEEL=0.33.1 PLONE_MAJOR=4.3 PLONE_VERSION=4.3.19 PLONE_MD5=04ed5beac7fb8504f06a36d44e407b06
# Sat, 18 Jan 2020 05:10:11 GMT
LABEL plone=4.3.19 os=alpine os.version=3.10 name=Plone 4.3 description=Plone image, based on Unified Installer maintainer=Plone Community
# Sat, 18 Jan 2020 05:10:12 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Sat, 18 Jan 2020 05:10:12 GMT
COPY file:d2686f3dde22793e1cf870d3f997b1d6ff10a1bb2a2c48fe9a9f11b9824a86c1 in /plone/instance/ 
# Sat, 18 Jan 2020 05:19:31 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5  Plone.tgz" | md5sum -c -  && tar -zxvf Plone.tgz  && cp -rv ./Plone-$PLONE_VERSION-UnifiedInstaller/base_skeleton/* /plone/instance/  && cp -v ./Plone-$PLONE_VERSION-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && rm -rf bin/buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance//var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apk del .build-deps  && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo  && rm -rf /plone/buildout-cache/downloads/*
# Sat, 18 Jan 2020 05:19:32 GMT
VOLUME [/data]
# Sat, 18 Jan 2020 05:19:33 GMT
COPY multi:1923bbb6e3d76129ed8afd8e145516fb42d067a3323b0830ce09a51a5a3d629c in / 
# Sat, 18 Jan 2020 05:19:33 GMT
EXPOSE 8080
# Sat, 18 Jan 2020 05:19:33 GMT
WORKDIR /plone/instance
# Sat, 18 Jan 2020 05:19:33 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Sat, 18 Jan 2020 05:19:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:19:34 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea5c17ab132115631f8ed013132367bade1bf4b9df91fe0e962bfbfc63336ac`  
		Last Modified: Sat, 18 Jan 2020 03:11:58 GMT  
		Size: 301.3 KB (301259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbe995357bf87b3689676cf8a89e250a99ba7fd60ab32e5eba2e83a20b4b215`  
		Last Modified: Sat, 18 Jan 2020 03:12:02 GMT  
		Size: 20.7 MB (20710099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afb78be294494b794b2f2c01c26730bff6457c34d5b6a13ba07546577e9498c`  
		Last Modified: Sat, 18 Jan 2020 03:11:59 GMT  
		Size: 1.9 MB (1866333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a82ad45119d5f52a1df44dff6cc6de735a04c6867e3e080fe21afe3729096a3`  
		Last Modified: Sat, 18 Jan 2020 05:20:55 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e26bc6dd24f9e6306eb30e8c5e9aa850cf167e8d9f465cd685fb501d04fc713`  
		Last Modified: Sat, 18 Jan 2020 05:20:55 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74006605627051fdd0e073d7839cae6ffacd8a4b1197c04f3d43d541ba92b4`  
		Last Modified: Sat, 18 Jan 2020 05:21:18 GMT  
		Size: 83.2 MB (83207586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba557a7ce1308e9163d3d062b78f53321a03a33aba618587f786379f78f58015`  
		Last Modified: Sat, 18 Jan 2020 05:20:55 GMT  
		Size: 2.9 KB (2882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:4-alpine` - linux; arm variant v6

```console
$ docker pull plone@sha256:1e63dfd4c5908b845d5bac1dca174b53408010b475a43d22fb4b49f6d1a42a2e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106888996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a991125168409a4903b40a186797193713907b4966ebbb6cc2867694fca6c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:38:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Jan 2020 04:38:59 GMT
ENV LANG=C.UTF-8
# Sat, 18 Jan 2020 05:31:00 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 18 Jan 2020 05:31:12 GMT
RUN apk add --no-cache ca-certificates
# Sat, 18 Jan 2020 05:31:17 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 18 Jan 2020 05:31:21 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 18 Jan 2020 05:42:26 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 18 Jan 2020 05:42:28 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 18 Jan 2020 05:42:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 18 Jan 2020 05:42:33 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 18 Jan 2020 05:42:51 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 18 Jan 2020 05:42:58 GMT
CMD ["python2"]
# Sat, 18 Jan 2020 08:30:35 GMT
ENV PIP=9.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=40.8.0 WHEEL=0.33.1 PLONE_MAJOR=4.3 PLONE_VERSION=4.3.19 PLONE_MD5=04ed5beac7fb8504f06a36d44e407b06
# Sat, 18 Jan 2020 08:30:37 GMT
LABEL plone=4.3.19 os=alpine os.version=3.10 name=Plone 4.3 description=Plone image, based on Unified Installer maintainer=Plone Community
# Sat, 18 Jan 2020 08:30:41 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Sat, 18 Jan 2020 08:30:42 GMT
COPY file:d2686f3dde22793e1cf870d3f997b1d6ff10a1bb2a2c48fe9a9f11b9824a86c1 in /plone/instance/ 
# Sat, 18 Jan 2020 08:50:22 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5  Plone.tgz" | md5sum -c -  && tar -zxvf Plone.tgz  && cp -rv ./Plone-$PLONE_VERSION-UnifiedInstaller/base_skeleton/* /plone/instance/  && cp -v ./Plone-$PLONE_VERSION-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && rm -rf bin/buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance//var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apk del .build-deps  && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo  && rm -rf /plone/buildout-cache/downloads/*
# Sat, 18 Jan 2020 08:50:27 GMT
VOLUME [/data]
# Sat, 18 Jan 2020 08:50:28 GMT
COPY multi:1923bbb6e3d76129ed8afd8e145516fb42d067a3323b0830ce09a51a5a3d629c in / 
# Sat, 18 Jan 2020 08:50:29 GMT
EXPOSE 8080
# Sat, 18 Jan 2020 08:50:29 GMT
WORKDIR /plone/instance
# Sat, 18 Jan 2020 08:50:30 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Sat, 18 Jan 2020 08:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 18 Jan 2020 08:50:31 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f9ee5cb431b6df66261c35037b6a83da0e40c73306a795eab69536be10dfe1`  
		Last Modified: Sat, 18 Jan 2020 05:45:09 GMT  
		Size: 301.6 KB (301617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d417f4578e06c92fe68969a793bf3852e440daea306071b5d92b5c502fd710c2`  
		Last Modified: Sat, 18 Jan 2020 05:45:17 GMT  
		Size: 19.4 MB (19402798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a63a0774912f9ac4dd5c1437e52d6ebbdf7d46db19f2fe155901e32f4105b46`  
		Last Modified: Sat, 18 Jan 2020 05:45:10 GMT  
		Size: 1.9 MB (1866638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713c9be1ec87ac6d7c41b7a356e5622531c1d646bd9ec66e37a38cd3607d879c`  
		Last Modified: Sat, 18 Jan 2020 08:52:55 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854b109261c7eafbee3a685d612e481b4807639074abdde16a82498277881384`  
		Last Modified: Sat, 18 Jan 2020 08:52:55 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a7f12bf105d5815e3aa52882233c10af53a0865e602e7a159614b37889b01e`  
		Last Modified: Sat, 18 Jan 2020 08:53:33 GMT  
		Size: 82.7 MB (82694852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7653919b28d29adc59b854110b9d470260ae0e62b2235d08996cac1f2f31ea6f`  
		Last Modified: Sat, 18 Jan 2020 08:52:55 GMT  
		Size: 2.9 KB (2881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:4-alpine` - linux; arm64 variant v8

```console
$ docker pull plone@sha256:ab832218f6cf1b0b2dce951da90d362a64e9cb609c038c2bfe2b70c560b2bc06
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108132045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83992ca29ff74395291940ddc1be6f414eecb13692158102cf47c2f6eab7dc86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:23:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Jan 2020 03:23:12 GMT
ENV LANG=C.UTF-8
# Sat, 18 Jan 2020 04:06:50 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 18 Jan 2020 04:06:57 GMT
RUN apk add --no-cache ca-certificates
# Sat, 18 Jan 2020 04:06:58 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 18 Jan 2020 04:07:00 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 18 Jan 2020 04:16:17 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 18 Jan 2020 04:16:23 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 18 Jan 2020 04:16:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 18 Jan 2020 04:16:31 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 18 Jan 2020 04:16:45 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 18 Jan 2020 04:16:48 GMT
CMD ["python2"]
# Sat, 18 Jan 2020 08:32:37 GMT
ENV PIP=9.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=40.8.0 WHEEL=0.33.1 PLONE_MAJOR=4.3 PLONE_VERSION=4.3.19 PLONE_MD5=04ed5beac7fb8504f06a36d44e407b06
# Sat, 18 Jan 2020 08:32:38 GMT
LABEL plone=4.3.19 os=alpine os.version=3.10 name=Plone 4.3 description=Plone image, based on Unified Installer maintainer=Plone Community
# Sat, 18 Jan 2020 08:32:42 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Sat, 18 Jan 2020 08:32:43 GMT
COPY file:d2686f3dde22793e1cf870d3f997b1d6ff10a1bb2a2c48fe9a9f11b9824a86c1 in /plone/instance/ 
# Sat, 18 Jan 2020 08:52:37 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5  Plone.tgz" | md5sum -c -  && tar -zxvf Plone.tgz  && cp -rv ./Plone-$PLONE_VERSION-UnifiedInstaller/base_skeleton/* /plone/instance/  && cp -v ./Plone-$PLONE_VERSION-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && rm -rf bin/buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance//var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apk del .build-deps  && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo  && rm -rf /plone/buildout-cache/downloads/*
# Sat, 18 Jan 2020 08:52:50 GMT
VOLUME [/data]
# Sat, 18 Jan 2020 08:52:51 GMT
COPY multi:1923bbb6e3d76129ed8afd8e145516fb42d067a3323b0830ce09a51a5a3d629c in / 
# Sat, 18 Jan 2020 08:52:52 GMT
EXPOSE 8080
# Sat, 18 Jan 2020 08:52:53 GMT
WORKDIR /plone/instance
# Sat, 18 Jan 2020 08:52:55 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Sat, 18 Jan 2020 08:52:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 18 Jan 2020 08:52:57 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55aa4b23d1c945e644c16e0a10c13704ef3215b13d1752d03032a86786dc0a4`  
		Last Modified: Sat, 18 Jan 2020 04:19:56 GMT  
		Size: 301.8 KB (301760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec79a1c6d20ca237f366b092214e9eac3f82f49a431ddf5308b4815bfa96556`  
		Last Modified: Sat, 18 Jan 2020 04:20:03 GMT  
		Size: 20.4 MB (20364606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5f9354c0adebf0cff3e3665562084db2ff8813b2a371e6634d9c3bdceff8ce`  
		Last Modified: Sat, 18 Jan 2020 04:19:56 GMT  
		Size: 1.9 MB (1866651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec2b130d4ee4d3722fde146f79dd89860b194086ce7d3f71b22530bcd915779`  
		Last Modified: Sat, 18 Jan 2020 08:55:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de9f07540283b5c496e6032b5b31b16f8af2da11a833d0bac81874907171182`  
		Last Modified: Sat, 18 Jan 2020 08:55:01 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa22e5077bb3d23c164528359effe12d1accac130d8752975515a5885badcab`  
		Last Modified: Sat, 18 Jan 2020 08:55:31 GMT  
		Size: 82.9 MB (82870425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da45458b48e2516e9db8783fb9a3a7092be35a355a0161f7ffd0a1135b532c60`  
		Last Modified: Sat, 18 Jan 2020 08:55:01 GMT  
		Size: 2.9 KB (2882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:4-alpine` - linux; 386

```console
$ docker pull plone@sha256:4a1ea9f17a21ff129a9a44aaba2592cfb9130f55ceee3aa049c1b664df4e8c90
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109100612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19553522680ed21389240e3e9d68104a25f492165d54b744b666fbfcbd7cb397`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Fri, 27 Dec 2019 00:13:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Dec 2019 00:13:09 GMT
ENV LANG=C.UTF-8
# Fri, 27 Dec 2019 01:17:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 27 Dec 2019 01:17:46 GMT
RUN apk add --no-cache ca-certificates
# Fri, 27 Dec 2019 01:17:46 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Fri, 27 Dec 2019 01:17:46 GMT
ENV PYTHON_VERSION=2.7.17
# Fri, 27 Dec 2019 01:23:56 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Fri, 27 Dec 2019 01:23:56 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 27 Dec 2019 01:23:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 27 Dec 2019 01:23:57 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 27 Dec 2019 01:24:03 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 27 Dec 2019 01:24:03 GMT
CMD ["python2"]
# Fri, 27 Dec 2019 02:37:47 GMT
ENV PIP=9.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=40.8.0 WHEEL=0.33.1 PLONE_MAJOR=4.3 PLONE_VERSION=4.3.19 PLONE_MD5=04ed5beac7fb8504f06a36d44e407b06
# Fri, 27 Dec 2019 02:37:47 GMT
LABEL plone=4.3.19 os=alpine os.version=3.10 name=Plone 4.3 description=Plone image, based on Unified Installer maintainer=Plone Community
# Fri, 27 Dec 2019 02:37:48 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Fri, 27 Dec 2019 02:37:48 GMT
COPY file:d2686f3dde22793e1cf870d3f997b1d6ff10a1bb2a2c48fe9a9f11b9824a86c1 in /plone/instance/ 
# Fri, 27 Dec 2019 02:48:58 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5  Plone.tgz" | md5sum -c -  && tar -zxvf Plone.tgz  && cp -rv ./Plone-$PLONE_VERSION-UnifiedInstaller/base_skeleton/* /plone/instance/  && cp -v ./Plone-$PLONE_VERSION-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && rm -rf bin/buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance//var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apk del .build-deps  && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo  && rm -rf /plone/buildout-cache/downloads/*
# Fri, 27 Dec 2019 02:48:59 GMT
VOLUME [/data]
# Fri, 27 Dec 2019 02:48:59 GMT
COPY multi:1923bbb6e3d76129ed8afd8e145516fb42d067a3323b0830ce09a51a5a3d629c in / 
# Fri, 27 Dec 2019 02:48:59 GMT
EXPOSE 8080
# Fri, 27 Dec 2019 02:48:59 GMT
WORKDIR /plone/instance
# Fri, 27 Dec 2019 02:49:00 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Fri, 27 Dec 2019 02:49:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 02:49:00 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4da1fab2efe01267d0a1473ffb8f1f4343262be0cc184efc10df9681fc1223c`  
		Last Modified: Fri, 27 Dec 2019 01:26:47 GMT  
		Size: 301.9 KB (301916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b2354ba38dd60abbd3b32f1ec5374e91ef2f00a721c6e3f1cf1a6ed5a547a7`  
		Last Modified: Fri, 27 Dec 2019 01:26:52 GMT  
		Size: 21.5 MB (21458073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf62fe68aabe29e41db98062995b1965fd64dcb92eb4bd391922e79494fad06`  
		Last Modified: Fri, 27 Dec 2019 01:26:48 GMT  
		Size: 1.9 MB (1866219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ac367d4462cbe733e60d54167d564b66a5a65a3958244c9dd0e473e8dd63f2`  
		Last Modified: Fri, 27 Dec 2019 02:50:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3f69faed1f57b6863a010f8e8ad1e5923397ed21049da84d475b67e48c94ef`  
		Last Modified: Fri, 27 Dec 2019 02:50:42 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f25cf10403cd1baf0239cbd18d84dbf4c6f957fd6e16531dac721cbd9f59d57`  
		Last Modified: Fri, 27 Dec 2019 02:51:07 GMT  
		Size: 82.7 MB (82663792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecc1f592a6f9d64bd687c91360af9f7c8825c8b81da974a236d900449c08655`  
		Last Modified: Fri, 27 Dec 2019 02:50:42 GMT  
		Size: 2.9 KB (2882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:4-alpine` - linux; ppc64le

```console
$ docker pull plone@sha256:019bebc67eba0eb549de6ca37fe17498450736e4e557e64e2cba4551cab0a4ed
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111354923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ea427eab6b7b43141dcc323e538051f58d676f13c2b69bfa1cd2a84a2a4a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 23:28:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2019 23:28:17 GMT
ENV LANG=C.UTF-8
# Fri, 27 Dec 2019 00:44:25 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 27 Dec 2019 00:44:31 GMT
RUN apk add --no-cache ca-certificates
# Fri, 27 Dec 2019 00:44:34 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Fri, 27 Dec 2019 00:44:37 GMT
ENV PYTHON_VERSION=2.7.17
# Fri, 27 Dec 2019 00:51:40 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Fri, 27 Dec 2019 00:51:45 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 27 Dec 2019 00:51:47 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 27 Dec 2019 00:51:49 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 27 Dec 2019 00:52:02 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 27 Dec 2019 00:52:04 GMT
CMD ["python2"]
# Fri, 27 Dec 2019 03:07:18 GMT
ENV PIP=9.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=40.8.0 WHEEL=0.33.1 PLONE_MAJOR=4.3 PLONE_VERSION=4.3.19 PLONE_MD5=04ed5beac7fb8504f06a36d44e407b06
# Fri, 27 Dec 2019 03:07:20 GMT
LABEL plone=4.3.19 os=alpine os.version=3.10 name=Plone 4.3 description=Plone image, based on Unified Installer maintainer=Plone Community
# Fri, 27 Dec 2019 03:07:26 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Fri, 27 Dec 2019 03:07:27 GMT
COPY file:d2686f3dde22793e1cf870d3f997b1d6ff10a1bb2a2c48fe9a9f11b9824a86c1 in /plone/instance/ 
# Fri, 27 Dec 2019 03:24:46 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5  Plone.tgz" | md5sum -c -  && tar -zxvf Plone.tgz  && cp -rv ./Plone-$PLONE_VERSION-UnifiedInstaller/base_skeleton/* /plone/instance/  && cp -v ./Plone-$PLONE_VERSION-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && rm -rf bin/buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance//var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apk del .build-deps  && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo  && rm -rf /plone/buildout-cache/downloads/*
# Fri, 27 Dec 2019 03:24:54 GMT
VOLUME [/data]
# Fri, 27 Dec 2019 03:24:55 GMT
COPY multi:1923bbb6e3d76129ed8afd8e145516fb42d067a3323b0830ce09a51a5a3d629c in / 
# Fri, 27 Dec 2019 03:24:57 GMT
EXPOSE 8080
# Fri, 27 Dec 2019 03:25:01 GMT
WORKDIR /plone/instance
# Fri, 27 Dec 2019 03:25:04 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Fri, 27 Dec 2019 03:25:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 03:25:13 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6011251a4284beca320fe978a46c7db27fd3fc91b2ffe9f618d45a15d79fa3a0`  
		Last Modified: Fri, 27 Dec 2019 00:57:58 GMT  
		Size: 304.0 KB (303978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d225238fd6b2605a1be534512da327b2796049f64d9ef70743c0a296fca01a0f`  
		Last Modified: Fri, 27 Dec 2019 00:58:04 GMT  
		Size: 22.8 MB (22845979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30809c73c619392a495d984e607fe234c0c3b1e0d773e43f1020533d82463bc8`  
		Last Modified: Fri, 27 Dec 2019 00:57:58 GMT  
		Size: 1.9 MB (1866500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36111c702cd6d976acd1e800800ce4ae3e09ceb5571bf8aecf17899a43425ddc`  
		Last Modified: Fri, 27 Dec 2019 03:29:47 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531077f4afe87090aeea568731672853db5fc721a841914ff9e5a4fe181feef1`  
		Last Modified: Fri, 27 Dec 2019 03:29:48 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25ee761aef22394b1950285d28b2813a18341bbc3c74f933355b4a0905c957e`  
		Last Modified: Fri, 27 Dec 2019 03:31:42 GMT  
		Size: 83.5 MB (83516456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf99e91b9d677139fb543129f209bae6f0780f29d0cc161f2242b8724110dd84`  
		Last Modified: Fri, 27 Dec 2019 03:29:48 GMT  
		Size: 2.9 KB (2881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `plone:4-alpine` - linux; s390x

```console
$ docker pull plone@sha256:5deb0b3d8272529501e968d72a3d6f259938016a378c74303ba854bb6c4d9df5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105813789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f67df8d945e51112f46364d7f96ecc877ef28a2a22618c1f85b073bcdc4433`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Mon, 21 Oct 2019 16:47:28 GMT
ADD file:49020543846e4f93b34d71c0e4234ade7bd6dde3f45cb73784aa73ce0522c8bc in / 
# Mon, 21 Oct 2019 16:47:29 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 18:57:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2019 18:57:49 GMT
ENV LANG=C.UTF-8
# Tue, 22 Oct 2019 01:16:25 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 22 Oct 2019 01:16:26 GMT
RUN apk add --no-cache ca-certificates
# Tue, 22 Oct 2019 01:16:26 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Thu, 24 Oct 2019 00:57:22 GMT
ENV PYTHON_VERSION=2.7.17
# Fri, 15 Nov 2019 03:54:46 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		zlib-dev 	&& apk del .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-shared 		--enable-unicode=ucs4 		--with-system-expat 		--with-system-ffi 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Fri, 15 Nov 2019 03:54:47 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 15 Nov 2019 03:54:47 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 15 Nov 2019 03:54:47 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 15 Nov 2019 03:54:52 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 15 Nov 2019 03:54:52 GMT
CMD ["python2"]
# Fri, 15 Nov 2019 05:41:29 GMT
ENV PIP=9.0.3 ZC_BUILDOUT=2.13.1 SETUPTOOLS=40.8.0 WHEEL=0.33.1 PLONE_MAJOR=4.3 PLONE_VERSION=4.3.19 PLONE_MD5=04ed5beac7fb8504f06a36d44e407b06
# Fri, 15 Nov 2019 05:41:29 GMT
LABEL plone=4.3.19 os=alpine os.version=3.10 name=Plone 4.3 description=Plone image, based on Unified Installer maintainer=Plone Community
# Fri, 15 Nov 2019 05:41:30 GMT
RUN addgroup -g 500 plone  && adduser -S -D -G plone -u 500 plone  && mkdir -p /plone/instance /data/filestorage /data/blobstorage
# Fri, 15 Nov 2019 05:41:30 GMT
COPY file:d2686f3dde22793e1cf870d3f997b1d6ff10a1bb2a2c48fe9a9f11b9824a86c1 in /plone/instance/ 
# Fri, 15 Nov 2019 05:49:38 GMT
RUN apk add --no-cache --virtual .build-deps     gcc     libc-dev     zlib-dev     libjpeg-turbo-dev     libpng-dev     libxml2-dev     libxslt-dev     pcre-dev  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5  Plone.tgz" | md5sum -c -  && tar -zxvf Plone.tgz  && cp -rv ./Plone-$PLONE_VERSION-UnifiedInstaller/base_skeleton/* /plone/instance/  && cp -v ./Plone-$PLONE_VERSION-UnifiedInstaller/buildout_templates/buildout.cfg /plone/instance/buildout-base.cfg  && pip install pip==$PIP setuptools==$SETUPTOOLS zc.buildout==$ZC_BUILDOUT wheel==$WHEEL  && cd /plone/instance  && buildout  && rm -rf bin/buildout  && ln -s /data/filestorage/ /plone/instance/var/filestorage  && ln -s /data/blobstorage /plone/instance//var/blobstorage  && find /data  -not -user plone -exec chown plone:plone {} \+  && find /plone -not -user plone -exec chown plone:plone {} \+  && rm -rf /Plone*  && apk del .build-deps  && apk add --no-cache --virtual .run-deps     su-exec     bash     rsync     libxml2     libxslt     libjpeg-turbo  && rm -rf /plone/buildout-cache/downloads/*
# Fri, 15 Nov 2019 05:49:39 GMT
VOLUME [/data]
# Fri, 15 Nov 2019 05:49:40 GMT
COPY multi:1923bbb6e3d76129ed8afd8e145516fb42d067a3323b0830ce09a51a5a3d629c in / 
# Fri, 15 Nov 2019 05:49:40 GMT
EXPOSE 8080
# Fri, 15 Nov 2019 05:49:40 GMT
WORKDIR /plone/instance
# Fri, 15 Nov 2019 05:49:41 GMT
HEALTHCHECK &{["CMD-SHELL" "nc -z -w5 127.0.0.1 8080 || exit 1"] "1m0s" "5s" "1m0s" '\x00'}
# Fri, 15 Nov 2019 05:49:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2019 05:49:41 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:fb7172052a60e640810f01efff381654bf9ed44082461455cfcc6306d192d541`  
		Last Modified: Mon, 21 Oct 2019 16:48:40 GMT  
		Size: 2.6 MB (2573587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87da057bc7467c488226a0f5368a96c0eb396ff2684bd7a58d0dbb5c88ef6334`  
		Last Modified: Tue, 22 Oct 2019 01:19:36 GMT  
		Size: 302.4 KB (302376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b59e9c7ba879b7726965965c20aebe3c0d4b0d1032d472bfa698573429771b`  
		Last Modified: Fri, 15 Nov 2019 04:02:57 GMT  
		Size: 18.8 MB (18760145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9909268e4fa5a3831d4999d5a4f51fbe166535e2aa4f6a10ec849612450f3cd4`  
		Last Modified: Fri, 15 Nov 2019 04:02:41 GMT  
		Size: 1.9 MB (1865159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713d1701eacb2a15b19690ac4773c55641b5d1debba3f196cfc7990e6c774496`  
		Last Modified: Fri, 15 Nov 2019 05:50:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9774f4c2b30a6dd85f9aeb626f23f15158bf3b3875cf7ff0a8b43bb685ba2e6`  
		Last Modified: Fri, 15 Nov 2019 05:50:57 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0532261992abf2ba66caecbfa821c01b3cf5a66cb39a4ec2e57587d94cd71`  
		Last Modified: Fri, 15 Nov 2019 05:51:14 GMT  
		Size: 82.3 MB (82307029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c29cf0a416f0efa34e9e523d60f254cbbf77def9f8b1b1141ebad83e803c55f`  
		Last Modified: Fri, 15 Nov 2019 05:50:57 GMT  
		Size: 2.9 KB (2881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
