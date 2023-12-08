## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:b944570c2f667cfb312913d3478de80037fe9967f6fd20a1358e3f1b87467164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:b1d94a17104c4814aa7672316e4c713aefcdfa6ffd19043f4111784c09931cda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983623336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61ba19fe8fdfa90a532d1f355b356c651a2921264135f6417c72193a5f37396`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:43:34 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:43:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:43:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:43:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:44:11 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:44:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:15:35 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:17:49 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:17:50 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 21:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 21:00:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:21:33 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:21:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1d4a557f047b695f94452d9707061981d7fae4239c674b332282b8291963c`  
		Last Modified: Thu, 16 Nov 2023 03:11:20 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45549c207f14d769cba7c36b66157ec213bbc32ce57d685d8e2c407cf3987bb`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674717e06bf8cb25d5887393ef9568ee0ab6390966b9666808e836e9bd471d`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2227badcd9f5f2b70b3d2ffd1c18887498f413c07802bfb334e8dc7b2d2acc`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f3b5e90a2e6028cf194e870b24a7158f875f18b81f4f9137a5db3ea1f79ac`  
		Last Modified: Thu, 16 Nov 2023 03:11:23 GMT  
		Size: 25.5 MB (25536225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7811a5416dcd19193a5b3ab9327607bf845f7ff77f95d3e20abdfb7435c32ae0`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5931209e960a94616639ea72e4d3ad9dc9cb554790ce930152c73bdc1449c034`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 266.6 KB (266600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a70f603a2fb4e76edd3165b62a179fb8f6410e265f5ae4a3732ee68e610034b`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e37840dec3a6665ce48520be8b2c51b654359765bee5ab0780ee74746f0eb2`  
		Last Modified: Tue, 05 Dec 2023 20:39:08 GMT  
		Size: 69.3 MB (69342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d16ae54757acda093616d24735d4c92d4676649bec49807fc35de90d15e15c`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5744d01eddd2ef9d9673fdb0f0e48203fad1b01f2b14899a3ec6393c4548e75`  
		Last Modified: Tue, 05 Dec 2023 21:02:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35bb848667aa413b6ce6c309a4c2169635b0740dc335b9b39413a00627c01ab`  
		Last Modified: Tue, 05 Dec 2023 21:02:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630e9807bbb8995ce52459e6e3c8d818351c481e0ce29280570e90d0138d33`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15ec018ec91e33ee96d4f0e6b66d9edb40b185a13f91d16f12d0bf682ab08b`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79cc8b934303f209cd48271252cb46966445a1099aac277ae4caf120af718ab`  
		Last Modified: Fri, 08 Dec 2023 20:23:49 GMT  
		Size: 1.7 MB (1677815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f75043e75fb7c85d3daec88a29069c6ff40b8feeaa26bac868d524758955`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
