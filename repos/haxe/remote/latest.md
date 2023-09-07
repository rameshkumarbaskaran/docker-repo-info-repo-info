## `haxe:latest`

```console
$ docker pull haxe@sha256:62559e9848cab5cba78dec72ba49ab3ef71d093a61db898c48115db220cbe73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:5775d43abd94c79992ce3f386248ad627b539d01dc0a463d6b36fcfda4e0188d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140028997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180e6864620b3b6c6a28976a362c89a72233024a9f48d93cd625f6950e2c54ce`
-	Default Command: `["haxe"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:57:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:58:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 20:13:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 20:13:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 20:13:45 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 07 Sep 2023 20:15:04 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Thu, 07 Sep 2023 20:15:05 GMT
ENV HAXE_VERSION=4.3.1
# Thu, 07 Sep 2023 20:15:05 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Thu, 07 Sep 2023 20:17:55 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.3.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Thu, 07 Sep 2023 20:17:55 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d190df514e96e82a9048dff1406b65e853dbdfbfc0d8474b85ef6bf37bfea62a`  
		Last Modified: Thu, 07 Sep 2023 03:05:52 GMT  
		Size: 15.8 MB (15760386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b939be1a16917d966978485a9a71e7b85c49562a3c586f5e4a1f29a4e37eea`  
		Last Modified: Thu, 07 Sep 2023 03:06:08 GMT  
		Size: 54.6 MB (54584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e083df299c42de533d9bffb7e165f6a81557098e053bf856892a714bda6a68af`  
		Last Modified: Thu, 07 Sep 2023 20:55:04 GMT  
		Size: 1.4 MB (1368849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a65024e549046886d1d8366acfdf99cd9dcf685f5bae51af19b644353720f62`  
		Last Modified: Thu, 07 Sep 2023 20:55:04 GMT  
		Size: 1.4 MB (1447525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e57399840bb66ccd8814c11bafc5744d9578db45dcaa2602f7ba59f6c260a6`  
		Last Modified: Thu, 07 Sep 2023 20:55:06 GMT  
		Size: 11.8 MB (11811014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:1bd1fd5de9d1f226bf328629670e28a5ab64b4d7814342dfda04cdb380c842db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129481979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c469e813cd8ac09f2ea7e058d911458c83260f302982908e21c13b4493c290`
-	Default Command: `["haxe"]`

```dockerfile
# Thu, 07 Sep 2023 00:57:59 GMT
ADD file:931564fb3c8ea78b763a6b98f2739bb7c6a38484122c560a87c7166b7d45c5e6 in / 
# Thu, 07 Sep 2023 00:58:00 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:35:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:36:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:35:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 19:35:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:35:53 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 07 Sep 2023 19:37:23 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Thu, 07 Sep 2023 19:37:23 GMT
ENV HAXE_VERSION=4.3.1
# Thu, 07 Sep 2023 19:37:23 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Thu, 07 Sep 2023 19:40:49 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.3.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Thu, 07 Sep 2023 19:40:50 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:5826e0d927336e7231f9d05ec48f075045fb51f9b3f16f1e20972f2a3634d102`  
		Last Modified: Thu, 07 Sep 2023 01:02:50 GMT  
		Size: 50.2 MB (50219233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a3e40045b60de87bd316fc81bad3ca642a31ef598e190c09841e07788e602b`  
		Last Modified: Thu, 07 Sep 2023 01:46:10 GMT  
		Size: 14.9 MB (14868694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5b825bbf3a3a8da6c02d2c0b4fb980ffaddcae8ddf4c4f56ac13548697fddc`  
		Last Modified: Thu, 07 Sep 2023 01:46:28 GMT  
		Size: 50.4 MB (50355718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ea62cff14dafe9eeaf7888a17ad677f8c9f4cea19ed2c23ae0c91de3cb70f`  
		Last Modified: Thu, 07 Sep 2023 20:23:50 GMT  
		Size: 1.3 MB (1281934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ecf618d0f351f09cbda68b54b18b84b43ba651568420782fa2e6ca0fc2063`  
		Last Modified: Thu, 07 Sep 2023 20:23:50 GMT  
		Size: 1.4 MB (1387944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41d0cd27ba8a147ebe8b2cb39152131dc82dd69300e743199904a266b419d8a`  
		Last Modified: Thu, 07 Sep 2023 20:23:53 GMT  
		Size: 11.4 MB (11368456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:812fe110329c6d41bd9fb68f3965a921d2ee0e9066ac2fbe6248e99c11db8293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140395799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692dedfb67304cea42a8bdbb1575b9dc3d41edd84d438dc4c68c32c3336c2272`
-	Default Command: `["haxe"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:52:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:52:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 16:21:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 16:21:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 16:21:08 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 07 Sep 2023 16:22:22 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Thu, 07 Sep 2023 16:22:22 GMT
ENV HAXE_VERSION=4.3.1
# Thu, 07 Sep 2023 16:22:22 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Thu, 07 Sep 2023 16:25:00 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.3.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Thu, 07 Sep 2023 16:25:00 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b3f92a99188e47f7b0b8d38aff11fd0ad90510e0d26506aec007d24fe539b6`  
		Last Modified: Thu, 07 Sep 2023 07:00:19 GMT  
		Size: 15.7 MB (15746623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbd1eb48e6c614e3e3767ae9ba92cd3104dc0df1c1cf83b5211c232c4962473`  
		Last Modified: Thu, 07 Sep 2023 07:00:33 GMT  
		Size: 54.7 MB (54676071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf5bfa3fcf368365a5d9699a546c61e293daef630efb0bb4f53dbe463f447cf`  
		Last Modified: Thu, 07 Sep 2023 16:56:52 GMT  
		Size: 1.4 MB (1359607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8fc0789a85bde87b352e643e8ec12f771d6909b72c9e8d99c041b414f73ba2`  
		Last Modified: Thu, 07 Sep 2023 16:56:52 GMT  
		Size: 1.4 MB (1438388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c42ea624d0fa447c87ff61824b2552c5c98b27c7ad470b772863c7e447cd12`  
		Last Modified: Thu, 07 Sep 2023 16:56:54 GMT  
		Size: 13.5 MB (13470394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.1906; amd64

```console
$ docker pull haxe@sha256:185175f3fa5194b728b019c6c9a7233b29a2de8cae5008c44c82017d8a951f60
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1823679222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f742b7dbd3ec15fd07ad5ba90221a01d536ec52494f01bb083ea42fa77a2d22`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Thu, 10 Aug 2023 01:08:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Aug 2023 03:27:19 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Thu, 10 Aug 2023 03:27:19 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Thu, 10 Aug 2023 03:27:21 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Thu, 10 Aug 2023 03:27:22 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Thu, 10 Aug 2023 03:27:22 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Thu, 10 Aug 2023 03:27:45 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 03:29:00 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 03:29:20 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Thu, 10 Aug 2023 03:29:21 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 10 Aug 2023 03:29:53 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 03:29:53 GMT
ENV HAXE_VERSION=4.3.1
# Thu, 10 Aug 2023 03:33:57 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.1/haxe-4.3.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (8f77bf1dc3fae88b3174e311c60e69ab25c02093a0801bd3e49b28609f465e1e) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '8f77bf1dc3fae88b3174e311c60e69ab25c02093a0801bd3e49b28609f465e1e') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 03:34:18 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Thu, 10 Aug 2023 03:34:19 GMT
ENV HOMEDRIVE=C:
# Thu, 10 Aug 2023 03:34:40 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 03:35:05 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Thu, 10 Aug 2023 03:35:06 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b1b41cab0d4b78c8daa50728be89bc3c25ded051cc1e654b316623692507f1`  
		Last Modified: Thu, 10 Aug 2023 01:55:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1841c3478af952514ce4dae0c44728debc2c0f0d4abd2c37bc51ff926b65c624`  
		Last Modified: Thu, 10 Aug 2023 05:16:41 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbf1b5e58a702ce70f9e7efaaf8825b067ff6a28e7ceaee9eede71524738c15`  
		Last Modified: Thu, 10 Aug 2023 05:16:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4f4753e06082f4cf963f01f42c87cacb9c8cc245a3650024395dd21bdb8e6`  
		Last Modified: Thu, 10 Aug 2023 05:16:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63163c782ff51a90271d25b061cf43233a06e41087231cc54fc9ec2fb1603b0`  
		Last Modified: Thu, 10 Aug 2023 05:16:39 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd94b10c7451ed3c1a12f1216e54c8d9744d6f433937bb3f5ce6eb3b2e970a9d`  
		Last Modified: Thu, 10 Aug 2023 05:16:39 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6108818dafb0e1679fb799995c9bdc0c162fb53e19fd80c3e910b4f4d2755367`  
		Last Modified: Thu, 10 Aug 2023 05:16:39 GMT  
		Size: 451.2 KB (451157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878a0003ebe9775d2f296c733a9c3bec23a7a30e291b1898c5a9d2dd0ad64a9b`  
		Last Modified: Thu, 10 Aug 2023 05:16:40 GMT  
		Size: 12.9 MB (12862410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768b526d8f7114fbddce148e3b420af79d543e9b75c2b2b433b5ff7452b3754`  
		Last Modified: Thu, 10 Aug 2023 05:16:37 GMT  
		Size: 293.4 KB (293400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae8a3ab99a2771fadabd2e8844394491c228ed6dd40a29ddb8beabcb27ba225`  
		Last Modified: Thu, 10 Aug 2023 05:16:36 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4f5d2b7416c2bfaab7d3d22c413028c715f5f38036cd4e6848a3a2f099711e`  
		Last Modified: Thu, 10 Aug 2023 05:16:37 GMT  
		Size: 2.1 MB (2120646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b4edea733d901f01ccca930b2431971597967374248c61f22e48066dc5e7a1`  
		Last Modified: Thu, 10 Aug 2023 05:16:36 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ad10153d3a094edf9c2f7f4e05a466b410cf60040e7cb716c3419118f5712`  
		Last Modified: Thu, 10 Aug 2023 05:16:40 GMT  
		Size: 9.6 MB (9562374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ca8b98c67ee4b23fedf7ae89771ad29ed14e05b84bc89fef39cd0411f71423`  
		Last Modified: Thu, 10 Aug 2023 05:16:34 GMT  
		Size: 327.4 KB (327434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8203516f182f8078b154b73db500c8c6634ce31f8eea7d9ed0912c0e3286b0`  
		Last Modified: Thu, 10 Aug 2023 05:16:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fb6934014743bfc3204a4f6473a0821fdf4c9c35d7481c6ef0888aeefdb66`  
		Last Modified: Thu, 10 Aug 2023 05:16:34 GMT  
		Size: 331.7 KB (331719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d4bb992fc8a538512275559375abc705aa5e2bd0ab6e9a55809444f3ffc28d`  
		Last Modified: Thu, 10 Aug 2023 05:16:34 GMT  
		Size: 352.2 KB (352242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babdf1072379067ffcf321eb63388d30d520363f65d1a8443204a331cf0de6af`  
		Last Modified: Thu, 10 Aug 2023 05:16:34 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.4737; amd64

```console
$ docker pull haxe@sha256:3fe6dd0c79f06331378893d69fd5c82b2fa603d879129ed51b1a64572c20825f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2026895199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a559c9fd75ddb87443d7a163f7f7c2008f17eada56636aeea816ee8c1e013cb`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Thu, 10 Aug 2023 01:11:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Aug 2023 03:35:19 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Thu, 10 Aug 2023 03:35:20 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Thu, 10 Aug 2023 03:35:20 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Thu, 10 Aug 2023 03:35:21 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Thu, 10 Aug 2023 03:35:22 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Thu, 10 Aug 2023 03:36:27 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 03:38:28 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 03:39:29 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Thu, 10 Aug 2023 03:39:30 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 10 Aug 2023 03:40:47 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 03:40:48 GMT
ENV HAXE_VERSION=4.3.1
# Thu, 10 Aug 2023 03:45:37 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.1/haxe-4.3.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (8f77bf1dc3fae88b3174e311c60e69ab25c02093a0801bd3e49b28609f465e1e) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '8f77bf1dc3fae88b3174e311c60e69ab25c02093a0801bd3e49b28609f465e1e') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 03:46:40 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Thu, 10 Aug 2023 03:46:40 GMT
ENV HOMEDRIVE=C:
# Thu, 10 Aug 2023 03:48:07 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 03:49:36 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Thu, 10 Aug 2023 03:49:37 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5180b8f5f7c2303ba89717cfa778a2173921ca7efdc058cfd6ed951c6d5ca3`  
		Last Modified: Thu, 10 Aug 2023 01:57:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8a2f0252db32029a9b854d394505325edaafeca4dd21fe95acbf735a1b9e8c`  
		Last Modified: Thu, 10 Aug 2023 05:16:58 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a5d5e86f12ca902e8083511147e83de5859403011fc74e55854e154d84233f`  
		Last Modified: Thu, 10 Aug 2023 05:16:57 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb91de73a117847c7ca71917129026b4d8cce034f08afcaa72e1fae5553c9db`  
		Last Modified: Thu, 10 Aug 2023 05:16:58 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9b520ff44be02fd27ef798f9fca7e3498c660e422504e0014d2ea3a2ca000e`  
		Last Modified: Thu, 10 Aug 2023 05:16:56 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf9fa8941ce4667402e4164c730510082a2957794e3c2b1b465ed6540cf28f7`  
		Last Modified: Thu, 10 Aug 2023 05:16:55 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9797be130477979fc64f985045fb8f561862a5cf31ef77ab61c27bc8b99ab4`  
		Last Modified: Thu, 10 Aug 2023 05:16:56 GMT  
		Size: 247.4 KB (247355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0bc82b06fa64991c0e336753fb461890411f743620c1bd23dd17116c948a4f`  
		Last Modified: Thu, 10 Aug 2023 05:16:57 GMT  
		Size: 13.1 MB (13058759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e4929a66ead53cf919fc5400ad2fdb8d8ce9be6db3a55d8ace67d84e7ef313`  
		Last Modified: Thu, 10 Aug 2023 05:16:53 GMT  
		Size: 213.6 KB (213642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5d9211fb61888759a4bd9b4ee378dba6a436f8e910bae19e46a838eed1b1e1`  
		Last Modified: Thu, 10 Aug 2023 05:16:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ccdfba56588574d13d4a198cdd4fbc10b2894ab9a88139ba7db3190158bc5`  
		Last Modified: Thu, 10 Aug 2023 05:16:54 GMT  
		Size: 2.1 MB (2113546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20777a4c9d2b2107c9ce9c07cb2d600077e9a4c85a460baab738d807fa6d95`  
		Last Modified: Thu, 10 Aug 2023 05:16:53 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec693e647b63d94cfe7206449b2092aea828185e5d3932b8dc298848a154cb4`  
		Last Modified: Thu, 10 Aug 2023 05:16:59 GMT  
		Size: 14.5 MB (14516796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7e8673a3efaf0818d81829cbdffbba7940d5481c96063afdbaf805fe197f33`  
		Last Modified: Thu, 10 Aug 2023 05:16:51 GMT  
		Size: 221.0 KB (220969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96974c8abdf5d5a5e4543df6ae6e942cb6a6c19d214a7d80e848040e802532fd`  
		Last Modified: Thu, 10 Aug 2023 05:16:51 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15775488c083bf073082581a61a18d5ef81ca6ba0771a0e413e0a32b0b7d94d5`  
		Last Modified: Thu, 10 Aug 2023 05:16:51 GMT  
		Size: 223.5 KB (223528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ccbeb2577f6c1176496036e44f8d06af004e5f01893dfc1d502bf7b2d850b8`  
		Last Modified: Thu, 10 Aug 2023 05:16:51 GMT  
		Size: 331.2 KB (331162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0536f74a500d488cbc72761e495015f8e84de16f6d9b6e7dedc030b3c4db5f8`  
		Last Modified: Thu, 10 Aug 2023 05:16:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
