## `ruby:2-buster`

```console
$ docker pull ruby@sha256:8a543e50fe465ecea579ceada26cd1ee7558216c1abfd6d9cad85f9852bbc473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `ruby:2-buster` - linux; amd64

```console
$ docker pull ruby@sha256:c98299bc1a36ae046d7acc3d4fcc9974f31501d7cc8603179177445bc0790176
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326668743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a8d47489b71d59942ec0d2594109d34f01569cf2f40b37351a15f4be8254fd`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:24:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 07:24:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:25:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 20:21:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 04 Feb 2023 20:21:42 GMT
ENV LANG=C.UTF-8
# Sat, 04 Feb 2023 20:49:02 GMT
ENV RUBY_MAJOR=2.7
# Sat, 04 Feb 2023 20:49:02 GMT
ENV RUBY_VERSION=2.7.7
# Sat, 04 Feb 2023 20:49:02 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Sat, 04 Feb 2023 20:50:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 04 Feb 2023 20:50:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Feb 2023 20:50:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Feb 2023 20:50:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 20:50:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 04 Feb 2023 20:50:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390d41539fbbd93f1f47d53f91bd33882827be2b6c7bd1aee8e0e5a3357e375`  
		Last Modified: Sat, 04 Feb 2023 07:30:33 GMT  
		Size: 7.9 MB (7861207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b21370b9f71057fb1b91dcef9da199c272320fda90e0f449887f779b625b4`  
		Last Modified: Sat, 04 Feb 2023 07:30:33 GMT  
		Size: 10.0 MB (10001436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab930f25aaae407656553520d66a66def23df0c747402157413d83ec3726f10`  
		Last Modified: Sat, 04 Feb 2023 07:30:49 GMT  
		Size: 51.9 MB (51867959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955f339d2cf4512ae13cf7c3f00f454c99cfcc7c4b17f1f1fdaacc8e3c60289b`  
		Last Modified: Sat, 04 Feb 2023 07:31:22 GMT  
		Size: 191.9 MB (191922928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc697e2d418c8ae0e3bf22154c2380bb11b0935689b6d921e11858fa554e2d17`  
		Last Modified: Sat, 04 Feb 2023 20:54:42 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff06dd60d0f5e52d504c9a7ceb176e84b0938469f052e714fa31a7e035954046`  
		Last Modified: Sat, 04 Feb 2023 20:57:46 GMT  
		Size: 14.6 MB (14565727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b314f3a1539ea746539d3bb5471447dbe6125bdb60535afe11991b82fafd3104`  
		Last Modified: Sat, 04 Feb 2023 20:57:44 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:705d5883d91875dcefd1aa18368d95d5d53b14f4d9afe23559fa8cccf85108f3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291765468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fa05a560f98a57efae603de1d49c5921aa9f1e6003924049862db220d72011`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 04 Feb 2023 09:59:50 GMT
ADD file:afaf1103e4ec74dcbbf13ec6a8049b78c15a909b8713dce5796a5ef6d7d5cbd4 in / 
# Sat, 04 Feb 2023 09:59:50 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:50:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 10:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:52:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 20:26:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 04 Feb 2023 20:26:22 GMT
ENV LANG=C.UTF-8
# Sat, 04 Feb 2023 20:52:58 GMT
ENV RUBY_MAJOR=2.7
# Sat, 04 Feb 2023 20:52:58 GMT
ENV RUBY_VERSION=2.7.7
# Sat, 04 Feb 2023 20:52:58 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Sat, 04 Feb 2023 20:54:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 04 Feb 2023 20:54:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Feb 2023 20:54:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Feb 2023 20:54:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 20:54:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 04 Feb 2023 20:54:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6dcab737b693be9e498f0363e4109adad2721ce23274f5579d19c70a85bd0dd6`  
		Last Modified: Sat, 04 Feb 2023 10:06:48 GMT  
		Size: 45.9 MB (45915803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6e058491667780df79c8ec2f0e4ab6d30a1fd4de33026781accda5b3f6963e`  
		Last Modified: Sat, 04 Feb 2023 11:00:26 GMT  
		Size: 7.1 MB (7148033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc01ede664e8db1e40b02e51768800016138b95a3b01c6acbef2ff92bc72b971`  
		Last Modified: Sat, 04 Feb 2023 11:00:26 GMT  
		Size: 9.3 MB (9348950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7884d12160d845706964d8461ae4c4230da405e65c813c8de89d04b1eb95bf1b`  
		Last Modified: Sat, 04 Feb 2023 11:00:45 GMT  
		Size: 47.4 MB (47397102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d6d3f40feedf9f36571597bf0d58133db7b072488d5d4306f6d19ace14c19f`  
		Last Modified: Sat, 04 Feb 2023 11:01:22 GMT  
		Size: 168.1 MB (168105321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49608928368693e06167a6f1763a650804329f647b973e35efc7d1206c266a9b`  
		Last Modified: Sat, 04 Feb 2023 21:01:42 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33924a53bad2cb039fa6ba08bfafd0666c1b1844539f2a7e4997a434d3a95225`  
		Last Modified: Sat, 04 Feb 2023 21:06:00 GMT  
		Size: 13.8 MB (13849916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba4a7e839cd75f370019ac9444105d72ba579b226690a0a7e336cfb80fcb04`  
		Last Modified: Sat, 04 Feb 2023 21:05:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:abfac3c144c63cb77ae072dda5f901a01b12e76da4ec138ab08e5843bc063ce8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317085182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461f10807af7b805051c80a9062a15f0a248b6e9634679a1d137246b468891df`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:48 GMT
ADD file:fba5b8ea423b27a3182ca7344a0d2365acc105b05b21a0da48675799058af042 in / 
# Thu, 09 Feb 2023 03:58:49 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:09:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:09:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 09:09:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:10:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 21:16:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 09 Feb 2023 21:16:25 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 21:26:04 GMT
ENV RUBY_MAJOR=2.7
# Thu, 09 Feb 2023 21:26:04 GMT
ENV RUBY_VERSION=2.7.7
# Thu, 09 Feb 2023 21:26:04 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Thu, 09 Feb 2023 21:27:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 09 Feb 2023 21:27:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 09 Feb 2023 21:27:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 09 Feb 2023 21:27:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 21:27:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 09 Feb 2023 21:27:10 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4b9dcf1a413259e77edbbd27343105dd36806b4cafcd111a22643d0f4b9a619f`  
		Last Modified: Thu, 09 Feb 2023 04:02:52 GMT  
		Size: 49.2 MB (49239119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e4160b1fcca909cd3754de59fc8ede1ec2474c8db65b3228181597bc0c1af6`  
		Last Modified: Thu, 09 Feb 2023 09:15:19 GMT  
		Size: 7.7 MB (7729381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4582ad2d4aa743383d14b7cbf2b2ea971703b6bb3fd7f359c424cf40471c002`  
		Last Modified: Thu, 09 Feb 2023 09:15:19 GMT  
		Size: 10.0 MB (10003621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92cd0ceb159c469814ce2cc5423354b1766c2627b313e1eb6fe616c3ec84641`  
		Last Modified: Thu, 09 Feb 2023 09:15:37 GMT  
		Size: 52.2 MB (52190981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f070cb675c685c98b535c55826863a03a3bf0dea76e971b13ac70ab7bd4a4101`  
		Last Modified: Thu, 09 Feb 2023 09:16:02 GMT  
		Size: 183.5 MB (183500324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16f07f349bfda3891fa43d65b3f24e60761cbe85dd3862f200ceff349b8589c`  
		Last Modified: Thu, 09 Feb 2023 21:29:12 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a52c210a47f66e44b74a4358d011beaaf8cc38a6b5fa36e2c80390df2204d09`  
		Last Modified: Thu, 09 Feb 2023 21:31:01 GMT  
		Size: 14.4 MB (14421380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0265e8013127d16ccd1703b407c10e9d4fed881a4872357127d39f304e8330f1`  
		Last Modified: Thu, 09 Feb 2023 21:30:59 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-buster` - linux; 386

```console
$ docker pull ruby@sha256:5e153c5df1c403d18f1a941a076ba9d1cc415fb71a6d1c38ed1ce87582bb61e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335066581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f558bb1dd8c4765eb6c316c2520c005c13973cb22116782a9488dc6a807f159`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:33 GMT
ADD file:23aa007679cd84321e9278c9f6261256b1734b2e27727d84ecd3e3418e6b8dff in / 
# Sat, 04 Feb 2023 07:49:34 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:21:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:21:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 08:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:22:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 20:57:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 04 Feb 2023 20:57:54 GMT
ENV LANG=C.UTF-8
# Sat, 04 Feb 2023 21:25:06 GMT
ENV RUBY_MAJOR=2.7
# Sat, 04 Feb 2023 21:25:07 GMT
ENV RUBY_VERSION=2.7.7
# Sat, 04 Feb 2023 21:25:08 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Sat, 04 Feb 2023 21:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 04 Feb 2023 21:26:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Feb 2023 21:26:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Feb 2023 21:26:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 21:26:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 04 Feb 2023 21:26:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:18e547e593209084f2c8150bc5b70229a02a902a855c32fb560765e6a40891a2`  
		Last Modified: Sat, 04 Feb 2023 07:55:26 GMT  
		Size: 51.2 MB (51207661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8fea1d8fd49ba5a0ae9da75d09851083564e4fa53759c92ed5a03751202a4`  
		Last Modified: Sat, 04 Feb 2023 08:28:15 GMT  
		Size: 8.0 MB (8028113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8515c265b400bd98948709e2586c37c422b0d2048eb83a5ccdc8b29283cabc0`  
		Last Modified: Sat, 04 Feb 2023 08:28:15 GMT  
		Size: 10.1 MB (10128141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb9f57be690b700ae664ce1678e467395e53370cce9c61888dfd14a6db428d`  
		Last Modified: Sat, 04 Feb 2023 08:28:33 GMT  
		Size: 53.5 MB (53469942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d7c58887265197048a04add11323a261040eb5f85124f174477290a2046bda`  
		Last Modified: Sat, 04 Feb 2023 08:29:07 GMT  
		Size: 198.4 MB (198445277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9792af01fd45981544390926ebefe58d7fb516ebcfafdb48939de9584b5d83a3`  
		Last Modified: Sat, 04 Feb 2023 21:32:38 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8036671b102cd51292564a6146c697eb7ea60c763c0bfaf1b629668ecdf312ef`  
		Last Modified: Sat, 04 Feb 2023 21:36:25 GMT  
		Size: 13.8 MB (13787105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1539af1e492c00d9815835fead3cb83702e96398fd405fb50c0564614c088f30`  
		Last Modified: Sat, 04 Feb 2023 21:36:23 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
