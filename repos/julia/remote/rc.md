## `julia:rc`

```console
$ docker pull julia@sha256:5c703c39886dae64ece22c75c0089e7aa776f0d61c7e40efa0568a2eabd3ef1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:7877eae88f51a50344c0163b9bbf66bf172aafb1f886fe558c12a55a51a26780
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180380190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962d9af977135081e45a79ed327316679788673c0bee136703122b0ca4588997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:02:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 11 Jan 2023 06:02:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:02:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 11 Jan 2023 06:02:56 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Wed, 11 Jan 2023 06:03:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-beta2-linux-x86_64.tar.gz'; 			sha256='72c0bfaa457784c83495e9da3ab706ed5053ee4d287472e03ff869d8eb72e0ee'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-beta2-linux-aarch64.tar.gz'; 			sha256='1ee292e33cc777c781d382c46521bc479941510ce4934271e7ca7e124150922a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-beta2-linux-i686.tar.gz'; 			sha256='1d900a852661d2a1b19287d12b689ee580709ba46f60eb62e6146ed8a38f772d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 11 Jan 2023 06:03:15 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 11 Jan 2023 06:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:03:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fa56be37265448a2b510f943c9ac54b9a0beaa493933cc3ef983e8b3cec234`  
		Last Modified: Wed, 11 Jan 2023 06:06:08 GMT  
		Size: 2.4 MB (2426594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7120db784a973dc2a601d8ebf765b34dfd04f4e6f5bcba3fbfe090f52f475e`  
		Last Modified: Wed, 11 Jan 2023 06:06:32 GMT  
		Size: 146.6 MB (146556253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbad9c33ca481a51d63854974c6b58e61bc24da0b0b8da13e502da1e94fe7f12`  
		Last Modified: Wed, 11 Jan 2023 06:06:08 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3751c5b59bad57988b92dac4dc7f4a81bacfa4e507e679c19a60cb297af8af38
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173069590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b5a464f6f90bffc5e4413653d97acd3ba026ae64b2dbeff8cfa9e59ed4e878`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 05:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 05:34:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 11 Jan 2023 05:34:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 05:34:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 11 Jan 2023 05:34:35 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Wed, 11 Jan 2023 05:34:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-beta2-linux-x86_64.tar.gz'; 			sha256='72c0bfaa457784c83495e9da3ab706ed5053ee4d287472e03ff869d8eb72e0ee'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-beta2-linux-aarch64.tar.gz'; 			sha256='1ee292e33cc777c781d382c46521bc479941510ce4934271e7ca7e124150922a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-beta2-linux-i686.tar.gz'; 			sha256='1d900a852661d2a1b19287d12b689ee580709ba46f60eb62e6146ed8a38f772d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 11 Jan 2023 05:34:58 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 11 Jan 2023 05:34:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Jan 2023 05:34:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33ec9f0d04deca261a5c5b9ffc666a96675fc51615950205808fe2f6549879c`  
		Last Modified: Wed, 11 Jan 2023 05:37:21 GMT  
		Size: 2.4 MB (2414271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1712d6c2d97cb3ae3edfe749b9ebbc42915baaaee78f1ace47856fd5e1fa6a`  
		Last Modified: Wed, 11 Jan 2023 05:37:38 GMT  
		Size: 140.6 MB (140610130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1563b479580cf0e40d2ba037ed53b8a976f38348df3d3549e8b3406e2776fd14`  
		Last Modified: Wed, 11 Jan 2023 05:37:20 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:4ad186ef1ab7348482c9b55e96cc34d60dd91aaa696531ab885ff3d2ddca0aaa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178750883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c145c60f05fe9c34c945b5ef74cac0f3bb1b978bea0e73ba882fe76bce8b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 11 Jan 2023 03:16:08 GMT
ADD file:68afc7c49a947a9fb253ffeba9950cdc39e241f8a5cf0133043cfc612447f597 in / 
# Wed, 11 Jan 2023 03:16:08 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 05:41:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 05:41:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 11 Jan 2023 05:41:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 05:41:52 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 11 Jan 2023 05:41:53 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Wed, 11 Jan 2023 05:42:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-beta2-linux-x86_64.tar.gz'; 			sha256='72c0bfaa457784c83495e9da3ab706ed5053ee4d287472e03ff869d8eb72e0ee'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-beta2-linux-aarch64.tar.gz'; 			sha256='1ee292e33cc777c781d382c46521bc479941510ce4934271e7ca7e124150922a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-beta2-linux-i686.tar.gz'; 			sha256='1d900a852661d2a1b19287d12b689ee580709ba46f60eb62e6146ed8a38f772d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 11 Jan 2023 05:42:19 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 11 Jan 2023 05:42:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Jan 2023 05:42:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:165165b78fad597abd0883f40adcaa0edcfe981a358deea181323680a07b7011`  
		Last Modified: Wed, 11 Jan 2023 03:22:01 GMT  
		Size: 32.4 MB (32375738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33635ddeb839f7e404118d0482fc8b3e7a90a11fb654de2bf61a000fe717928`  
		Last Modified: Wed, 11 Jan 2023 05:45:47 GMT  
		Size: 2.5 MB (2531793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a379930db4f178569a0eb2cb3ae21f9dfee31333890b3a6b56ee38d28520dfaa`  
		Last Modified: Wed, 11 Jan 2023 05:46:06 GMT  
		Size: 143.8 MB (143842979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d0620bfb0620a7b85f9b1bb38034c82951363a4d693b35978a7a5782e8ff7a`  
		Last Modified: Wed, 11 Jan 2023 05:45:46 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.1487; amd64

```console
$ docker pull julia@sha256:fa33d75a48fee051a892dde0e7ade1e9b7894d252254b54f159f0f0eacc4227a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1546596895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19db9f001c1dd1d2f3a4a231ab5a33252574940d42b0f072c26c3d799bd2b55`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 07:13:24 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Thu, 12 Jan 2023 07:13:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-beta2-win64.exe
# Thu, 12 Jan 2023 07:13:26 GMT
ENV JULIA_SHA256=b651d54e41243fba9b979d4d8c5d6f770030c0a8089062d2fe74638c3e736cec
# Thu, 12 Jan 2023 07:14:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 12 Jan 2023 07:14:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1cc83ed1fe1e9a39e2b1300ab5ef92c59d9e248b41af124ce06eb70b23974d`  
		Last Modified: Thu, 12 Jan 2023 07:25:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef41bb551747249ab2252d713344c3827c9f76f9f0bf642feda9b505e5eb9c1`  
		Last Modified: Thu, 12 Jan 2023 07:25:40 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef270d5c7611678dff62c98090654c7c8294118b8e0dfe569aba8680e89c52ce`  
		Last Modified: Thu, 12 Jan 2023 07:25:40 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e995eb0836582aee23107116979e32d13a4f24f84af276b3b1113a48786a19`  
		Last Modified: Thu, 12 Jan 2023 07:26:20 GMT  
		Size: 160.6 MB (160560875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d02e666c61d90d4bac51be3286e736ee2681fc5bb338806d96524004bcdb5e8`  
		Last Modified: Thu, 12 Jan 2023 07:25:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.3887; amd64

```console
$ docker pull julia@sha256:47911d13475fc0db55fe1d7c60d2d628d56a8c2a240a1b52b8ae423a609d1b77
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1868249266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f3f84644abe5bd93322cf26c288d8ba682048f99d8b3bfb95053a1063bfcd0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 07:15:08 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Thu, 12 Jan 2023 07:15:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-beta2-win64.exe
# Thu, 12 Jan 2023 07:15:11 GMT
ENV JULIA_SHA256=b651d54e41243fba9b979d4d8c5d6f770030c0a8089062d2fe74638c3e736cec
# Thu, 12 Jan 2023 07:16:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 12 Jan 2023 07:16:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3957efb289f7c193e18ab4ed3d195f9277d9dc5325b4890f0d3fb2ba90de749`  
		Last Modified: Thu, 12 Jan 2023 07:26:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a2ab9e48d3ae1a36885e7d1767ce3b0f7e53ec07a35fdb9009e104263dea89`  
		Last Modified: Thu, 12 Jan 2023 07:26:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68f44bc6ea14080bb7c9d96ffdd82dd68378b610d7f7cf36abf49eaa682b424`  
		Last Modified: Thu, 12 Jan 2023 07:26:31 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ab305a53aa36787e83fba8a33ac96bb0ae1a5d9a4de85cafdbc11cdfdda929`  
		Last Modified: Thu, 12 Jan 2023 07:27:12 GMT  
		Size: 160.3 MB (160298587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e1278496cf78a05fadfca7476c15102fff9865ec8bedb38cb54490043ad6bf`  
		Last Modified: Thu, 12 Jan 2023 07:26:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
