## `mongo:latest`

```console
$ docker pull mongo@sha256:f1b5a4e2acc7db563457f41443103a2d48d1ee5a13332734f82222aa719e2542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:695e5eb141aa8516bd4857ee987d65401a424d0e5f8e0244ab89f6da981ddf65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232484056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0850fead9327a6d88722c27116309022d78e9daf526b407a88de09762c32e620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:36:46 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 09 Dec 2022 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:36:57 GMT
ENV GOSU_VERSION=1.12
# Fri, 09 Dec 2022 02:36:57 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 09 Dec 2022 02:37:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 09 Dec 2022 02:37:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 09 Dec 2022 02:37:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 09 Dec 2022 02:37:08 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 09 Dec 2022 02:37:08 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 09 Dec 2022 02:37:08 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 09 Dec 2022 02:37:08 GMT
ENV MONGO_MAJOR=6.0
# Fri, 09 Dec 2022 02:37:09 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 09 Dec 2022 02:37:09 GMT
ENV MONGO_VERSION=6.0.3
# Fri, 09 Dec 2022 02:37:32 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 09 Dec 2022 02:37:34 GMT
VOLUME [/data/db /data/configdb]
# Fri, 09 Dec 2022 02:37:34 GMT
ENV HOME=/data/db
# Fri, 09 Dec 2022 02:37:34 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Fri, 09 Dec 2022 02:37:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:37:35 GMT
EXPOSE 27017
# Fri, 09 Dec 2022 02:37:35 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef773e84b43a9957d1af78717d365575c45617e5309f34a2aa8e495069798539`  
		Last Modified: Fri, 09 Dec 2022 02:40:25 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfad1efb66451e1de01270bfb34ed66ec187ecc32cdb67bdec2fedca0cb7b78`  
		Last Modified: Fri, 09 Dec 2022 02:40:27 GMT  
		Size: 8.3 MB (8347737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e59a6d63c9b4462dbd6841a103e52acfc8ad333bf6058f5c5ed5c529e26104`  
		Last Modified: Fri, 09 Dec 2022 02:40:26 GMT  
		Size: 1.2 MB (1235335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f00ac700e0cec4e1e43e12f9c179f244d0bcd5f384c2c9c5c40b8ae4eab0c8`  
		Last Modified: Fri, 09 Dec 2022 02:40:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d33bf42f45676f2ad9ece4a44befa90451c705849c3b61ba529faf185a4a9e`  
		Last Modified: Fri, 09 Dec 2022 02:40:23 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa69d77b61ca264fb64e7b1405de4f1460f6b1d576d730d23d4a24fc660d42`  
		Last Modified: Fri, 09 Dec 2022 02:40:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa77b709a7d6fc6fa80fbe7b4df17a20ca071aeeb0d3a32c5153dff3ee52b630`  
		Last Modified: Fri, 09 Dec 2022 02:40:50 GMT  
		Size: 194.3 MB (194315456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245bd0c9ace239b697bee32efe953e526cb6e27005de6e4f3ce3ea04c461055f`  
		Last Modified: Fri, 09 Dec 2022 02:40:24 GMT  
		Size: 5.0 KB (4962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:dac1a094fc6ca3b76efeff9239669a892cc386cdbac7610b9a1c538a2e4f8329
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225833167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dea954758764febcecc5f2d513a1454d9809740e7447b410015fbffdf1d38bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:32:26 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 09 Dec 2022 03:33:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:33:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 09 Dec 2022 03:33:02 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 09 Dec 2022 03:33:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 09 Dec 2022 03:33:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 09 Dec 2022 03:33:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 09 Dec 2022 03:33:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 09 Dec 2022 03:33:12 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 09 Dec 2022 03:33:12 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 09 Dec 2022 03:33:12 GMT
ENV MONGO_MAJOR=6.0
# Fri, 09 Dec 2022 03:33:13 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 09 Dec 2022 03:33:13 GMT
ENV MONGO_VERSION=6.0.3
# Fri, 09 Dec 2022 03:33:36 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 09 Dec 2022 03:33:40 GMT
VOLUME [/data/db /data/configdb]
# Fri, 09 Dec 2022 03:33:40 GMT
ENV HOME=/data/db
# Fri, 09 Dec 2022 03:33:40 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Fri, 09 Dec 2022 03:33:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Dec 2022 03:33:40 GMT
EXPOSE 27017
# Fri, 09 Dec 2022 03:33:40 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fa6fcd8473e6fa6433f55142d9c974f4567154eb0a71e8d1e87798291f30b3`  
		Last Modified: Fri, 09 Dec 2022 03:36:34 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446df0a3bab48e1d13c800934f85a49fd3699cbcfa499e48832a0ce9952ebe88`  
		Last Modified: Fri, 09 Dec 2022 03:36:35 GMT  
		Size: 8.2 MB (8176933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103570790f4fc06adbaceee688035e7165ead154becbe7a6dc15ec6c1c33f590`  
		Last Modified: Fri, 09 Dec 2022 03:36:34 GMT  
		Size: 1.2 MB (1170741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecf974f5e71402b0c615f04b25c9e20e6d86259d2e95df9000a30c8061c12de`  
		Last Modified: Fri, 09 Dec 2022 03:36:32 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b443c152443efaa69fd0a2c9b50d543cb1f14d7c76a710a2ec98fe5a4a8a93a5`  
		Last Modified: Fri, 09 Dec 2022 03:36:32 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16ff3964c535e1af53e87669d6c71320f13ee4e198563e026ef3816374d8f27`  
		Last Modified: Fri, 09 Dec 2022 03:36:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb556a2f7a2ff6727796e82da3e4df0e18ec03d2e048491aeb0787d78c230b2`  
		Last Modified: Fri, 09 Dec 2022 03:36:51 GMT  
		Size: 189.3 MB (189283674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e210662203f590472301e89c3cd2c71d5376cd632dc15657fcd040e28d0b6c`  
		Last Modified: Fri, 09 Dec 2022 03:36:31 GMT  
		Size: 5.0 KB (4963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.1249; amd64

```console
$ docker pull mongo@sha256:4056973ed363c4fc7139e0d3aeb76397164596eca267d61099849e536a324780
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2995066920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c07e57652a9782d664cb537e986d03b202781a96458e930826223be8e12e96`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Wed, 09 Nov 2022 14:41:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 16 Nov 2022 19:15:39 GMT
ENV MONGO_VERSION=6.0.3
# Wed, 16 Nov 2022 19:15:40 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.3-signed.msi
# Wed, 16 Nov 2022 19:15:41 GMT
ENV MONGO_DOWNLOAD_SHA256=6557ae0360747d348aefdf30d1360f577804c446579c2012e0b04e5ec2489c49
# Wed, 16 Nov 2022 19:18:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 16 Nov 2022 19:18:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 16 Nov 2022 19:18:14 GMT
EXPOSE 27017
# Wed, 16 Nov 2022 19:18:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcc0cd10e58716558145d847bcea390e3840d172df19b8d0f08a57dd985262d`  
		Last Modified: Wed, 09 Nov 2022 19:02:46 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ece0a1889d31de1895fb48f6f37d23fca3a7f73e8b63b6e37ea1a868e7f66d`  
		Last Modified: Wed, 16 Nov 2022 21:18:06 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91609187359c05a5835119c3a1d9f2fff8d4d397e52da17425675df1087983d4`  
		Last Modified: Wed, 16 Nov 2022 21:18:06 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ae461c4682087af4c74e18ddd8f7274f6b15e4660c44435a82269994377a2`  
		Last Modified: Wed, 16 Nov 2022 21:18:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28c4f5edecc349d7f8990290609bf47befb11c720df04afa49cf40abb1cb5f7`  
		Last Modified: Wed, 16 Nov 2022 21:19:52 GMT  
		Size: 513.3 MB (513288297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34784e2cca2c762ae85677db36f88e17c66ea756c09c19cf6dec5c3de1678b07`  
		Last Modified: Wed, 16 Nov 2022 21:18:04 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bcc4c3a2fc9d68cd21dc03876150493f0d81cc877ffb1fb788da9c1be473a0d`  
		Last Modified: Wed, 16 Nov 2022 21:18:04 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0caf8a1fc0a90f46855c1e51b85f42551fb4457108fe6bf7df383b6fc2d2fb`  
		Last Modified: Wed, 16 Nov 2022 21:18:04 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.3650; amd64

```console
$ docker pull mongo@sha256:eea28197a1ce2de148516d698d523cfbda754746efb1788863b098c6568eb142
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3291675239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2052a242f5d01f2b519f8a117028ac3536560851e84abd493a923f2cfbe62ec0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 16 Nov 2022 19:18:34 GMT
ENV MONGO_VERSION=6.0.3
# Wed, 16 Nov 2022 19:18:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.3-signed.msi
# Wed, 16 Nov 2022 19:18:37 GMT
ENV MONGO_DOWNLOAD_SHA256=6557ae0360747d348aefdf30d1360f577804c446579c2012e0b04e5ec2489c49
# Wed, 16 Nov 2022 19:22:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 16 Nov 2022 19:22:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 16 Nov 2022 19:22:18 GMT
EXPOSE 27017
# Wed, 16 Nov 2022 19:22:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c3c860f0c8b679ce28966385de521dc6f0dfd2e3d9a35f46b3e061b644bcf9`  
		Last Modified: Wed, 16 Nov 2022 21:20:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99877d1d553152415574273cb6ce93cab85495d9ac3f65bf327da1c9612c187b`  
		Last Modified: Wed, 16 Nov 2022 21:20:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e35fc34567f814a64eee812f3ea37bb2b2076a4cf22bf702dac1cab4840b67`  
		Last Modified: Wed, 16 Nov 2022 21:20:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9b0252e0b3bd96b6b1d1944246eb54475576d95348038ff3d43d00d0fa08d1`  
		Last Modified: Wed, 16 Nov 2022 21:21:45 GMT  
		Size: 513.1 MB (513078538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f105d6fa9e90ea3455202cdf23f2ebe84938a4db78e953271127cfb9f314cf83`  
		Last Modified: Wed, 16 Nov 2022 21:20:09 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcc7547f91eb159d4d3743e0ae2707a60e85525990a7ec8a8f577020b690a70`  
		Last Modified: Wed, 16 Nov 2022 21:20:09 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65ad05df5da36181da6db4a4ce0c8f3aa42c9fef131f3d12084f3101a9ec5e7`  
		Last Modified: Wed, 16 Nov 2022 21:20:09 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
