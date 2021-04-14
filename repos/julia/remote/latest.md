## `julia:latest`

```console
$ docker pull julia@sha256:c91732fcb8729437f279b8346b63bf914aa45d86bd025dab694a70eae324affb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:ced2706a015ca51638dbaea44e52a427122401f428a4ef99a33aa26922149242
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152690810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b007b680bbb4418775a5f6055036efe3e37d29b7a9f67d793b990ddaa291cba9`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:55:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 10 Apr 2021 06:55:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 06:55:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 10 Apr 2021 06:55:19 GMT
ENV JULIA_VERSION=1.6.0
# Sat, 10 Apr 2021 06:55:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='463b71dc70ca7094c0e0fd6d55d130051a7901e8dec5eb44d6002c57d1bd8585' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0f496972d26cea88151204d03e6bd87702aa1ff983de3b1e4f320c48ef67325f' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='601fea2ece89df4398146d077ee456a9abe0c9d2f19c5fc22be1f01c77949777' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='594639c9824f8dfb26074e875b27d7ed6c354d77a89469acbbe03e819021cb57' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 10 Apr 2021 06:55:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113f91229f9c8886c99154152d2b89193390ef02de463be9079d60a98c9b9934`  
		Last Modified: Sat, 10 Apr 2021 06:57:57 GMT  
		Size: 4.5 MB (4457997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2af2149ee7023dab04332294630ca344b80493fb5c424a5bd99945821802656`  
		Last Modified: Sat, 10 Apr 2021 06:58:21 GMT  
		Size: 121.1 MB (121093440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:504b4ead938fdffcd8cdd6539456c457ba3b891df2b26f685cd2b47620d3ab7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145220638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f05330593a4081e8266903b13648b882c19eeb9650eb6000bc942e5fa256de`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:25 GMT
ADD file:b24da7eb23eeae04e00d0e45da29a89fe8f992e8dcf4ba482afb907b8015b7bf in / 
# Sat, 10 Apr 2021 00:41:28 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 04:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 04:44:44 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 10 Apr 2021 04:44:44 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 04:44:45 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 10 Apr 2021 04:44:46 GMT
ENV JULIA_VERSION=1.6.0
# Sat, 10 Apr 2021 04:45:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='463b71dc70ca7094c0e0fd6d55d130051a7901e8dec5eb44d6002c57d1bd8585' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0f496972d26cea88151204d03e6bd87702aa1ff983de3b1e4f320c48ef67325f' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='601fea2ece89df4398146d077ee456a9abe0c9d2f19c5fc22be1f01c77949777' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='594639c9824f8dfb26074e875b27d7ed6c354d77a89469acbbe03e819021cb57' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 10 Apr 2021 04:45:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:15cb40b9c4df1a06940dc2a154c3be46844241235c1a091afa70da0ee2dc811a`  
		Last Modified: Sat, 10 Apr 2021 00:47:53 GMT  
		Size: 25.9 MB (25904582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50efa104be575ecdac5e5c9a088c46c41a22ab286646b5831164ef61a3f0799e`  
		Last Modified: Sat, 10 Apr 2021 04:47:21 GMT  
		Size: 4.3 MB (4338429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3002f5cc7df548d5c1a0594364c31c703b5919154e07da49217eb7e7ced229`  
		Last Modified: Sat, 10 Apr 2021 04:47:51 GMT  
		Size: 115.0 MB (114977627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:8860e2e536cf8dbb6c9b96f9ebab3e5f6315130cdeed10e4ef77bece99061439
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151193023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb80343567a9afba870e14691980e47bf7c2ef642966c9f2cf923f6d3f2e2b99`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 10 Apr 2021 00:39:42 GMT
ADD file:8885d4d13678543780bb04ba14b621179665f7951d5b261036a7092df9b376e7 in / 
# Sat, 10 Apr 2021 00:39:43 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 15:29:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:29:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 10 Apr 2021 15:29:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 15:29:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 10 Apr 2021 15:29:13 GMT
ENV JULIA_VERSION=1.6.0
# Sat, 10 Apr 2021 15:29:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='463b71dc70ca7094c0e0fd6d55d130051a7901e8dec5eb44d6002c57d1bd8585' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0f496972d26cea88151204d03e6bd87702aa1ff983de3b1e4f320c48ef67325f' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='601fea2ece89df4398146d077ee456a9abe0c9d2f19c5fc22be1f01c77949777' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='594639c9824f8dfb26074e875b27d7ed6c354d77a89469acbbe03e819021cb57' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 10 Apr 2021 15:29:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7cc57a8772e5e479618650dfa70f315b474d3f205d04bde7f602f469c1928d84`  
		Last Modified: Sat, 10 Apr 2021 00:46:07 GMT  
		Size: 27.8 MB (27788987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a736f834e1ba502d6c1a7780d13032b1d8d992c44ecefa53d1c9afb4019e1d69`  
		Last Modified: Sat, 10 Apr 2021 15:31:38 GMT  
		Size: 4.6 MB (4610587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df647124d1fb1e23465cfe5d5660cef59f2a816761c2f549b101471c1fccde7`  
		Last Modified: Sat, 10 Apr 2021 15:32:08 GMT  
		Size: 118.8 MB (118793449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:ce7e5c45ada2add4fedf99f6b7ec9706081d59cc1c9a745fb1bb2e28e9b18f9a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141894412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb37ca87e77ca11a23188667ce70dfe65d1ffcc8bc910041c479be6545c1d37c`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 10 Apr 2021 01:26:49 GMT
ADD file:ab87d4854aa8628ce8f4e603c0496499f6f28c3d2525ace782c7369691dafc8c in / 
# Sat, 10 Apr 2021 01:26:56 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 14:44:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 14:44:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 10 Apr 2021 14:44:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 14:44:33 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 10 Apr 2021 14:44:40 GMT
ENV JULIA_VERSION=1.6.0
# Sat, 10 Apr 2021 14:46:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='463b71dc70ca7094c0e0fd6d55d130051a7901e8dec5eb44d6002c57d1bd8585' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0f496972d26cea88151204d03e6bd87702aa1ff983de3b1e4f320c48ef67325f' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='601fea2ece89df4398146d077ee456a9abe0c9d2f19c5fc22be1f01c77949777' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='594639c9824f8dfb26074e875b27d7ed6c354d77a89469acbbe03e819021cb57' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 10 Apr 2021 14:46:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3e1e599482ca47095f85e429b346b76375aa85015ddcca050e85c2a8b1fdda9c`  
		Last Modified: Sat, 10 Apr 2021 01:33:57 GMT  
		Size: 30.5 MB (30545933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de5cbe49ae47809605d7676cf919113b9fcd0039eeeb96d8a990491cb6e266e`  
		Last Modified: Sat, 10 Apr 2021 14:47:08 GMT  
		Size: 4.9 MB (4853557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8253160fa70f9b07956cf3a6c80f0a75f90129e3ddbffe493bd200709ca2cc31`  
		Last Modified: Sat, 10 Apr 2021 14:47:28 GMT  
		Size: 106.5 MB (106494922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull julia@sha256:1bf7a664c6a714b8fb3140a9eac00e3e82dca8f2300d282f0392027718c51cc7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2607759000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7808e910e53aae2d433b9ccaa68600072e7037e1e923c051c7a71d218f988668`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 15:45:04 GMT
ENV JULIA_VERSION=1.6.0
# Wed, 14 Apr 2021 15:45:05 GMT
ENV JULIA_SHA256=0c1f5cfe5d4ffb3505282a46169d85f31666217d3ada4831a4a5d7f2b981f0cc
# Wed, 14 Apr 2021 15:46:59 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 14 Apr 2021 15:47:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312646c4957279e469b50aedf3757f4a11e29212a3099befb751d88ac905c617`  
		Last Modified: Wed, 14 Apr 2021 15:55:34 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c002ff82d3e0d7b6882c459315c8e7672c3d80b175767f3f61334fc65305cc70`  
		Last Modified: Wed, 14 Apr 2021 15:55:34 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f6db741c9bb768c1f002c2349188ece3a2deafa9cbffff2b5a2ffe8602b3f`  
		Last Modified: Wed, 14 Apr 2021 15:58:08 GMT  
		Size: 138.0 MB (137999503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915a66b78a7f9d3da86afa694097ede83e89e3d92f0a07bd6b5e6acef3ee7088`  
		Last Modified: Wed, 14 Apr 2021 15:55:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.14393.4350; amd64

```console
$ docker pull julia@sha256:fd99cb35e2eb00e0812acc8b219351e95c524be755bd34f53885de8f175b2291
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5937951731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff83a096e2947bc7bf5d147d58d47455a2504b73c1c12ed11d25080833169762`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 15:47:17 GMT
ENV JULIA_VERSION=1.6.0
# Wed, 14 Apr 2021 15:47:18 GMT
ENV JULIA_SHA256=0c1f5cfe5d4ffb3505282a46169d85f31666217d3ada4831a4a5d7f2b981f0cc
# Wed, 14 Apr 2021 15:50:00 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 14 Apr 2021 15:50:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3c4712b14d17e1058564ac4c2df894bb4dcfbee6cb098104ce094701d507f0`  
		Last Modified: Wed, 14 Apr 2021 15:58:31 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7708d29f19c8525171582e0b94e45b198fc6cad762beb7141f3669fe158c825e`  
		Last Modified: Wed, 14 Apr 2021 15:58:31 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ca715cc74a53feb8160ae6de9a6890e87711c8b5e55d76957c0ef369c20ad`  
		Last Modified: Wed, 14 Apr 2021 15:59:04 GMT  
		Size: 143.1 MB (143062253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af004a4a663d68ae5095fe560d874a169dbe2f3f38a1674b34754e2d7b8e36b2`  
		Last Modified: Wed, 14 Apr 2021 15:58:30 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
