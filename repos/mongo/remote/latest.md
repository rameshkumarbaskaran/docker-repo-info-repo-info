## `mongo:latest`

```console
$ docker pull mongo@sha256:695cc4d237d158d32d5ddcadefe06444dbbd5feac2d50f560b60b70f2198c16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:028650e24cdc662da15e11809d63b4f2a0b7eb782f3ca4f80a303a4c255fab89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237158219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61eca46d7769696024576c77399590837fa7efd5265809638981ad7d7977e987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:00:25 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 04 May 2023 08:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:00:35 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 May 2023 08:00:35 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 04 May 2023 08:00:42 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 May 2023 08:00:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 May 2023 08:00:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 04 May 2023 08:00:43 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 04 May 2023 08:00:43 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 08:00:44 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 08:00:44 GMT
ENV MONGO_MAJOR=6.0
# Thu, 04 May 2023 08:00:44 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 24 May 2023 01:40:05 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 24 May 2023 01:40:34 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 24 May 2023 01:40:35 GMT
VOLUME [/data/db /data/configdb]
# Wed, 24 May 2023 01:40:35 GMT
ENV HOME=/data/db
# Wed, 24 May 2023 01:40:36 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Wed, 24 May 2023 01:40:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 01:40:36 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:40:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb83bb7be9889457cf3729cf50df2596a4c21e221943325d43e3621afc85296`  
		Last Modified: Thu, 04 May 2023 08:01:33 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95121721c4c526b9ccd2b5630e6b439780c39872431d4a3bedcbc4769350cdc`  
		Last Modified: Thu, 04 May 2023 08:01:34 GMT  
		Size: 5.0 MB (5027884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799041b403cabf54ac974c77fee7211729ec7ddc13fbabe98f93868f43a32fcb`  
		Last Modified: Thu, 04 May 2023 08:01:34 GMT  
		Size: 1.3 MB (1252462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1828e70ef29acb455c8b97fe8b6bc926a79a105e578b55cf78bd979be29535b5`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3781beae9e4d098a887d213f6d3fbb1c9c9648b3516672f63c534a6aa1ea67`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d575316233327cdb50cd97e5b06250f7e5733f3e9aa5a79ba8821492145fd78`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf73eea516c85b3b9a343be653841792b483e848393886655392e7be08c1c876`  
		Last Modified: Wed, 24 May 2023 01:42:32 GMT  
		Size: 200.4 MB (200438961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cf5b4ad9679ad118d13d063177463f678e486a09decaacfe5557a68c1396b8`  
		Last Modified: Wed, 24 May 2023 01:42:08 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f1026aa44f9e6cf6bb714edaecd2fe0b1045139b35bc38904d3f4e1f5516ef5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230693129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4a59e38e8e780359e5d862cbaad924f94eff768314f360137e8025c5541b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:51:06 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 04 May 2023 03:51:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:51:18 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 May 2023 03:51:18 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 04 May 2023 03:51:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 May 2023 03:51:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 May 2023 03:51:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 04 May 2023 03:51:25 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 04 May 2023 03:51:25 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 03:51:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 03:51:26 GMT
ENV MONGO_MAJOR=6.0
# Thu, 04 May 2023 03:51:26 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 24 May 2023 00:44:13 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 24 May 2023 00:44:49 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 24 May 2023 00:44:52 GMT
VOLUME [/data/db /data/configdb]
# Wed, 24 May 2023 00:44:52 GMT
ENV HOME=/data/db
# Wed, 24 May 2023 00:44:52 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Wed, 24 May 2023 00:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 00:44:52 GMT
EXPOSE 27017
# Wed, 24 May 2023 00:44:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c1bc6eb929a761d6c8e4e8e9ca2ca6899807a698ab2ce58119de51c77f0c3f`  
		Last Modified: Thu, 04 May 2023 03:52:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5af3169343953ea89194ebd7f6953d78bf81eda11daaa939e57beec9acd2a30`  
		Last Modified: Thu, 04 May 2023 03:52:12 GMT  
		Size: 5.0 MB (4968460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f5afa97a66a32b032396016f112241bcd27938b1504b994944c902286d9571`  
		Last Modified: Thu, 04 May 2023 03:52:11 GMT  
		Size: 1.2 MB (1185066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05f20747b8314c2fa5c58ac2f2afbe9e5d9d099b795355ece221d2f2cfec7b4`  
		Last Modified: Thu, 04 May 2023 03:52:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5a4df6de089141e46014379b79716d1d54b9ce14a15e2a5cf77d65f460012d`  
		Last Modified: Thu, 04 May 2023 03:52:09 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee7bab4fd177aa035083292992f83182e701972b707eec8852b9329657df6b6`  
		Last Modified: Thu, 04 May 2023 03:52:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34df35d91d39c62b7c94162b624c4733e1b3ad7f9816262294a0a8d89e033ff`  
		Last Modified: Wed, 24 May 2023 00:46:43 GMT  
		Size: 196.1 MB (196141463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60895e13c05065289eddaeaa2356a7e7016f60d958e66ee243d3b02c31df54e5`  
		Last Modified: Wed, 24 May 2023 00:46:26 GMT  
		Size: 5.0 KB (5021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.1726; amd64

```console
$ docker pull mongo@sha256:a2f69ee6120c8a6a8aecfb8b549a6908b487b1e60f091defdb089abac37a865c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291249118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f69c64675d1a5b1fb32837234214a489c9cf662056000b942410123b5aa9a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 01:53:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 24 May 2023 01:15:18 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 24 May 2023 01:15:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.6-signed.msi
# Wed, 24 May 2023 01:15:20 GMT
ENV MONGO_DOWNLOAD_SHA256=585afad69ec57040b1a8f502a039c3fef160dccbe6c48c53e15adde9976724a6
# Wed, 24 May 2023 01:17:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 24 May 2023 01:17:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 May 2023 01:17:23 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:17:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ae2b2372db6d2d1ac04a5297e71fc9a798a078f7d1a0bcccae77193e8b58b2`  
		Last Modified: Wed, 10 May 2023 02:22:13 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d831657b6564663196da33c47e5fa0f92a4e6b78e4a96b9cbc1ec1bf946ac8`  
		Last Modified: Wed, 24 May 2023 01:36:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672c5d119420c2b20df34efd39c415c938b2db3d4dcdb592264506f5cfa6ec97`  
		Last Modified: Wed, 24 May 2023 01:36:41 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fdb8bdf3d875e92884eaabbf6b06a6496e13831133251a53af8ef37e21807`  
		Last Modified: Wed, 24 May 2023 01:36:39 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a552c02ac76991f000d7287a801bcfc2bad41959603f378a52ada85ebe4bd263`  
		Last Modified: Wed, 24 May 2023 01:37:52 GMT  
		Size: 516.3 MB (516257735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b5e8f7877f1db588fc2aca5f97f743d8fa294704483f477087ac48ca10727f`  
		Last Modified: Wed, 24 May 2023 01:36:39 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ba9687f93d1fca18db83236308825e8a2da391a369922a050920b18c05c1e9`  
		Last Modified: Wed, 24 May 2023 01:36:39 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d671a02933775a0a5d518cfcd7a98aece04846819091f0feeaeae05f1bcc7459`  
		Last Modified: Wed, 24 May 2023 01:36:39 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.4377; amd64

```console
$ docker pull mongo@sha256:095a6ea5ce5ab252da3482e9473e849f9df5d94fe24e97a72392e6cb7048615f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2588350793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a95a1c92ed7b9c11f977baff37067a95367b36e465c3ce408f33b5d97de5cf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 24 May 2023 01:17:31 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 24 May 2023 01:17:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.6-signed.msi
# Wed, 24 May 2023 01:17:32 GMT
ENV MONGO_DOWNLOAD_SHA256=585afad69ec57040b1a8f502a039c3fef160dccbe6c48c53e15adde9976724a6
# Wed, 24 May 2023 01:20:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 24 May 2023 01:20:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 May 2023 01:20:23 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:20:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81422d35aa8341bef06d995d7408b001c17532ac305453ae0624a5fe5e5e6657`  
		Last Modified: Wed, 24 May 2023 01:38:08 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701a81d477339f7560020a3830e02d167506aa5d802fc0b2760d0f4b94db5cc8`  
		Last Modified: Wed, 24 May 2023 01:38:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54657ad5e91207bfa9bebbebee13cf435d661b2582babb24ce1836f591edd41`  
		Last Modified: Wed, 24 May 2023 01:38:06 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddcc78b8d32e33da88a9fe23fd9f9dab4a91f107b829263619cf23424e801bb`  
		Last Modified: Wed, 24 May 2023 01:39:23 GMT  
		Size: 516.3 MB (516305726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f04476c99fec34f432553c85888a9d9f7bf5a96fba998745250a25c6212815`  
		Last Modified: Wed, 24 May 2023 01:38:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da05dabf67ce090785770af822f43b188c4bdef6e4b536387bae97abd6e65516`  
		Last Modified: Wed, 24 May 2023 01:38:06 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e117fdef73bdf4e0a5707103633f94f2eb79a4ec5da4a5c53cde435bf9b86e1`  
		Last Modified: Wed, 24 May 2023 01:38:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
