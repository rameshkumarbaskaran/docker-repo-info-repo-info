## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:1ea950c78a75f48532e163bcb5b49cf0f72544c6cc09296e85d4f36681eb64f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull golang@sha256:a343bae15d6de68b43fbdffa6110ee2e066691c9054251d5ceaeee082174a689
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2152566679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ca19ccde679005aa552fef5cf4d6316886eda1171f6cc90636449190134eb5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Nov 2023 02:49:42 GMT
ENV GOLANG_VERSION=1.21.4
# Thu, 16 Nov 2023 02:52:53 GMT
RUN $url = 'https://dl.google.com/go/go1.21.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '79e5428e068c912d9cfa6cd115c13549856ec689c1332eac17f5d6122e19d595'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:52:55 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30930da8ed1e8bdc54250c940331ca68cda0bfb62284a10c659fbd0768848ea`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d113e76a38d50789cec61e62343c448b0f781f2edc2150f8abe914796df72325`  
		Last Modified: Thu, 16 Nov 2023 03:12:14 GMT  
		Size: 69.3 MB (69322889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e233c1968dbb3ae85985bbd8b98ec9454199ca20141c642a7884444c1bc7c7`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
