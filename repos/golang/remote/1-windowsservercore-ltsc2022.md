## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:d2eee5705fc8b910d2b6597c6b0588c296c818bd7290346e0fd8f2bc5645d6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull golang@sha256:d0ac7f10a7a535acb092a652226a71a8ab54613eb225f6cc752bd5e41faf18e7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2679675700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238556e505c6a50286acf7c0fc4159905993337b480693f24c8dcb7b43e3fa09`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 09 Dec 2022 09:36:47 GMT
RUN Install update 10.0.20348.1366
# Tue, 13 Dec 2022 22:45:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Dec 2022 00:13:55 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Dec 2022 00:13:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Dec 2022 00:13:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Dec 2022 00:13:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Dec 2022 00:14:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 00:14:46 GMT
ENV GOPATH=C:\go
# Wed, 14 Dec 2022 00:15:18 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Dec 2022 00:35:15 GMT
ENV GOLANG_VERSION=1.19.4
# Wed, 14 Dec 2022 00:39:13 GMT
RUN $url = 'https://dl.google.com/go/go1.19.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ada490e188bfb57c7388da7c5eba7565390992b6496204d30e710d37755956b0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 00:39:14 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa20ce142ecceb471dc070d9582fff942cef447b7c8ff22f2223ffe3737c99`  
		Last Modified: Tue, 13 Dec 2022 23:54:14 GMT  
		Size: 1.0 GB (1021665190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb8b9a4ec3ca516cfaa44f64e80b1e3aaecdbde870177411ff046f81f991dd2`  
		Last Modified: Tue, 13 Dec 2022 23:51:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e949ed00a67bfedd910770b630dc901df3b74f58d6755b55714def7d6710d`  
		Last Modified: Wed, 14 Dec 2022 01:11:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5eb5b41928124d94b99e548d8010c06fa5a01ddc4965df09a0a45de870fd602`  
		Last Modified: Wed, 14 Dec 2022 01:11:56 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf6c5652a34a0b006bbaabc715acea90b976298b71368163a4c825ca557df68`  
		Last Modified: Wed, 14 Dec 2022 01:11:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31770cf797a116c54aabbc41c4ce0a1fdd94b455881fad04c47fb8e035443a52`  
		Last Modified: Wed, 14 Dec 2022 01:11:55 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5d864bf59b78f6d1db2f91bee0c4f7959333189bb8c4a7a9c26402ac824ac3`  
		Last Modified: Wed, 14 Dec 2022 01:12:03 GMT  
		Size: 25.7 MB (25660561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318f13fe4094e65caf46f5d176223522e26763a1841252e6d76f5a68a3c816c5`  
		Last Modified: Wed, 14 Dec 2022 01:11:53 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7cbf5baf91a376e73bdb128ea3a0678267ed8fd1f560b300225eda3349da34`  
		Last Modified: Wed, 14 Dec 2022 01:11:53 GMT  
		Size: 514.5 KB (514472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea746f6c7963f52eb12946e492ef1328ce5d0a0ac9d21805c6da981b22f51d0`  
		Last Modified: Wed, 14 Dec 2022 01:14:53 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd1e5597f5d101d6fc3b28e86d230762773975a3108d109a6ab0ffba69f3c1`  
		Last Modified: Wed, 14 Dec 2022 01:15:46 GMT  
		Size: 157.8 MB (157826391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6441302a12d424defc481b75ea33cfd061edcc05ffb44aafd7819166aaa4201`  
		Last Modified: Wed, 14 Dec 2022 01:14:53 GMT  
		Size: 1.5 KB (1542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
