## `mongo:latest`

```console
$ docker pull mongo@sha256:1e72fdd16fc769e5200dad77eff5b2316730d42473c281d8192872698e1f8689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:5b5263a7d25d06d5149904eaaacdb359edcd4f26a3d971265f85362dd2406655
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249706920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21ad2afe409e7d5cba51a409dadff2b9935b67b91934e44cdf7b44cd2778f33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:06:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 06 Apr 2022 04:06:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:06:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:06:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 06 Apr 2022 04:06:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:06:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 04:06:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 06 Apr 2022 04:06:39 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 06 Apr 2022 04:06:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 06 Apr 2022 04:06:40 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 06 Apr 2022 04:06:40 GMT
ENV MONGO_MAJOR=5.0
# Wed, 06 Apr 2022 04:06:40 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 11 Apr 2022 21:42:25 GMT
ENV MONGO_VERSION=5.0.7
# Mon, 11 Apr 2022 21:42:54 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 11 Apr 2022 21:42:56 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 11 Apr 2022 21:42:56 GMT
VOLUME [/data/db /data/configdb]
# Mon, 11 Apr 2022 21:42:56 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Mon, 11 Apr 2022 21:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Apr 2022 21:42:56 GMT
EXPOSE 27017
# Mon, 11 Apr 2022 21:42:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a086fc80eaabd12d02bd4065e009878cfc9362d238169ea745e39a263c2270`  
		Last Modified: Wed, 06 Apr 2022 04:09:02 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6592c2fb05fb80b5a3c01c92bc623faf5fc0ded7dd0551be39ea78a4d9efc8`  
		Last Modified: Wed, 06 Apr 2022 04:09:03 GMT  
		Size: 3.1 MB (3064007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad2281c276115bf50711681c05326e6a65cec55a5d727481ac937664a35efa`  
		Last Modified: Wed, 06 Apr 2022 04:09:03 GMT  
		Size: 6.5 MB (6505644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34073132290cb60828b8a5ca2eb216d7f6c21a306dd0ba675f0a297b5ed5acd0`  
		Last Modified: Wed, 06 Apr 2022 04:09:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec793bc1a2aee24538b2237e39e4a3a0a5f2d6d6362e613893093708f8ebcf4a`  
		Last Modified: Wed, 06 Apr 2022 04:09:00 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660887418c9b636f3ae29187f3e75b0b75f104c10c76177bda14c4f86c667dd4`  
		Last Modified: Wed, 06 Apr 2022 04:09:00 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6674b2f5c8282f9746304f125205ff9fa8213318e3f22e5904e54b5afd375cc8`  
		Last Modified: Mon, 11 Apr 2022 21:43:56 GMT  
		Size: 211.6 MB (211562254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ad8871da64841dd4393c3945e964a6e11fbed92e1abc7dbbee2271509f521a`  
		Last Modified: Mon, 11 Apr 2022 21:43:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f7bc3e1868adeb709abf3b25e3acca6c194d0977675d48c8307dbcbc2fabe7`  
		Last Modified: Mon, 11 Apr 2022 21:43:27 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:714b74ff465bd78abbae10bfcefe1bb331c6ad38c40a2226b0ad8db5428db25e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241848404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1658c558d2d5bd62863e0c8746b8b296387cc7f6bdbb295ec5e0b715247b10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:29:38 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 05 Apr 2022 23:29:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:29:49 GMT
ENV GOSU_VERSION=1.12
# Tue, 05 Apr 2022 23:29:50 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 05 Apr 2022 23:30:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 05 Apr 2022 23:30:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 05 Apr 2022 23:30:11 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 05 Apr 2022 23:30:12 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 05 Apr 2022 23:30:13 GMT
ENV MONGO_MAJOR=5.0
# Tue, 05 Apr 2022 23:30:14 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 11 Apr 2022 21:46:09 GMT
ENV MONGO_VERSION=5.0.7
# Mon, 11 Apr 2022 21:46:32 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 11 Apr 2022 21:46:32 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 11 Apr 2022 21:46:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 11 Apr 2022 21:46:35 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Mon, 11 Apr 2022 21:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Apr 2022 21:46:36 GMT
EXPOSE 27017
# Mon, 11 Apr 2022 21:46:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9275dc5f58a824992dd7134eb5d1a03b3444789e31773e1610b9604d7fd5293f`  
		Last Modified: Tue, 05 Apr 2022 23:33:26 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e820cd795df140b554de55a8fd8db2ab8e46f204bf20439b9fe7e342d06b323e`  
		Last Modified: Tue, 05 Apr 2022 23:33:27 GMT  
		Size: 2.9 MB (2911252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003e7508c0ed3f4cf57557f470f1fdf5d9d803515e608dd76cc5fdc86673f691`  
		Last Modified: Tue, 05 Apr 2022 23:33:28 GMT  
		Size: 6.2 MB (6247673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c926d087e859efce609d51a7725b4dc22aad4acbeea44ae5fcc9093aeae447`  
		Last Modified: Tue, 05 Apr 2022 23:33:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c8045d45d9657198979d78588596602f3074b44802c00a92565770e7eb13db`  
		Last Modified: Tue, 05 Apr 2022 23:33:24 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2561362d345d5c89d213f5606c562b6b692a8ecf8800ca8b4fd260e8bcc59dc9`  
		Last Modified: Tue, 05 Apr 2022 23:33:24 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce14378ef364a0a513134bbc3b63c762cf01047f38f6e0634fd5df52de6fb4e`  
		Last Modified: Mon, 11 Apr 2022 21:48:03 GMT  
		Size: 205.5 MB (205511504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2e8cf09fc93337256d677de212c10c59f3ceb22060fc6b919fc8c8bb5c84f3`  
		Last Modified: Mon, 11 Apr 2022 21:47:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2f4560781063c6f09360ce9f50171a0368d5aa42143e9a2157eb5afd4d2dc5`  
		Last Modified: Mon, 11 Apr 2022 21:47:36 GMT  
		Size: 5.0 KB (4951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.643; amd64

```console
$ docker pull mongo@sha256:c551917cd7b27ab5d0cac9e87fd504f95ca06ebf2610b6c56e6386060f7499d1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2533895103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac90c1acdfdaba1bb473c3770aaeec1f112740703d2e7198934a6b7b5949c356`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 12:34:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 17:30:03 GMT
ENV MONGO_VERSION=5.0.7
# Wed, 13 Apr 2022 17:30:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.7-signed.msi
# Wed, 13 Apr 2022 17:30:05 GMT
ENV MONGO_DOWNLOAD_SHA256=3d9eee63d56ff75176cf03308274a29c9e385704e21a26f5864cfe1357ca3cf7
# Wed, 13 Apr 2022 17:31:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 17:31:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Apr 2022 17:31:31 GMT
EXPOSE 27017
# Wed, 13 Apr 2022 17:31:32 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2a5d28823cc7f2a78cb6b52a2cadb350e978705d7634adbcfbc4bd80d4637c2`  
		Last Modified: Wed, 13 Apr 2022 14:11:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8f4da1c3ac9a9cbd52543f5061c6fbc24a8980cd9411d4c625e91284f5b288`  
		Last Modified: Wed, 13 Apr 2022 17:54:38 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98bbc2ba4f98de333dcd6e5061d585a325577094c32c28c1d4ed43033083828`  
		Last Modified: Wed, 13 Apr 2022 17:54:38 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c35fca65cba01d939edbc701a2c58410b94e430bf93350d54c5abfcffc5409`  
		Last Modified: Wed, 13 Apr 2022 17:54:35 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69d1ed8b2315a6126b58e0d3151aa9ac27ebe1ce7fb5ca243afb444bf5be36f`  
		Last Modified: Wed, 13 Apr 2022 17:59:50 GMT  
		Size: 306.9 MB (306930393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e21e42a9a082d8988a908b45e9b1dedfb7e7d70199a134f3a0c327e068b3f37`  
		Last Modified: Wed, 13 Apr 2022 17:54:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eded7b672fbe2a2927fd581a459e220208a0a649acf8a7ebc9da0878f1895c`  
		Last Modified: Wed, 13 Apr 2022 17:54:35 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553d324af8f0d9738175edafbdc297be5a0e884bdb80cc169f549247a9ed59a4`  
		Last Modified: Wed, 13 Apr 2022 17:54:35 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.2803; amd64

```console
$ docker pull mongo@sha256:ab65c946e5b4492352a6d791aa7669b2e74a7437ff60729386be70fbf9828b1d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3022632808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c662661f2fbc399624dc311c88d35a12012533055c15e9b4f97244af6022f333`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 17:31:45 GMT
ENV MONGO_VERSION=5.0.7
# Wed, 13 Apr 2022 17:31:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.7-signed.msi
# Wed, 13 Apr 2022 17:31:46 GMT
ENV MONGO_DOWNLOAD_SHA256=3d9eee63d56ff75176cf03308274a29c9e385704e21a26f5864cfe1357ca3cf7
# Wed, 13 Apr 2022 17:34:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 17:34:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Apr 2022 17:34:07 GMT
EXPOSE 27017
# Wed, 13 Apr 2022 17:34:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b66ea12661f8a8e6b38ced86e61ba70695074d50b6beeccf745bb6c4fbf8060`  
		Last Modified: Wed, 13 Apr 2022 18:00:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1758d9b808173f706b8e382fdfa0119c87b64413fe0fb97d4e73e7c8b8b4767f`  
		Last Modified: Wed, 13 Apr 2022 18:00:13 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f8a0b16fd9885a81c9960737cb8a1c89d4f9ab8e6bc80ba5a9a94d89299e2`  
		Last Modified: Wed, 13 Apr 2022 18:00:11 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfba45e2006de2b17af9f6c74b2adc209b96d198686dd629a481e419f9b0b96`  
		Last Modified: Wed, 13 Apr 2022 18:00:59 GMT  
		Size: 306.7 MB (306702622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6896d514b1629ff43d1862822a5b0a64c497a3d9709d33e037960907f7cb56`  
		Last Modified: Wed, 13 Apr 2022 18:00:11 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0bc625ce7c9a95cfe10076a85555dd4d864fa68d209de4689debf9238825c6`  
		Last Modified: Wed, 13 Apr 2022 18:00:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc6d4eaef225bdb7607651756a84aeb7f1ab8a16b004a692a09b7f2a6cb79c8`  
		Last Modified: Wed, 13 Apr 2022 18:00:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
