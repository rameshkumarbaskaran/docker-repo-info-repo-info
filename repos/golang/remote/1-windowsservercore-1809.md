## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:b391ce94f7710cf1b3e4f32c4c7e0433c059f3806bec220c7765d27ea043e886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull golang@sha256:df6a9e3fa685d49165b47467aa052e5c74b1c7200cdd2bbadb9faab4008c9733
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2857832976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d9e3617fa7b3c5e603319a4e1d2f0be606dad868916ce09b1fc2ff88de1a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 12:24:47 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Sep 2021 12:24:48 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Sep 2021 12:24:49 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Sep 2021 12:24:50 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Sep 2021 12:26:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Sep 2021 12:26:02 GMT
ENV GOPATH=C:\go
# Wed, 15 Sep 2021 12:26:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Sep 2021 12:26:50 GMT
ENV GOLANG_VERSION=1.17.1
# Wed, 15 Sep 2021 12:29:31 GMT
RUN $url = 'https://dl.google.com/go/go1.17.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '2f2d0a5d7c59fb38fcacaf1e272cf701bb8c050300ba8b609fc30d2c5800f02e'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Sep 2021 12:29:32 GMT
WORKDIR C:\go
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
	-	`sha256:7df95d283f38510b566a89cdc28ca1b0a2438f52bb9d42e379d2932f514e81be`  
		Last Modified: Wed, 15 Sep 2021 13:00:40 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0abf7bec76e064c3d49f7a594e9008d1c75a172eecc2b793ced99c77c9c77aa`  
		Last Modified: Wed, 15 Sep 2021 13:00:38 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68963a99150702ae64dba60fe0001260a4041019c1cb04c27f5be8d555a0aea`  
		Last Modified: Wed, 15 Sep 2021 13:00:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6245724834e44ef992bdf261c9bb4d35a507434af9ccd3b0a99ed93de6ec36db`  
		Last Modified: Wed, 15 Sep 2021 13:00:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e9acc2ca31d64c2f460a41ae307033a0b4534da67568287b2c57a8b6adf0f2`  
		Last Modified: Wed, 15 Sep 2021 13:01:04 GMT  
		Size: 25.4 MB (25442862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cbdd322efcb8b015e7a68beb6210682d71efcfe68c64b70abf7aa47f5a58d3`  
		Last Modified: Wed, 15 Sep 2021 13:00:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb20bca5389066bf8009801141c70732d96038bb176ce80e932d8d8dad391659`  
		Last Modified: Wed, 15 Sep 2021 13:00:35 GMT  
		Size: 320.1 KB (320056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a84248c33aa17110a0f6d967386a5c2a1ea95d49605bea91561aff7d169172`  
		Last Modified: Wed, 15 Sep 2021 13:00:35 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b9eca5698fe3ad6241e9326040eebf831ade7114ad0602220c0a4e89d33a5e`  
		Last Modified: Wed, 15 Sep 2021 13:01:07 GMT  
		Size: 145.4 MB (145360971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0ddecc5a00ee2f93392f5db3581babd9936446768867f3f297aa8adc195b6f`  
		Last Modified: Wed, 15 Sep 2021 13:00:35 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
