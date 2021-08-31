## `mongo:latest`

```console
$ docker pull mongo@sha256:58ea1bc09f269a9b85b7e1fae83b7505952aaa521afaaca4131f558955743842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:827898fe26e633d2ba767fc2fd6f2bec664878a7ea6655a2c2a20d7bbc8b1e49
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248638295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcbeb494bed17f8d46fbf05569d7b9e079eb49010d2c098d914c1d04ca9f78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:51:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 31 Aug 2021 03:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:51:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 31 Aug 2021 03:51:15 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 31 Aug 2021 03:51:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 31 Aug 2021 03:51:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Aug 2021 03:51:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 31 Aug 2021 03:51:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 31 Aug 2021 03:51:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 31 Aug 2021 03:51:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 31 Aug 2021 03:51:35 GMT
ENV MONGO_MAJOR=5.0
# Tue, 31 Aug 2021 03:51:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 31 Aug 2021 03:51:35 GMT
ENV MONGO_VERSION=5.0.2
# Tue, 31 Aug 2021 03:52:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 31 Aug 2021 03:52:05 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 31 Aug 2021 03:52:05 GMT
VOLUME [/data/db /data/configdb]
# Tue, 31 Aug 2021 03:52:05 GMT
COPY file:df3353d9b2c25ef83b499ecae7fd5d611adb4a9462a577435178acaad3c8c695 in /usr/local/bin/ 
# Tue, 31 Aug 2021 03:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Aug 2021 03:52:05 GMT
EXPOSE 27017
# Tue, 31 Aug 2021 03:52:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664b0ebdcc074096f3cdb5767cd0679b6eb1b867cc4803caebc900c3a0e3cd7a`  
		Last Modified: Tue, 31 Aug 2021 03:54:55 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d598f4d3c08173a580ddfbc1aab7570a506bbe19ef2f760eef62bb18b0f2fe42`  
		Last Modified: Tue, 31 Aug 2021 03:54:56 GMT  
		Size: 3.1 MB (3064917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291455135b00f1125d53ec53b9bd1246a1a95c5289d78d52aeeebc2ca216e5ed`  
		Last Modified: Tue, 31 Aug 2021 03:54:56 GMT  
		Size: 6.5 MB (6506306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46409342f130fad45e914eb39eb6ff00f27268fb1b229f287a6b8102d7aa9bf`  
		Last Modified: Tue, 31 Aug 2021 03:54:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2b9c6e6f3a34b81bff9c8e5cca15de3929bb9eaac42390afe055c4fb1dead8`  
		Last Modified: Tue, 31 Aug 2021 03:54:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149f6335fc27dbe4a0d20cedeadb246cd0527052841f69e697ecf1dc3e5345cf`  
		Last Modified: Tue, 31 Aug 2021 03:54:53 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeb6f3bec76525035e546be91577375aa0cba19b64e0a261a1f3675468eecf7`  
		Last Modified: Tue, 31 Aug 2021 03:55:21 GMT  
		Size: 210.5 MB (210488552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8617caab2de56669e93c1c2b69ec7b1ff4755e928b0c99c1aecbcfabd9bef863`  
		Last Modified: Tue, 31 Aug 2021 03:54:53 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067d70de78282dabaa4714800e36e38a20fca78b2e99631e17480af35f36924e`  
		Last Modified: Tue, 31 Aug 2021 03:54:53 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:6f1615a312ff7e57fe3366e1a81d0fe98150aa2ac6a1a4beed2654cf719fc80c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 MB (238072223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31299b956c796f9089951170dabfd46a135f123eedfa12cb25c3cfa4ea356c6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:15:52 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 31 Aug 2021 03:15:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:15:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 31 Aug 2021 03:16:00 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 31 Aug 2021 03:16:13 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 31 Aug 2021 03:16:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Aug 2021 03:16:23 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 31 Aug 2021 03:16:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 31 Aug 2021 03:16:23 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 31 Aug 2021 03:16:23 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 31 Aug 2021 03:16:24 GMT
ENV MONGO_MAJOR=5.0
# Tue, 31 Aug 2021 03:16:24 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 31 Aug 2021 03:16:25 GMT
ENV MONGO_VERSION=5.0.2
# Tue, 31 Aug 2021 03:16:46 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 31 Aug 2021 03:16:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 31 Aug 2021 03:16:48 GMT
VOLUME [/data/db /data/configdb]
# Tue, 31 Aug 2021 03:16:48 GMT
COPY file:df3353d9b2c25ef83b499ecae7fd5d611adb4a9462a577435178acaad3c8c695 in /usr/local/bin/ 
# Tue, 31 Aug 2021 03:16:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Aug 2021 03:16:49 GMT
EXPOSE 27017
# Tue, 31 Aug 2021 03:16:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9e2375f5b5048fb0013ccb2e7290680c2590799520474598fe5ed6e21b3fa9`  
		Last Modified: Tue, 31 Aug 2021 03:20:22 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fc6079c33aea50db5ae3f5319d71f1cdf0b7d825e846d2d5d2051bddee77e6`  
		Last Modified: Tue, 31 Aug 2021 03:20:22 GMT  
		Size: 2.9 MB (2915391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e5461d9f2757a86731db084491d3c69e14f07c17810efd521d6aada80f86e2`  
		Last Modified: Tue, 31 Aug 2021 03:20:22 GMT  
		Size: 6.4 MB (6406210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249760dddaa1f69b0c9d1f8a23943c6d0eba70c05f68f93646af174928ab2ab7`  
		Last Modified: Tue, 31 Aug 2021 03:20:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94ab21b2c6a234bc42bd66502c16587a74d8a32f4a6e9ee43682ef83aa9420`  
		Last Modified: Tue, 31 Aug 2021 03:20:19 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acb3085c69e083aa0d451db77aa3c6bbf3203d22bcd2e86928c4f08e75dd8a6`  
		Last Modified: Tue, 31 Aug 2021 03:20:19 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eeed934852a8e456670af4eb68f5e89cbaacb05173abd6328b4a423e83659dc`  
		Last Modified: Tue, 31 Aug 2021 03:20:49 GMT  
		Size: 201.6 MB (201569076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e4b5b03a55bd1f09a42abd3b766841aabd3351ff4effc50ff1c20df20e3d9f`  
		Last Modified: Tue, 31 Aug 2021 03:20:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f71684ba4f6f0b50ec3af19175732b1641fb1c99434f93da957db2f5ad01fec`  
		Last Modified: Tue, 31 Aug 2021 03:20:19 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.2114; amd64

```console
$ docker pull mongo@sha256:d1592975df2f53e365352c4655ff95543776f3f87803222a1ae4eca3f9fcd4b0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2976772404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881b0b5e414a3c1a9d294850aa2e841cb216d9f9905ebbf008cb326abd8672c6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 25 Aug 2021 13:46:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 25 Aug 2021 19:38:11 GMT
ENV MONGO_VERSION=5.0.2
# Wed, 25 Aug 2021 19:38:12 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.2-signed.msi
# Wed, 25 Aug 2021 19:38:13 GMT
ENV MONGO_DOWNLOAD_SHA256=8c517e4b1598d627ee16c2dd45be90397bf040cf2845eef2aff0b9bc25062228
# Wed, 25 Aug 2021 19:40:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 19:40:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 25 Aug 2021 19:40:15 GMT
EXPOSE 27017
# Wed, 25 Aug 2021 19:40:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:985da5cbc0735e1c422e766af23125ba345f431cb337ea43ec32298d0bb8e4ea`  
		Last Modified: Wed, 25 Aug 2021 15:45:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658daa6e465de2e8f951f7cc7f7fc7bcac7946ca1d3a281ab8080f828ed47a95`  
		Last Modified: Wed, 25 Aug 2021 20:01:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53b88d0d8031cad96cddf85893e17fbcf1f81c7ecc57e35d89e5139f1a9f399`  
		Last Modified: Wed, 25 Aug 2021 20:01:57 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf20037e536db8e6ecf6ca661157a1a13428891172fec3b39e1b58a50a1146`  
		Last Modified: Wed, 25 Aug 2021 20:01:54 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1227c86fa7a71ea32cd31b6f7623bf109919d7be73af22a4bca0c302cfbe83d0`  
		Last Modified: Wed, 25 Aug 2021 20:02:45 GMT  
		Size: 290.8 MB (290765245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbc30f10f98aa8cfb33527e195657371709483ca7f3ac3823f37ba6633dd971`  
		Last Modified: Wed, 25 Aug 2021 20:01:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df248022067962cd2e97a4f5830c039784df486f4470d5479bcf74cb2b98f521`  
		Last Modified: Wed, 25 Aug 2021 20:01:53 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a2e173c76c2274f766c62c19c9459c263d9ca1e817fd332a4d2ceb096c96de`  
		Last Modified: Wed, 25 Aug 2021 20:01:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.14393.4583; amd64

```console
$ docker pull mongo@sha256:28fc771fc3e4cf094c86ef62e719a879cfa6ce994d84d212f23c3c69b8af9469
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6566098677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faac1ce88c047426be2b4ee87af431bd3ac3185dcae6b12f9cf2a57c3d7e9dc6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:59:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 25 Aug 2021 19:40:23 GMT
ENV MONGO_VERSION=5.0.2
# Wed, 25 Aug 2021 19:40:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.2-signed.msi
# Wed, 25 Aug 2021 19:40:24 GMT
ENV MONGO_DOWNLOAD_SHA256=8c517e4b1598d627ee16c2dd45be90397bf040cf2845eef2aff0b9bc25062228
# Wed, 25 Aug 2021 19:42:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 19:42:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 25 Aug 2021 19:42:40 GMT
EXPOSE 27017
# Wed, 25 Aug 2021 19:42:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a869803fc3d8292f0fe1bc6ed35e1ceedbd7c797a1486767a55f88c6c28ed4c5`  
		Last Modified: Wed, 25 Aug 2021 15:45:25 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae64dd51cae865b4fb1f2dff46a2a28c142afc717d2bf51d33fa91044f3b89c`  
		Last Modified: Wed, 25 Aug 2021 20:03:03 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a9fdae42abe869550529825a5ed22a28d10d7b723d1b1c36dd70a3c66f2087`  
		Last Modified: Wed, 25 Aug 2021 20:03:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11515d204e6c2d6b6ee5e319faca359304331db62af63ee66ee79110920df48a`  
		Last Modified: Wed, 25 Aug 2021 20:03:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96873d298adf1b77548a67c52c60bf53094d7152fedab2839da13ee2353c9c74`  
		Last Modified: Wed, 25 Aug 2021 20:03:52 GMT  
		Size: 295.1 MB (295123000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd183858c1b7762db7816f865b42952b23b8842785235492250805c2b1bf15a`  
		Last Modified: Wed, 25 Aug 2021 20:03:00 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9969cdae0a3da21fd9c98332f01a059a52048731d43587716a9c52b41a5eaff`  
		Last Modified: Wed, 25 Aug 2021 20:03:00 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795a58437c09d52d08db591ccbcc6a9fda4772573cbf4dafc72f943c01061d9d`  
		Last Modified: Wed, 25 Aug 2021 20:03:00 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
