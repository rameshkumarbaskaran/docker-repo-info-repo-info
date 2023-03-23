## `ruby:2-slim-buster`

```console
$ docker pull ruby@sha256:e0a7ebfacbc80a17209ee8e342d9243018e0b3887c4bbffd394fb3928fc54ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `ruby:2-slim-buster` - linux; amd64

```console
$ docker pull ruby@sha256:19be208606e9952729b1e32133de3bc1645e737f52b3532db13c6110a4568647
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54277791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1b04b9a8983af979af975bc0e2e0fe1a268a2e1e712bacf8ed58a11f05e1e2`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 17:20:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 17:20:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 01 Mar 2023 17:20:31 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 17:47:59 GMT
ENV RUBY_MAJOR=2.7
# Wed, 01 Mar 2023 17:47:59 GMT
ENV RUBY_VERSION=2.7.7
# Wed, 01 Mar 2023 17:47:59 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Wed, 01 Mar 2023 17:49:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 01 Mar 2023 17:49:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 01 Mar 2023 17:49:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 01 Mar 2023 17:49:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 17:49:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 01 Mar 2023 17:49:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7682b5f7466b6f39ee82e9691d40a4ca1bb67bfea8bc16ec7e38bf00562d0ed3`  
		Last Modified: Wed, 01 Mar 2023 17:52:34 GMT  
		Size: 12.6 MB (12581271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5c03f639e55b89597134c46536faf245cf13480d4659491354cf9b3d5346ec`  
		Last Modified: Wed, 01 Mar 2023 17:52:32 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ef79c3ed22d73104450e503ab1277afc0db629395fbfcafa168f19b0d3a4c0`  
		Last Modified: Wed, 01 Mar 2023 17:55:34 GMT  
		Size: 14.6 MB (14556262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db56570ef0aeca3b5f3f9b189f3256849f2fe3ed22cd16ce10a8dca09c7254d1`  
		Last Modified: Wed, 01 Mar 2023 17:55:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:ff11f7f18c8babea210587854ce435d989d96fb51e3766ba57bf2216f990112f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46434389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89725b6c0f2e92ed3cbb28e772f2d336ec57fcf8dc5acc226ae91a72a10e19ec`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Mar 2023 01:20:33 GMT
ADD file:b3a5424864097d73516302c7e0a8fe9394880555c85f25a82a020ec3fc887eb8 in / 
# Thu, 23 Mar 2023 01:20:34 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:04:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:04:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Mar 2023 12:04:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 12:16:59 GMT
ENV RUBY_MAJOR=2.7
# Thu, 23 Mar 2023 12:16:59 GMT
ENV RUBY_VERSION=2.7.7
# Thu, 23 Mar 2023 12:16:59 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Thu, 23 Mar 2023 12:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Mar 2023 12:18:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Mar 2023 12:18:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Mar 2023 12:18:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 12:18:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Mar 2023 12:18:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:369fe072796976e1501c1a8d490c05b9ac47287c34c004013e0982d2dd4bb7c2`  
		Last Modified: Thu, 23 Mar 2023 01:33:32 GMT  
		Size: 22.7 MB (22748632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a36a116fcde17de391a7f4c18d825c5715e3488853a964e3f5e93a78da4b74c`  
		Last Modified: Thu, 23 Mar 2023 12:19:38 GMT  
		Size: 9.9 MB (9879101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3a6b03dd3841045d5951b4c644210a362cb9c82dc3556575d44c756731cd9b`  
		Last Modified: Thu, 23 Mar 2023 12:19:36 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bd77abd1802b225b39b8cf35c8dcb0762bd7206d0c4b2064912581f569ca7c`  
		Last Modified: Thu, 23 Mar 2023 12:21:14 GMT  
		Size: 13.8 MB (13806284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3980307e383307c92555c3c53d7c86a9f6ea12ddf0b76a9cc6eee3570a1f9a15`  
		Last Modified: Thu, 23 Mar 2023 12:21:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:dfcd330059f8ea7f84c296d07198b6f547f93be0f703a6d3c9fbb324790fa89b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51605646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76d7800e0eb7056c8257bf7be69bdb8101bd427b60051329aa5cc2fb55e341d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:23 GMT
ADD file:44e400cc6a1bc5df5a57bda478c9accf9b58950fa2fd069cc7620128fe786770 in / 
# Thu, 23 Mar 2023 00:45:23 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:15:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Mar 2023 06:15:44 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 06:27:03 GMT
ENV RUBY_MAJOR=2.7
# Thu, 23 Mar 2023 06:27:03 GMT
ENV RUBY_VERSION=2.7.7
# Thu, 23 Mar 2023 06:27:03 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Thu, 23 Mar 2023 06:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Mar 2023 06:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Mar 2023 06:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Mar 2023 06:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 06:28:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Mar 2023 06:28:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:cfe0f778e53ce031ef449bc02975a07f2568716dea807ed2f390d352c0001972`  
		Last Modified: Thu, 23 Mar 2023 00:48:45 GMT  
		Size: 25.9 MB (25922660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf59d8adf19b93abd1fa3b3e9698cba257577fafa00ada83157699269b185ee`  
		Last Modified: Thu, 23 Mar 2023 06:29:26 GMT  
		Size: 11.3 MB (11281828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86dc49fc370f7c4f762b32def07e53be056ee10d300c68220210ea73a8f4e43`  
		Last Modified: Thu, 23 Mar 2023 06:29:24 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1402f59ee4612d7b5f6a880b668a02ef2f643c43c3751dc53c289fe59a0bcaeb`  
		Last Modified: Thu, 23 Mar 2023 06:30:52 GMT  
		Size: 14.4 MB (14400784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fca089ced858afb6786e23cf194c542d15fb11365a51718e6fcefd9c94ee99`  
		Last Modified: Thu, 23 Mar 2023 06:30:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:b143754e85b0a0eaeb365759bdd8457ea5f8b4724ee9a45282798371dc85a7bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59079304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae8171bb7e7cb9c5d3823ae17899d17a325b4d902c1df696290418d857bde5e`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:35 GMT
ADD file:d90e1c78fceb91ea00c9b00cdf477b7254e3d4d37b561698e90b75c62d84320c in / 
# Wed, 01 Mar 2023 01:39:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 08:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:01:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 01 Mar 2023 08:01:37 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 09:01:00 GMT
ENV RUBY_MAJOR=2.7
# Wed, 01 Mar 2023 09:01:00 GMT
ENV RUBY_VERSION=2.7.7
# Wed, 01 Mar 2023 09:01:01 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Wed, 01 Mar 2023 09:03:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 01 Mar 2023 09:03:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 01 Mar 2023 09:03:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 01 Mar 2023 09:03:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 09:03:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 01 Mar 2023 09:03:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5dd0dee7d259a761fe8021e1fd6a2a9a8590880098b27d4f97cfbda4e50bc631`  
		Last Modified: Wed, 01 Mar 2023 01:45:36 GMT  
		Size: 27.8 MB (27798766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb6a6d9ca7fe04860ade4c6a340754c3e0c5ef84adebe743f8dfb62e8955a3`  
		Last Modified: Wed, 01 Mar 2023 09:11:40 GMT  
		Size: 17.2 MB (17246925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93458dd1a2678ac86f8e3fdce64a33ae344f53bf4e2306848097f621db2dbb1b`  
		Last Modified: Wed, 01 Mar 2023 09:11:35 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed165a12c4f585b11616806c9246bae1d90a4a881d9e21b9f8a33980913dd6`  
		Last Modified: Wed, 01 Mar 2023 09:16:52 GMT  
		Size: 14.0 MB (14033238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae1dbef50128a865d4ffcee31bafac946f2a033e23b990e63027046cb0500e`  
		Last Modified: Wed, 01 Mar 2023 09:16:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
