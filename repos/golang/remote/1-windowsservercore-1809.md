## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:74797120cac57694b971fab8083198ffd0f2c3392cf292b4748bb47b5fe9f1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull golang@sha256:8f59f4209bc31f6904389f11733928a3ad3240830f2d64c071e0ea43ebe1134b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206720025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519bbfc2d064a479d17f71ccfaa2b9f7cbedc22efb656cf99e52ddea812e4ad6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 01:22:55 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 May 2023 01:22:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 May 2023 01:22:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 May 2023 01:22:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 May 2023 01:24:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 01:24:15 GMT
ENV GOPATH=C:\go
# Wed, 10 May 2023 01:25:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 01:25:20 GMT
ENV GOLANG_VERSION=1.20.4
# Wed, 10 May 2023 01:28:23 GMT
RUN $url = 'https://dl.google.com/go/go1.20.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e7528da720f470b711fbd826814167a5fe1bc02a479ab1958dcf839a8294e6d2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 01:28:24 GMT
WORKDIR C:\go
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
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69c8e1c8adec95ce194194fafcfc6a1e07f15344588a0b08f7f625c5a547434`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47736757cd8e844fa5669cb79caf4053a95eb6b57e09dd4ab01823f071f92f24`  
		Last Modified: Wed, 10 May 2023 01:46:45 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd4aa96423c060d9cbb5c55c535627e8c1e46ba89f752a3d601450afe81b5b8`  
		Last Modified: Wed, 10 May 2023 01:46:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f8de560673af047f7136635e2e62927f8f69d11a928140de06383e86fb295`  
		Last Modified: Wed, 10 May 2023 01:46:44 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8138b5cc05a953f350e06a0713c2c031257b514bb362629f520d00db71fd7`  
		Last Modified: Wed, 10 May 2023 01:46:49 GMT  
		Size: 25.5 MB (25530178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814a31d39859b5f50d901390aa5410b00f1637dce1a5839d12e69722fab50294`  
		Last Modified: Wed, 10 May 2023 01:46:42 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05276aaa698fd9d43e2a1961637e16578fa84a5128237d7c2bdfe57c54fa89`  
		Last Modified: Wed, 10 May 2023 01:46:42 GMT  
		Size: 262.2 KB (262162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3734828ef55699f77b7686172c89a9ddbfa6c7d7df35e5608bcb63248792fc2f`  
		Last Modified: Wed, 10 May 2023 01:46:42 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713486e6c97a59ac1a7d96bfe00885c5591238a7c5f55b2d6baee0ce6a02e9dd`  
		Last Modified: Wed, 10 May 2023 01:47:05 GMT  
		Size: 108.9 MB (108881087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab53917aeeb5148bb38ff14d0a2a6854191a27519ffdd95b1d86bde2060768e0`  
		Last Modified: Wed, 10 May 2023 01:46:42 GMT  
		Size: 1.5 KB (1540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
