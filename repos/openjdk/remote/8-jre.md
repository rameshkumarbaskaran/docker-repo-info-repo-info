## `openjdk:8-jre`

```console
$ docker pull openjdk@sha256:7bea97f6ff5d8c477903a27434da37ff39863d8beac30efca053818b43276762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2183; amd64
	-	windows version 10.0.14393.4651; amd64

### `openjdk:8-jre` - linux; amd64

```console
$ docker pull openjdk@sha256:111cdaa7fc894acdf0b172f5665cdc33214a87548b6dbdcbee413f46019ace2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117964203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c45f8d078ff59ab3032958af7ca0fbd57b7924129027f86e6fd3a32223b5890`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:07 GMT
ADD file:1fedf68870782f1b44cd50691444aab4061cc0c70f24e5fabe9c562cc46eb9af in / 
# Fri, 03 Sep 2021 01:21:08 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:31:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:31:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 08:39:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:42:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Fri, 03 Sep 2021 08:42:23 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Fri, 03 Sep 2021 08:42:24 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 08:42:24 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:42:24 GMT
ENV JAVA_VERSION=8u302
# Fri, 03 Sep 2021 08:42:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
```

-	Layers:
	-	`sha256:955615a668ce169f8a1443fc6b6e6215f43fe0babfb4790712a2d3171f34d366`  
		Last Modified: Fri, 03 Sep 2021 01:26:55 GMT  
		Size: 54.9 MB (54926871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2756ef5f69a5190f4308619e0f446d95f5515eef4a814dbad0bcebbbbc7b25a8`  
		Last Modified: Fri, 03 Sep 2021 06:39:22 GMT  
		Size: 5.2 MB (5153100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911ea9f2bd51e53a455297e0631e18a72a86d7e2c8e1807176e80f991bde5d64`  
		Last Modified: Fri, 03 Sep 2021 06:39:23 GMT  
		Size: 10.9 MB (10871687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1918195b7da3406545d23e584aeb307c0ef2d97fc09a8e85fc30e97a3602bf`  
		Last Modified: Fri, 03 Sep 2021 09:03:46 GMT  
		Size: 5.7 MB (5653792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c57183dafd260851f8ed01bb75b476cfee970ce2cce3cd8320f8380187929d`  
		Last Modified: Fri, 03 Sep 2021 09:07:23 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d70515740dfe345f66c496a767f231b388faf1dcc13485ddc5cd9485463f37`  
		Last Modified: Fri, 03 Sep 2021 09:07:29 GMT  
		Size: 41.4 MB (41358544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jre` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7d2f3996def2bd95d01d99d29a9b846463e5117ee64ea8845c2e0f818d7c1e8d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115891165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7e6cb6521a63a3cb2f6318e2ee20f745453e1f4d674cd05889a95a865eed73`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:18 GMT
ADD file:0b1ff9dcb90d6b787179d2e43ca534c39e0372227a3af198bab158a89fb2c966 in / 
# Fri, 03 Sep 2021 00:40:19 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 10:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 10:54:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Fri, 03 Sep 2021 10:54:36 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Fri, 03 Sep 2021 10:54:36 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 10:54:36 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 10:54:36 GMT
ENV JAVA_VERSION=8u302
# Fri, 03 Sep 2021 10:54:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
```

-	Layers:
	-	`sha256:ffacddc51d82196acb1d49f2e3c13601fc16c61c995a860b450d23b000353ca1`  
		Last Modified: Fri, 03 Sep 2021 00:48:17 GMT  
		Size: 53.6 MB (53613054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f80252dfabbfc5bdf4862b9fa8d2de7110ac4a6f08bf30e6f574f6243d0c93d`  
		Last Modified: Fri, 03 Sep 2021 04:40:56 GMT  
		Size: 5.1 MB (5142543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138e2c18ad04e197e8431cfc2923456979d5b0cfb9c6549a62bcd3732d77bd03`  
		Last Modified: Fri, 03 Sep 2021 04:40:56 GMT  
		Size: 10.9 MB (10872696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a57001d0fde6c8ddb9c29c60734a0bb80875425833e4890dfa80dc87809735`  
		Last Modified: Fri, 03 Sep 2021 11:16:53 GMT  
		Size: 5.6 MB (5647293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cfcb08baf48151efa83fb9a6ded570e26d3a60a860e2304277c038e0814961`  
		Last Modified: Fri, 03 Sep 2021 11:21:08 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98bea2d04ac6ea7d95be7db7d574d1730f7fa14276d79816f454111564c0f4e`  
		Last Modified: Fri, 03 Sep 2021 11:21:13 GMT  
		Size: 40.6 MB (40615370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jre` - windows version 10.0.17763.2183; amd64

```console
$ docker pull openjdk@sha256:04a87e6d9c6225a47be196568a0b6310b40efafa0d96bc8b99c614a032095f60
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2725947326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da39d6e6e8a6e86a232c9b299818c0990ccdc12d5ad25bf176befd27ab5a146d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 00:31:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 Sep 2021 00:58:52 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Sep 2021 00:59:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 15 Sep 2021 00:59:43 GMT
ENV JAVA_VERSION=8u302
# Wed, 15 Sep 2021 01:04:27 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_8u302b08.zip
# Wed, 15 Sep 2021 01:05:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d714779fd458636d1b2289ae98777c0c8707a28708bffccab0b1314b59d77c`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 356.1 KB (356133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9998cfbf545427a53752bf7f902eda63cf98803f0f62c60a0eed02e19d37b118`  
		Last Modified: Wed, 15 Sep 2021 01:26:48 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69b63e938990f7d42d7e7be027d18606660968ded7aea5aeea6bd41758d9c95`  
		Last Modified: Wed, 15 Sep 2021 01:26:48 GMT  
		Size: 315.7 KB (315723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95c82487d9cf9b5e66221f693ea13cd0d7ebfe4126d371da0e3a820296db24d`  
		Last Modified: Wed, 15 Sep 2021 01:26:48 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e729a09cd654b255f750576e5f6170fbd9d0a491225ffe3d1fb8c80c2f1acf`  
		Last Modified: Wed, 15 Sep 2021 01:28:05 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04052eef6ce4db287d508f0db4d52771589063e43a231f700ac02746193514f8`  
		Last Modified: Wed, 15 Sep 2021 01:28:10 GMT  
		Size: 38.6 MB (38572002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jre` - windows version 10.0.14393.4651; amd64

```console
$ docker pull openjdk@sha256:c4e285fb36121cc76928d7a414c207a7e42dfcd4d0f13f4bdd8e4a4469843df6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6310561125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6790fa214102ade7499f018478159204c9d97d2b9abefd630504cbe68272384e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 00:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 00:35:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 Sep 2021 01:01:17 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Sep 2021 01:02:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 15 Sep 2021 01:02:14 GMT
ENV JAVA_VERSION=8u302
# Wed, 15 Sep 2021 01:05:38 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_8u302b08.zip
# Wed, 15 Sep 2021 01:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8721f004192f15fe71b8626ef3f3e34cbf2cfe1d15a63b6b544ab946162ef707`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b794d0a07a41196dae8678e4ecbb9a5766d6db31f9729bfe3f1d83963af3e0`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 339.2 KB (339172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c1f344e0222373968e87d0c3fbe3d9a5aed9d026ee90d28e8eab0fdf9a3144`  
		Last Modified: Wed, 15 Sep 2021 01:27:13 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae30094a4b1b2f3f76d86ef0aa8a23200a08d345879a9a5c5a7664b1d79a1e9`  
		Last Modified: Wed, 15 Sep 2021 01:27:13 GMT  
		Size: 328.7 KB (328675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995f2a34e252d4ec7fc3d8ded958122942d4d83b2e1e018821b5be28d9cda692`  
		Last Modified: Wed, 15 Sep 2021 01:27:13 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91577608c3de1594346d0f0c6cfb1239910e0629818406e884e8601dfd22b08`  
		Last Modified: Wed, 15 Sep 2021 01:28:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4743e953dd269817e80a1bb22819948ceca4d47111d4268895fc070ff7f7321a`  
		Last Modified: Wed, 15 Sep 2021 01:29:00 GMT  
		Size: 38.6 MB (38559610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
