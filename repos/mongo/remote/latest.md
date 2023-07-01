## `mongo:latest`

```console
$ docker pull mongo@sha256:32ce4bc06b970bce41f9068112f22ddd51c4b16bff0be79a7a335fe40492728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:0d5209d754046783e6f194e55f28fc8846a9adee9b3f221280032007683605db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237538506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56225fdc72d0ba2b9e3c73e6772093fdc33a2ebf67578ed1be3efb21564e7d8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:14:50 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 16 Jun 2023 03:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:15:18 GMT
ENV GOSU_VERSION=1.16
# Fri, 16 Jun 2023 03:15:18 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 16 Jun 2023 03:15:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 16 Jun 2023 03:15:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 16 Jun 2023 03:15:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 16 Jun 2023 03:15:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 16 Jun 2023 03:15:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 16 Jun 2023 03:15:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 16 Jun 2023 03:15:48 GMT
ENV MONGO_MAJOR=6.0
# Fri, 16 Jun 2023 03:15:49 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 30 Jun 2023 23:33:05 GMT
ENV MONGO_VERSION=6.0.7
# Fri, 30 Jun 2023 23:33:24 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 30 Jun 2023 23:33:25 GMT
VOLUME [/data/db /data/configdb]
# Fri, 30 Jun 2023 23:33:25 GMT
ENV HOME=/data/db
# Fri, 30 Jun 2023 23:33:26 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Fri, 30 Jun 2023 23:33:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jun 2023 23:33:26 GMT
EXPOSE 27017
# Fri, 30 Jun 2023 23:33:26 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5d4dae314d61ef2c7df20dbb6134a5e213a5131de25af242f608e8621368f`  
		Last Modified: Fri, 16 Jun 2023 03:17:58 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe6867b3f800a0cfee1cf1e018de5214b3da298faf0f0e5d6651547c53c765c`  
		Last Modified: Fri, 16 Jun 2023 03:17:59 GMT  
		Size: 5.1 MB (5050584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4c7cb44e892df114bea9e573b88e40ac1e651feb36f91fa6dd91a014f56a7c`  
		Last Modified: Fri, 16 Jun 2023 03:17:58 GMT  
		Size: 1.3 MB (1252923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c7016c15b5571e14f18e728cca49a7f5882fc084cac8412e36d4981757a81f`  
		Last Modified: Fri, 16 Jun 2023 03:17:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d740b6c98119553d4d259f37335119abf517fff019448d1f2cc526e3996ab89`  
		Last Modified: Fri, 16 Jun 2023 03:17:56 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329604f2207885845c2a7dff036e513a28de91883838129f7bae448f71f26aae`  
		Last Modified: Fri, 16 Jun 2023 03:17:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fa33e0d6430f0672c0322d0c1a87e569a93cf0ad6d4f8b78561ae698d70fa1`  
		Last Modified: Fri, 30 Jun 2023 23:35:25 GMT  
		Size: 200.8 MB (200795290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84daea1c560ef1624ca7aa977ed42549da469a34eb79115b0175844f371d54f`  
		Last Modified: Fri, 30 Jun 2023 23:35:01 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ca7a85b60368af36120e490d4e633fac9c297e0b752a59df3479459e8057dda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231078300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7268dfde552369a7ce8b630bfa50b6b41180cf79df08bab7e6b6ba8c32eca1a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:28:53 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 16 Jun 2023 03:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:29:02 GMT
ENV GOSU_VERSION=1.16
# Fri, 16 Jun 2023 03:29:02 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 16 Jun 2023 03:29:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 16 Jun 2023 03:29:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 16 Jun 2023 03:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 16 Jun 2023 03:29:27 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 16 Jun 2023 03:29:27 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 16 Jun 2023 03:29:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 16 Jun 2023 03:29:28 GMT
ENV MONGO_MAJOR=6.0
# Fri, 16 Jun 2023 03:29:28 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 30 Jun 2023 23:51:33 GMT
ENV MONGO_VERSION=6.0.7
# Fri, 30 Jun 2023 23:51:52 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 30 Jun 2023 23:51:53 GMT
VOLUME [/data/db /data/configdb]
# Fri, 30 Jun 2023 23:51:53 GMT
ENV HOME=/data/db
# Fri, 30 Jun 2023 23:51:53 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Fri, 30 Jun 2023 23:51:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jun 2023 23:51:53 GMT
EXPOSE 27017
# Fri, 30 Jun 2023 23:51:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cac3c1cd860738646e8f7907a2c3863a1ee373f9f3831276f505f4fe93848e`  
		Last Modified: Fri, 16 Jun 2023 03:31:24 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4918c863202ff28fd431e919e4f78c35a462692f2a210e2d527f0c79334672d8`  
		Last Modified: Fri, 16 Jun 2023 03:31:24 GMT  
		Size: 5.0 MB (4992702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15db68cff03fa562720903e404ed27b57a3abd31799aadffdd5fdb2240d36451`  
		Last Modified: Fri, 16 Jun 2023 03:31:24 GMT  
		Size: 1.2 MB (1185480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a8d4510bd52238dd307318b241c95bb5047ad5ce42b489d6a68f72efb1576`  
		Last Modified: Fri, 16 Jun 2023 03:31:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81877556e7b413ffc098ea9636438c1788f277520162a9cfef2ab4f42d6120f`  
		Last Modified: Fri, 16 Jun 2023 03:31:22 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7222461baf3a5795081e53a9a91777d9552181b24d41a4d36a9d83110079a8`  
		Last Modified: Fri, 16 Jun 2023 03:31:22 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d589ae6f5fd8b5c190ed0e1ec24fc25ccd50d86a0c42666aff7a7fb5dd2c86b`  
		Last Modified: Fri, 30 Jun 2023 23:53:33 GMT  
		Size: 196.5 MB (196502242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c0287bf536a64444cc554e50f829c0866a1601fa88ee33f25291928119046f`  
		Last Modified: Fri, 30 Jun 2023 23:53:15 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.1787; amd64

```console
$ docker pull mongo@sha256:f9c2934c24f81958e6ff8e94f7ebc07614fbe7d46adc015a2ffe09b66a9891fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942433860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846c5885ea4f61e0da9360c0950e7d571b3ade4ac5d25e80cec445332b94f94`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 02:25:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 24 Jun 2023 02:41:56 GMT
ENV MONGO_VERSION=6.0.6
# Sat, 24 Jun 2023 02:41:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.6-signed.msi
# Sat, 24 Jun 2023 02:41:58 GMT
ENV MONGO_DOWNLOAD_SHA256=585afad69ec57040b1a8f502a039c3fef160dccbe6c48c53e15adde9976724a6
# Sat, 24 Jun 2023 02:43:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 02:43:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:43:56 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:43:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369acdd1cf7c4d89f87cf3df6c1a935d83dad0afd57c96dcd7251a04481546a0`  
		Last Modified: Sat, 24 Jun 2023 05:25:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5616abab3d9ec61b9b1df568f529e1b8808781676555335fb440cdb2900c39e4`  
		Last Modified: Sat, 24 Jun 2023 06:41:06 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26855da333bfb6c0024c2ecfbdf9ecd4386aedbe614d45df43a3b3e6012934a`  
		Last Modified: Sat, 24 Jun 2023 06:41:06 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078351807daa9e213d7711f44fcfc076a0914ad18b779dc41e684da8c71e62a4`  
		Last Modified: Sat, 24 Jun 2023 06:41:04 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1d354bf30584043d8664975ab49662239980f869a62a3320bb23af279aef1c`  
		Last Modified: Sat, 24 Jun 2023 06:42:18 GMT  
		Size: 516.1 MB (516125356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353e77fd5dc58f4c913da69987f385306cce1e9180fa1c860e840f450146729`  
		Last Modified: Sat, 24 Jun 2023 06:41:04 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456f218ea7df8a7cdf57e10f1e780fb24b3c51c9972c7d5bee6feef9eeb8583c`  
		Last Modified: Sat, 24 Jun 2023 06:41:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22add58e900b33dbeada7c0a536e51370158424492b9f68a28049416d561fb`  
		Last Modified: Sat, 24 Jun 2023 06:41:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:48e29412a1c1543459aacaa534986a080c3fa1d1f501226d7534d45ee7f291fa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166885517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719cce80785572bcd4a78ace717429e7f6dd9894b9e539303316813e53910183`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 02:28:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 24 Jun 2023 02:44:10 GMT
ENV MONGO_VERSION=6.0.6
# Sat, 24 Jun 2023 02:44:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.6-signed.msi
# Sat, 24 Jun 2023 02:44:11 GMT
ENV MONGO_DOWNLOAD_SHA256=585afad69ec57040b1a8f502a039c3fef160dccbe6c48c53e15adde9976724a6
# Sat, 24 Jun 2023 02:46:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 02:46:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:46:19 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:46:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9634b679e6c602a6aaf0bae51625e7ca041489c77150db557640304f51bb37`  
		Last Modified: Sat, 24 Jun 2023 03:01:43 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c04e4c66f0c316991c767cd8487be1bb833ecf0dd8279b4b8948d35d9843944`  
		Last Modified: Sat, 24 Jun 2023 06:42:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5f68f9c3242e0657f0fbf3db30792de8615254c08280dcfa455f81a824be36`  
		Last Modified: Sat, 24 Jun 2023 06:42:34 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebbaad2c5797ad4eadd71cbb3941fd5cac755880687b8ba639394508e9cd0ac`  
		Last Modified: Sat, 24 Jun 2023 06:42:33 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1a97bcdadd53b96a0f2559bb23b822d66cf6a04fab66d8ff1e768c53c923c2`  
		Last Modified: Sat, 24 Jun 2023 06:43:49 GMT  
		Size: 516.1 MB (516139075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1886fa5089512d8d071df8e085375c686307f3f09e3e91c0e538b53c6c94d1`  
		Last Modified: Sat, 24 Jun 2023 06:42:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80eb6181dade42d5056178a8e4c4ce0694c7bbb545ab7997b4f8ace7dd76ef0`  
		Last Modified: Sat, 24 Jun 2023 06:42:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bd3182693c9af3ad026603416d9859c81cc6f8cc4b575d851ee96bd7e5cc01`  
		Last Modified: Sat, 24 Jun 2023 06:42:32 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
