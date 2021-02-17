## `golang:alpine3.12`

```console
$ docker pull golang@sha256:460a09e1b0f8b0e20dc23c49e10478b67af129f876a0cbc7c1f32977d9e70fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:alpine3.12` - linux; amd64

```console
$ docker pull golang@sha256:c1e13decd43c53629268fc48e14002631d7763b5cc984c82ec2136d2d14b3803
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108788651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808c8917ccc9324066bd74a14877d4c237c8ce0a17e3be63453bc1ef8c5be312`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 14:44:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 17 Dec 2020 14:44:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 14:44:21 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:23:56 GMT
ENV GOLANG_VERSION=1.16
# Wed, 17 Feb 2021 01:27:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='softfloat' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 	sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 17 Feb 2021 01:27:58 GMT
ENV GOPATH=/go
# Wed, 17 Feb 2021 01:27:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:28:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 17 Feb 2021 01:28:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0a1ba97153114db0134946070dd8e9886006994efe6e8fc8bd700f6970095f`  
		Last Modified: Thu, 17 Dec 2020 14:55:48 GMT  
		Size: 280.8 KB (280811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db7f31c0ee6d2a9f0c724c904ce2025164938e289d0250dd31d6bfafc452237`  
		Last Modified: Thu, 17 Dec 2020 14:55:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4308f52cebf14c342017a1d6ad96bf815da89f6a1a2cab2bd3426741377f603`  
		Last Modified: Wed, 17 Feb 2021 01:30:41 GMT  
		Size: 105.7 MB (105708496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59fd13825a9f468237379b7d02373e8667e4aea30f30f078212bedb04b43354`  
		Last Modified: Wed, 17 Feb 2021 01:30:16 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.12` - linux; arm variant v6

```console
$ docker pull golang@sha256:290b7710ef399b1e88db0be1fbc776eb7655d87df55c72eb4a81c3fbed0dd18d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104777849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb987832f674158a662ff859117bb02731cf0226db703a17883d188cfcdb6e56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:19:24 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 17 Dec 2020 01:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 01:19:28 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:53:25 GMT
ENV GOLANG_VERSION=1.16
# Wed, 17 Feb 2021 01:56:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='softfloat' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 	sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 17 Feb 2021 01:56:30 GMT
ENV GOPATH=/go
# Wed, 17 Feb 2021 01:56:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:56:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 17 Feb 2021 01:56:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec13a9d7ac84771eb7bc7617ba663afac7b1d2653e88d9bcdb8bccf6582b80aa`  
		Last Modified: Thu, 17 Dec 2020 01:29:41 GMT  
		Size: 281.0 KB (280973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9257d191bf96f32644fd965aa6a4ff717d858165485be44d9b4ab2f88819120`  
		Last Modified: Thu, 17 Dec 2020 01:29:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ef9f621b9b6f864229b8e75a800bf54e53f31a1aea14c36d6cb00f06d63f90`  
		Last Modified: Wed, 17 Feb 2021 01:58:24 GMT  
		Size: 101.9 MB (101892403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1cc931e9a8c143e8bd4f79d3c1a6caa5484615d25b1441195543549c8a20e3`  
		Last Modified: Wed, 17 Feb 2021 01:57:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.12` - linux; arm variant v7

```console
$ docker pull golang@sha256:42406257ed158904e8b173ae7ec0c5c2cf980bd1cdb4a36774e5b350422bae7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104375616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9065de4b7bca26e72034921869ff4807646917fc291ca7b417b3024883c938a2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:25:33 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 17 Dec 2020 01:25:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 01:25:38 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 02:02:21 GMT
ENV GOLANG_VERSION=1.16
# Wed, 17 Feb 2021 02:04:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='softfloat' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 	sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 17 Feb 2021 02:04:37 GMT
ENV GOPATH=/go
# Wed, 17 Feb 2021 02:04:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 02:04:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 17 Feb 2021 02:04:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0ca5f7e7e39c37c9f0a26160a742edda20ab73836336395e0b0aeded33776`  
		Last Modified: Thu, 17 Dec 2020 01:34:49 GMT  
		Size: 280.1 KB (280060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6490e713d90e3419a99e20463b25f536cd4a3aa5b97dc06f62e6dbdc4f826435`  
		Last Modified: Thu, 17 Dec 2020 01:34:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b2041a283d8f336fdb6473c68af5585f6a425a651c3ff486a616845fe59f21`  
		Last Modified: Wed, 17 Feb 2021 02:07:40 GMT  
		Size: 101.7 MB (101687692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6f691d273e2506fb87a982040fb20fa7bb10d9dde676537261bbd5bc298d87`  
		Last Modified: Wed, 17 Feb 2021 02:07:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a6ac81db12fc0cc04aa995927adf0f5068e36a8964209045d1e4cf7a7a17a5bb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (103998718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5e811d0fde07d9695fa732f49a2c13a6f97b060ef373f64543de17163f2c87`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:41:45 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 17 Dec 2020 04:41:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 04:41:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:43:30 GMT
ENV GOLANG_VERSION=1.16
# Wed, 17 Feb 2021 01:45:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='softfloat' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 	sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 17 Feb 2021 01:45:25 GMT
ENV GOPATH=/go
# Wed, 17 Feb 2021 01:45:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:45:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 17 Feb 2021 01:45:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e1f0424fba9fa0ae1558cf9537def9b5de2873566d5ef8564ba0f4a4e99fc6`  
		Last Modified: Thu, 17 Dec 2020 04:51:04 GMT  
		Size: 281.2 KB (281214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e458f4c6c667cc63829508308a9735d0586f4f55eff2b6c07236536557461e0`  
		Last Modified: Thu, 17 Dec 2020 04:51:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f903f760e2f27bfe9a4c757bbf65b02092f8def70bf40a6bb3871a18a4fae77`  
		Last Modified: Wed, 17 Feb 2021 01:48:07 GMT  
		Size: 101.0 MB (101008146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc59a1f83a7d26fb8d1649c288350f67c20213d101bcb646a7f60a2243d592fe`  
		Last Modified: Wed, 17 Feb 2021 01:47:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.12` - linux; 386

```console
$ docker pull golang@sha256:ced20a0980390a0080c98b8368ee60ace5dec426af8f51cc63578ef6cb71ea74
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108461243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa63a40c470e7b1fb8a89a4253ce69a0a465df82d94be47b3ca688b9452ad09c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:32 GMT
ADD file:de33fda50a142403e842620d20bc4404e66fc4ace16edc6946c4539e8a797458 in / 
# Thu, 17 Dec 2020 00:38:32 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 02:07:15 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 17 Dec 2020 02:07:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 02:07:16 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Feb 2021 04:22:22 GMT
ENV GOLANG_VERSION=1.15.8
# Fri, 05 Feb 2021 04:26:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.8.src.tar.gz'; 	sha256='540c0ab7781084d124991321ed1458e479982de94454a98afab6acadf38497c2'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 05 Feb 2021 04:26:40 GMT
ENV GOPATH=/go
# Fri, 05 Feb 2021 04:26:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Feb 2021 04:26:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 05 Feb 2021 04:26:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:455793c72b878001f0905634ed52a2524ba51796e7377bf00683a85123f7dce9`  
		Last Modified: Thu, 17 Dec 2020 00:39:18 GMT  
		Size: 2.8 MB (2794130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40840432391b9874ed7a9993a624f9f0a51b79928c8c8b9fe7e847802e39bb9e`  
		Last Modified: Thu, 17 Dec 2020 02:21:49 GMT  
		Size: 281.3 KB (281318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcd07ee69985a1d4a6d371a2c38b73690408d26fa31258f2301df6973fa4035`  
		Last Modified: Thu, 17 Dec 2020 02:21:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3553f7641285887df0260515ea19f5e459f9a412fe7bbd930203a99c51374`  
		Last Modified: Fri, 05 Feb 2021 04:46:04 GMT  
		Size: 105.4 MB (105385516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d940073ad689c08ce5cd5e5c14c142ac94ebc5c6d94eb8ccdca9099396df2e8a`  
		Last Modified: Fri, 05 Feb 2021 04:45:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.12` - linux; ppc64le

```console
$ docker pull golang@sha256:03d6b85fc49387337f23b0ea5ee08e81ef1019c3b8ea856004ce9d4258834b2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102576257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35ecc7a195e8a35d5393a31e6d0710a6dee5a7575e98cd451853d67571aebaa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:20:42 GMT
ADD file:0a38c9b4955f8faa79627c166fca80ef342e443a16ce2925a30eeae317bbd786 in / 
# Thu, 17 Dec 2020 00:20:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 08:14:01 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 17 Dec 2020 08:14:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 08:14:19 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:21:20 GMT
ENV GOLANG_VERSION=1.16
# Wed, 17 Feb 2021 01:23:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='softfloat' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 	sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 17 Feb 2021 01:24:09 GMT
ENV GOPATH=/go
# Wed, 17 Feb 2021 01:24:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:24:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 17 Feb 2021 01:24:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a9d343b7bcc225fe7ac17d96a81329510ab7f31a50472311cafe7168d3107317`  
		Last Modified: Thu, 17 Dec 2020 00:21:33 GMT  
		Size: 2.8 MB (2805226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf091f0415d5be50d1bb78d60eea983d45860f308d7b3a18cc9a3a2329bd7a2`  
		Last Modified: Thu, 17 Dec 2020 08:24:07 GMT  
		Size: 283.2 KB (283199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433009a251a58d325f4a615654b8f7c1aa06636266398f82829b79cd2d7cca18`  
		Last Modified: Thu, 17 Dec 2020 08:24:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ccb626463947ee1b496964c6adecf1cd1adf67cf60aa93500e53c1aa2822a4`  
		Last Modified: Wed, 17 Feb 2021 01:27:22 GMT  
		Size: 99.5 MB (99487522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c51574b666fa7a9f51e3eb134c3015a6e58abc256e08454c5f08f3803db82c`  
		Last Modified: Wed, 17 Feb 2021 01:27:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:alpine3.12` - linux; s390x

```console
$ docker pull golang@sha256:3f16237031a964d8a02802078c90081e0e3bf8ef4186e402aafec2da52393c91
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107662255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9df116347ab83e6a24e7e4137554f8962f9beaeae24f905d82d03e69678dc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 16 Dec 2020 23:41:37 GMT
ADD file:3ad3856d165e8760af85574a8ffa75ca44b7e1b97b64d1d6d4608445efa4b860 in / 
# Wed, 16 Dec 2020 23:41:37 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:33:00 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 17 Dec 2020 01:33:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Dec 2020 01:33:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:43:25 GMT
ENV GOLANG_VERSION=1.16
# Wed, 17 Feb 2021 01:44:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='softfloat' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 	sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 17 Feb 2021 01:44:48 GMT
ENV GOPATH=/go
# Wed, 17 Feb 2021 01:44:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:44:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 17 Feb 2021 01:44:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ee52640a49e15b8b7c8edb66c2d048b26abdee8d828d6e5ef4e10a28cb15a84f`  
		Last Modified: Wed, 16 Dec 2020 23:42:15 GMT  
		Size: 2.6 MB (2567018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa6a14f4067d7797fd5cfb87803df1ad2a3d7625d0b843e97d16cb7603123a7`  
		Last Modified: Thu, 17 Dec 2020 01:41:19 GMT  
		Size: 281.3 KB (281328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb7c9b3bde5c297668741ef40758508b43d424457fdbd8fcf1feb93e32b22f6`  
		Last Modified: Thu, 17 Dec 2020 01:41:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8834d59946096bc9b4f5ee953481cea12f8bcc050066852cc52794b7e8ab69`  
		Last Modified: Wed, 17 Feb 2021 01:46:40 GMT  
		Size: 104.8 MB (104813599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09861120977e407d4884d02482fc4f1a8baa3b9ddbde07039382e7200ad0c9d0`  
		Last Modified: Wed, 17 Feb 2021 01:46:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
