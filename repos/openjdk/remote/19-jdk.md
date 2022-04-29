## `openjdk:19-jdk`

```console
$ docker pull openjdk@sha256:0a0a140d764801272ad5959be605a59e37e4d0353484c9c75e25e5942ee99435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `openjdk:19-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:2db8abbe64e4599c345d7201ad27f1552013890bf9b73e0744016d3c9009353a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250304497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d951ae0fc8426a01d0f032fc02d1ba33010f51e8a7c4b73fc145aa41e72ca9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 Apr 2022 20:33:04 GMT
ADD file:9893213a9ea238f53ac68d87a3cf2f05d86763688392e5ddb6a2c9b60d3550a6 in / 
# Wed, 27 Apr 2022 20:33:05 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 21:53:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 27 Apr 2022 21:53:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 27 Apr 2022 21:53:12 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 21:53:12 GMT
ENV LANG=C.UTF-8
# Thu, 28 Apr 2022 23:20:07 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:20:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='e5667a2a1208eb3042dd0c3187dd61d10b435204e4d26e466b8f2c7a5d988ce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ff38640a2b5097e460a7dd54544f0cbe19b041262549cd3d1015fc81eec50f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Apr 2022 23:20:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:38a980f2cc8accf69c23deae6743d42a87eb34a54f02396f3fcfd7c2d06e2c5b`  
		Last Modified: Wed, 27 Apr 2022 20:33:57 GMT  
		Size: 42.1 MB (42114164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de849f1cfbe60b1c06a1db83a3129ab0ea397c4852b98e3e4300b12ee57ba111`  
		Last Modified: Wed, 27 Apr 2022 22:01:52 GMT  
		Size: 13.5 MB (13525123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bae0712aa77f57dd22f58a1b35f94b1174142a6910c667af216df96df757af`  
		Last Modified: Thu, 28 Apr 2022 23:27:41 GMT  
		Size: 194.7 MB (194665210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:911bd18ba389dd105e0a192db39d3338caecac35bc23d0c9a26012a7435870e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249842434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c979330a8bf1e87ccdc9bd893457d12df1c76f90d594a650ac5647f8773bdf5a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 Apr 2022 22:55:53 GMT
ADD file:6fef7a4ab2de57c438dad76949e7eb87cfb1ea6f45b0f2423f71188efdaa0d8e in / 
# Wed, 27 Apr 2022 22:55:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 23:27:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 27 Apr 2022 23:27:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 27 Apr 2022 23:27:36 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 23:27:37 GMT
ENV LANG=C.UTF-8
# Thu, 28 Apr 2022 23:40:40 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:41:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='e5667a2a1208eb3042dd0c3187dd61d10b435204e4d26e466b8f2c7a5d988ce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ff38640a2b5097e460a7dd54544f0cbe19b041262549cd3d1015fc81eec50f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Apr 2022 23:41:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:416105dc84fc8cf66df5d2c9f81570a2cc36a6cae58aedd4d58792f041f7a2f5`  
		Last Modified: Wed, 27 Apr 2022 22:56:57 GMT  
		Size: 42.0 MB (42018977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe66142579ff5bb0bb5cf989222e2bc77a97dcbd0283887dec04d5b9dfd48cfa`  
		Last Modified: Wed, 27 Apr 2022 23:43:32 GMT  
		Size: 14.3 MB (14294224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263588035ef12c053d63139b01e65205443da2e49da1db558898c137a72fcb48`  
		Last Modified: Thu, 28 Apr 2022 23:54:32 GMT  
		Size: 193.5 MB (193529233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - windows version 10.0.20348.643; amd64

```console
$ docker pull openjdk@sha256:5682a21ade23205e3f7c170a4e7bcefd1137400d6d2ae94783e0f8b93474ae74
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2418495963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011c4ca85b5e580313c9b3a69d1bad1622260aecfbdb75a527f025fd1eb59148`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 16:55:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Apr 2022 16:55:45 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 13 Apr 2022 16:56:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 28 Apr 2022 23:16:08 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:16:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_windows-x64_bin.zip
# Thu, 28 Apr 2022 23:16:10 GMT
ENV JAVA_SHA256=6fdaa7ab6e357ec6e741643e70ba0e44802e9b3e1c45021bfcc649b3fc62a170
# Thu, 28 Apr 2022 23:17:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 28 Apr 2022 23:17:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c156288a763e09322f37d1214a5fcfaa1ebfbf8a108ee1351f5321537e137ef`  
		Last Modified: Tue, 19 Apr 2022 00:49:30 GMT  
		Size: 629.6 KB (629633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351bf1ac33e20763f11b363ce89dc94a0246c9fba4a48c2ad7f54cc49702ec37`  
		Last Modified: Tue, 19 Apr 2022 00:49:30 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48226228ba4f77ff2595c0eb2da5dbff7a0c255e2945283b32a4a6432b6a5c6`  
		Last Modified: Tue, 19 Apr 2022 00:49:30 GMT  
		Size: 559.7 KB (559710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1280ef159ecf6e09b0cde4f7957af8bb59c5363a8731726f38079e4e9a55ce8f`  
		Last Modified: Fri, 29 Apr 2022 04:21:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c60af4aca03e3db789ddc365a622d64497c9abe8a9c7386eec739f5036b5847`  
		Last Modified: Fri, 29 Apr 2022 04:21:02 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc10ae1c6796225fec22bc0198e46b9362aa67021aabc53da487a2cd3c6dbcf`  
		Last Modified: Fri, 29 Apr 2022 04:21:02 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048163ea83cf5d6f599d573a6eb729e76436e33405a531afc7ea2774f7854579`  
		Last Modified: Fri, 29 Apr 2022 04:24:31 GMT  
		Size: 190.3 MB (190343286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bca1e1509425b50f3a7c0cff53ec8e065e1f0ab37b64dd5548c8555e01bccc`  
		Last Modified: Fri, 29 Apr 2022 04:21:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - windows version 10.0.17763.2803; amd64

```console
$ docker pull openjdk@sha256:76911a5c2847b633c6f5eab88866ebe8bed3e981e6f5abb9df0cb289c21f4caf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2906729656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3385203bccbe3aaf7fa417611e8af9aa30ba856fdc4bc4fa74be22667c674ca8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 16:58:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Apr 2022 16:58:07 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 13 Apr 2022 16:59:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 28 Apr 2022 23:17:36 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:17:37 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_windows-x64_bin.zip
# Thu, 28 Apr 2022 23:17:38 GMT
ENV JAVA_SHA256=6fdaa7ab6e357ec6e741643e70ba0e44802e9b3e1c45021bfcc649b3fc62a170
# Thu, 28 Apr 2022 23:19:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 28 Apr 2022 23:19:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25b7048e3be90e8d3856a943edfe91e214649883ffeabdf6fcebcea7b3053e2`  
		Last Modified: Tue, 19 Apr 2022 00:53:10 GMT  
		Size: 366.7 KB (366674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f218e98479db3f32c0db578928d63948fc1a4d83a3525921b9f9a7f4c999de53`  
		Last Modified: Tue, 19 Apr 2022 00:53:09 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4898bdb62896a1acbb34025e03c775d3d5f0f7299ae3f01875842d74e0e7984b`  
		Last Modified: Tue, 19 Apr 2022 00:53:10 GMT  
		Size: 322.4 KB (322423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df330f932d18bc6f73efeccb0de955303ccb3fda908249497dc84f863b9b937`  
		Last Modified: Fri, 29 Apr 2022 04:24:53 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e7f3696cf6e43d59dc4af5143d8ca0f7bc9c3e3bc25213410b7e2031e4e088`  
		Last Modified: Fri, 29 Apr 2022 04:24:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a64f59a2977c8df1e5022facdcfef8dd738cebe6066691efab6315c442f9d3`  
		Last Modified: Fri, 29 Apr 2022 04:24:52 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185f9ac4d970bee609aa9c3f817e543355d4d973bc503a145609bcdc618ed2d2`  
		Last Modified: Fri, 29 Apr 2022 04:28:21 GMT  
		Size: 190.1 MB (190111720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8035dd50ad45d5969b2a6d731ce98e4ec987e3f7671a6f61ccc7f9a7983b02d4`  
		Last Modified: Fri, 29 Apr 2022 04:24:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
