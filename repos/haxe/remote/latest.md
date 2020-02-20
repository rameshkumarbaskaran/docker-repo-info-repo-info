## `haxe:latest`

```console
$ docker pull haxe@sha256:b0e8e8f13126f0d0bde7111d23aa338e4a61cbdf100ff0bdb8eb757b6618cc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1040; amd64
	-	windows version 10.0.14393.3506; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:c9ef17fa673f7268cb665b2135e82ee1dbe3753da5fdde7fd774963dadfe9f1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132061450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71251ffb5dbd980ea0081ebc88dfd4204c31fccd51c31c934395f8c2d90b7d5`
-	Default Command: `["haxe"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:a5ec219cbfc4e0c31e7df48cc51abd9a5b92754e15403b2ab726e25042041680 in / 
# Sat, 01 Feb 2020 17:20:39 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:18:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:19:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 00:19:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 14:11:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 14:11:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 14:11:55 GMT
ENV NEKO_VERSION=2.3.0
# Sun, 02 Feb 2020 14:13:13 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Sun, 02 Feb 2020 14:13:13 GMT
ENV HAXE_VERSION=4.0.5
# Sun, 02 Feb 2020 14:13:13 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Sun, 02 Feb 2020 14:15:57 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 			' 	&& git clone --recursive --depth 1 --branch 4.0.5 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 	&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Sun, 02 Feb 2020 14:15:57 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:dc65f448a2e2f2ea557e69ed9ac65aa8ac0e16f1bce68f90de910b4d5a2f1ba1`  
		Last Modified: Sat, 01 Feb 2020 17:26:04 GMT  
		Size: 50.4 MB (50379770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346ffb2b67d7b35729673ced818325ed0ea57284e69de67f8bbc48c2bf294716`  
		Last Modified: Sun, 02 Feb 2020 00:37:48 GMT  
		Size: 7.8 MB (7811673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea4ecac934f71d68d4f5edb171f6cff42588edfa3f70ba8709be56e321eeddc`  
		Last Modified: Sun, 02 Feb 2020 00:37:49 GMT  
		Size: 10.0 MB (9996251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac92ddf84b35dac36ef6632f8d5a0c9c2d7038f6018f2d4fa1be056d90bd366`  
		Last Modified: Sun, 02 Feb 2020 00:38:05 GMT  
		Size: 51.8 MB (51791113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01edb32150e60b7d7779f8830a9a0b41ca0b58d579de65b88651ba24f585ccd0`  
		Last Modified: Sun, 02 Feb 2020 14:57:26 GMT  
		Size: 1.3 MB (1310662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84da5a46b0492611c3c380f08fdb90e2022192037d975e0b48752fe501ef608a`  
		Last Modified: Sun, 02 Feb 2020 14:57:26 GMT  
		Size: 2.4 MB (2417291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f3ecdd88c1560338dd97e49b74a7263e87187e6407b7a091933b4cba8c6766`  
		Last Modified: Sun, 02 Feb 2020 14:57:28 GMT  
		Size: 8.4 MB (8354690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:c043f7d587a8c0a65996eb01967fde496bf9d6ec6395974da57cc1e9a5a99252
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121257409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07c4960daafb074fea2acb2697399d3bcbabf78c201e55289a8e8d09b7a84d0`
-	Default Command: `["haxe"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:06 GMT
ADD file:a57a312731f174c4b03031908ff95f49d7055d8c196439f0ed07ed9c4834d993 in / 
# Sat, 01 Feb 2020 17:00:08 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:00:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:01:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:38:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 13:38:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:38:17 GMT
ENV NEKO_VERSION=2.3.0
# Sun, 02 Feb 2020 13:41:26 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Sun, 02 Feb 2020 13:41:28 GMT
ENV HAXE_VERSION=4.0.5
# Sun, 02 Feb 2020 13:41:28 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Sun, 02 Feb 2020 13:49:18 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 			' 	&& git clone --recursive --depth 1 --branch 4.0.5 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 	&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Sun, 02 Feb 2020 13:49:19 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:9bbb41bca8c6254da5088d03354297b1309dc75c2ccc738416025f89709ae5ee`  
		Last Modified: Sat, 01 Feb 2020 17:07:28 GMT  
		Size: 45.9 MB (45859700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e4acdbc2ab88c89aa359fbab11429ea6d7bd93ea589a22c6bbb833ff82b93`  
		Last Modified: Sat, 01 Feb 2020 18:25:50 GMT  
		Size: 7.1 MB (7096223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6b4707a3c3aff9cb939fc058b869c5412e78c37e43eb0b653565460495537`  
		Last Modified: Sat, 01 Feb 2020 18:25:50 GMT  
		Size: 9.3 MB (9343278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e096c4fc8c629edca6da3ce5a9e95288512cb11e3d3d01a6e49078d19c2acca`  
		Last Modified: Sat, 01 Feb 2020 18:26:13 GMT  
		Size: 47.3 MB (47315591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b77f0351b9ec2d9a20055b0d19a04b8a3f10da89da18d6b883e3f2e11e422c`  
		Last Modified: Sun, 02 Feb 2020 14:24:06 GMT  
		Size: 1.2 MB (1232765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389864dff7a41a78f0fc78e18ab0b908d967def43e7f8cb422c8ab821f1e10f3`  
		Last Modified: Sun, 02 Feb 2020 14:24:06 GMT  
		Size: 2.4 MB (2357160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5badcbe028ef2950cbc8d359c7fec5b6c80f7121c75897845e26d940f330c47f`  
		Last Modified: Sun, 02 Feb 2020 14:24:09 GMT  
		Size: 8.1 MB (8052692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:473f88252aa9127d9de16fe21001f72ec285d7b8738444c4020ef0385a65ca39
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133002738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6c19075667412df9f5585de7472da04b384c71f35b6339403587ab28af8b8d`
-	Default Command: `["haxe"]`

```dockerfile
# Sat, 01 Feb 2020 16:40:50 GMT
ADD file:b423f4b0ed41dfe1334031fe9b21f7e1c88ccb031d7e8f2ff165d618323424d7 in / 
# Sat, 01 Feb 2020 16:40:53 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:18:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:18:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:19:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:49:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 13:49:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:49:16 GMT
ENV NEKO_VERSION=2.3.0
# Sun, 02 Feb 2020 13:53:07 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Sun, 02 Feb 2020 13:53:08 GMT
ENV HAXE_VERSION=4.0.5
# Sun, 02 Feb 2020 13:53:09 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Sun, 02 Feb 2020 13:59:39 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 			' 	&& git clone --recursive --depth 1 --branch 4.0.5 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 	&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Sun, 02 Feb 2020 13:59:41 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:bc03a7ced18fc43ea9523dfb256d2c3fbb835dc0bb54bdb7fd309edf936a87e7`  
		Last Modified: Sat, 01 Feb 2020 16:46:06 GMT  
		Size: 49.2 MB (49171687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9d528c1473d79c18b401d44ca06b9733d9c51a8699b98e8325c9de60b9739`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 7.7 MB (7680993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981400d5d268dc989681d5f308b7d2e381809f0bcc82429f443f7539cf6117ba`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 10.0 MB (9983754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b2d547b8bc79a444406e56d724fb7d961c953e7f2797de4f55b29abee5605f`  
		Last Modified: Sat, 01 Feb 2020 17:35:22 GMT  
		Size: 52.1 MB (52102938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd99e9408745cf82856ec1abbe20a3dedda929e1b7376e88d16b3a5e27caaca8`  
		Last Modified: Sun, 02 Feb 2020 14:29:31 GMT  
		Size: 1.3 MB (1301746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb6cfb94494ba636a6a75e7f9a6317ad0615d99f16085392d1d82fd06a6982`  
		Last Modified: Sun, 02 Feb 2020 14:29:31 GMT  
		Size: 2.4 MB (2414824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df38316350953f5e14ee837e54eb022168419622b8cd2f7192e774dec23520f`  
		Last Modified: Sun, 02 Feb 2020 14:29:35 GMT  
		Size: 10.3 MB (10346796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.1040; amd64

```console
$ docker pull haxe@sha256:25b6dcf10a1bf67b3d0eff585babeb725753d8929280d88ca5073666325c8257
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2258905837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e80c96bf027a1a8896a4c76750efb3039c32e11163fe9a36f272f279c73b443`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 05:10:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 06:31:53 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Thu, 20 Feb 2020 06:31:54 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Thu, 20 Feb 2020 06:31:55 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Thu, 20 Feb 2020 06:31:57 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Thu, 20 Feb 2020 06:31:58 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Thu, 20 Feb 2020 06:32:37 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2020 06:33:47 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 06:34:14 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Thu, 20 Feb 2020 06:34:15 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 20 Feb 2020 06:34:58 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 06:34:59 GMT
ENV HAXE_VERSION=4.0.5
# Thu, 20 Feb 2020 06:39:34 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.0.5/haxe-4.0.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (93130ae2b1083efbcd9b8911afe2ba00d5af995f016149fd7ec629fa439c6120) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '93130ae2b1083efbcd9b8911afe2ba00d5af995f016149fd7ec629fa439c6120') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 06:39:59 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Thu, 20 Feb 2020 06:40:01 GMT
ENV HOMEDRIVE=C:
# Thu, 20 Feb 2020 06:40:27 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2020 06:40:55 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org') >$null
# Thu, 20 Feb 2020 06:41:23 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://d1smpvufia21az.cloudfront.net') >$null
# Thu, 20 Feb 2020 06:41:24 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f20f5493f581bb667af03f7639273e01559818f9d7dfe81dd7e9dfef3af2e11`  
		Last Modified: Thu, 20 Feb 2020 05:16:53 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568ff83287666599ba80735a7bd66fd0065e2f4700a067ae27b7172c40b6750d`  
		Last Modified: Thu, 20 Feb 2020 09:05:13 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7af0bcb1f99091a5ccb0b330e583a0aed9af5e14e29e93ace9b59a9162fa165`  
		Last Modified: Thu, 20 Feb 2020 09:05:13 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a021aa6ab71763c9edb0ddd85f3d6e5b8f3f6a46a958881ab878ea592ae1b5c5`  
		Last Modified: Thu, 20 Feb 2020 09:05:11 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7e775e3dfbb38b94ac05538fa2a9e66d20b1db05acd458c2b74c4103097ee7`  
		Last Modified: Thu, 20 Feb 2020 09:05:10 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e98ecec6e06f29cc3e8e560e5ed08b76bac7f82b8ddc6b58fa60feefc775f2c`  
		Last Modified: Thu, 20 Feb 2020 09:05:09 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c27b0dd30bdbedb544970757619510c0dbad0c6c11f739e2008e7bb421e93d`  
		Last Modified: Thu, 20 Feb 2020 09:05:10 GMT  
		Size: 4.6 MB (4566164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab26769e719ea17c2c1f4b8a34e2b919743e523cdd780e09a66398df1073fb67`  
		Last Modified: Thu, 20 Feb 2020 09:05:11 GMT  
		Size: 12.9 MB (12898928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7718c3c8fe3969c9dc7831dfdc209cac0ea5c7636b8a5d4d25b738460b4dbe`  
		Last Modified: Thu, 20 Feb 2020 09:05:07 GMT  
		Size: 297.4 KB (297394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7d69d2476328dc02a68fc6d3f18f41bc77a3be1c646a977cf891de1254f2bd`  
		Last Modified: Thu, 20 Feb 2020 09:05:05 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8c5bfddbed7370210a9f80b7094673968059d6d81d5acc19f77fbdf41d8174`  
		Last Modified: Thu, 20 Feb 2020 09:05:05 GMT  
		Size: 2.1 MB (2125304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09d1fb478051dbf974a36beef0e0a5c6b54f9eb9751707c4b16320d5144acc`  
		Last Modified: Thu, 20 Feb 2020 09:05:04 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0311460bc32eaaac6c4e97c2df4710ffb7d20f8338e80bbc97fbd6600733b5`  
		Last Modified: Thu, 20 Feb 2020 09:05:28 GMT  
		Size: 7.2 MB (7158101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbf0f32de4b26c92b333e5fe40f835ca407e779ce06839bc6006348a155723`  
		Last Modified: Thu, 20 Feb 2020 09:05:03 GMT  
		Size: 322.3 KB (322302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d0899f2c643968dcb3d5df0e7a6753721d4511f4e806231c08308fd00bfb37`  
		Last Modified: Thu, 20 Feb 2020 09:05:00 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2d757c3e64360f884f3e8ff48c1bbe672d66d97c5c0ca20b38acc2e56d2b2`  
		Last Modified: Thu, 20 Feb 2020 09:05:01 GMT  
		Size: 325.7 KB (325707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29540ae7bc361228bb7eef24d8914cfaae36141e5527069db1bc55c3e65e5ec`  
		Last Modified: Thu, 20 Feb 2020 09:05:01 GMT  
		Size: 342.1 KB (342065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f000bfe7199e7fe24e9d8098e23b7e9f38ce862ff3dc585c28f2ce50980897a8`  
		Last Modified: Thu, 20 Feb 2020 09:05:01 GMT  
		Size: 354.1 KB (354054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990b88c584ac09abb0c2c5d1f5c1d81554c8304023359194e5d7e4c77c159cb5`  
		Last Modified: Thu, 20 Feb 2020 09:05:00 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.14393.3506; amd64

```console
$ docker pull haxe@sha256:55af6beabdc02ea3963bfa0c94cdc2832cda42dd2ef99cfcf37074789ef55020
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5805214965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46001826a27ba5c5893381d2c0ec8a1bf4264add9f9d43021db158bd867dc1b`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 06:41:45 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Thu, 20 Feb 2020 06:41:46 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Thu, 20 Feb 2020 06:41:47 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Thu, 20 Feb 2020 06:41:49 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Thu, 20 Feb 2020 06:41:50 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Thu, 20 Feb 2020 06:43:07 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2020 06:45:16 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 06:46:35 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Thu, 20 Feb 2020 06:46:37 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 20 Feb 2020 06:48:14 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 06:48:15 GMT
ENV HAXE_VERSION=4.0.5
# Thu, 20 Feb 2020 06:53:23 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.0.5/haxe-4.0.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (93130ae2b1083efbcd9b8911afe2ba00d5af995f016149fd7ec629fa439c6120) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '93130ae2b1083efbcd9b8911afe2ba00d5af995f016149fd7ec629fa439c6120') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 06:54:38 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Thu, 20 Feb 2020 06:54:40 GMT
ENV HOMEDRIVE=C:
# Thu, 20 Feb 2020 06:55:53 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2020 06:57:21 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org') >$null
# Thu, 20 Feb 2020 06:58:34 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://d1smpvufia21az.cloudfront.net') >$null
# Thu, 20 Feb 2020 06:58:36 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70952547465feacd9a881950c68053de0695016089b56df1bf8b8eba263feb58`  
		Last Modified: Thu, 20 Feb 2020 09:06:13 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2712e9137fe77cc57c050aac68dca033d5cf870a3cf55710d5d073fa556056f7`  
		Last Modified: Thu, 20 Feb 2020 09:06:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e38ed301b7763ec250b1718f3a9e6e0d4a0c1cdcbb8726149bf528385412af`  
		Last Modified: Thu, 20 Feb 2020 09:06:11 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93ada470b3a2d2c9fe60276cf580b0c1842d800bfd77036d72322f353f0bf5a`  
		Last Modified: Thu, 20 Feb 2020 09:06:10 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fb06c974b3827e7d70b6c1f374ef5d8d87bd22a22d5c74c0ff78bea7f83a5b`  
		Last Modified: Thu, 20 Feb 2020 09:06:08 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb6d829079c2283b10613e79e3302c5c486e70b665cc3a1d39334fddaff0042`  
		Last Modified: Thu, 20 Feb 2020 09:06:10 GMT  
		Size: 5.4 MB (5360772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456660bee63daca1346c066d1953951e745dc1a41b9d35192df7a9ad3ea3040c`  
		Last Modified: Thu, 20 Feb 2020 09:06:11 GMT  
		Size: 22.4 MB (22387053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ea327b6da49e8029a4bb754e077132764d30a2b46ad8560c66354cb54a4c49`  
		Last Modified: Thu, 20 Feb 2020 09:06:05 GMT  
		Size: 5.3 MB (5300100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1c4cfff9944c3a5ce6f90475e52c5443919ee63120774d7f4418ad2df8d26d`  
		Last Modified: Thu, 20 Feb 2020 09:06:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ad93238a90c982bc2087fcf22f3b6c905c73590e94feea00c7578ddcbe0673`  
		Last Modified: Thu, 20 Feb 2020 09:06:04 GMT  
		Size: 7.1 MB (7125203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec160e40b0e19050951f10c3541c8e7af444264792e0fe79f97074008ae7c39`  
		Last Modified: Thu, 20 Feb 2020 09:05:59 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab996eb6cc24ffb0c31cce78d38b9566f64218f6db39602e2addd01cadd5243`  
		Last Modified: Thu, 20 Feb 2020 09:06:26 GMT  
		Size: 16.7 MB (16691639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882c3cc943ef19d8dcd0988b989c1b27bc5aff2f10b5497b1e6bbeb33d6fa668`  
		Last Modified: Thu, 20 Feb 2020 09:06:03 GMT  
		Size: 5.3 MB (5315030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd93813d0697a0a5ec6dab393fa59755bda22e721f14d94ec7041fae715717d`  
		Last Modified: Thu, 20 Feb 2020 09:05:53 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed468d08db22c004cf6edecda086d73ea48e0e9d806ebecec28444ae43ef732`  
		Last Modified: Thu, 20 Feb 2020 09:05:57 GMT  
		Size: 5.3 MB (5315034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fa3b98dbbcde6655fab42a2d1f4fe9fd047a61c06d09960abd78618ad8ecbb`  
		Last Modified: Thu, 20 Feb 2020 09:05:56 GMT  
		Size: 5.3 MB (5320853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c1b7ced837972ed378a8ee931485cb1fe6c74e04a218e06484f702c2105300`  
		Last Modified: Thu, 20 Feb 2020 09:05:56 GMT  
		Size: 5.3 MB (5322406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd93e184f35e360af21714c4148cb2b7e2a8458d8254c9204e2dcc0ec85741a`  
		Last Modified: Thu, 20 Feb 2020 09:05:53 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
