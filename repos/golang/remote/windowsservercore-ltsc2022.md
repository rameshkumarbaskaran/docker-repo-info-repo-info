## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:00aab6ac885a878c119cabc2009228128e71006f618b69e9fbc65df15cb69663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull golang@sha256:647b841b8cc8b449ebd00e2774b7fcc8753d7053dd83227c11c306d956662f00
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1909669428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d55e6ed2e19880c46cc905d5c21776c8103ec5e4853fed33d75b0173c5a673`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 01:19:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 May 2023 01:19:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 May 2023 01:19:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 May 2023 01:19:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 May 2023 01:19:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 01:20:00 GMT
ENV GOPATH=C:\go
# Wed, 10 May 2023 01:20:22 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 01:20:23 GMT
ENV GOLANG_VERSION=1.20.4
# Wed, 10 May 2023 01:22:38 GMT
RUN $url = 'https://dl.google.com/go/go1.20.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e7528da720f470b711fbd826814167a5fe1bc02a479ab1958dcf839a8294e6d2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 01:22:39 GMT
WORKDIR C:\go
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
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a5817a4fb4758348ab4368724df2dc391387df461e1a8d85ce78b44e62941c`  
		Last Modified: Wed, 10 May 2023 01:45:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dab590dc88f85f33daec526784c193cc1c9b17e7b5698c2c2062f2834024c6`  
		Last Modified: Wed, 10 May 2023 01:45:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f079b4dc01fb29bd7fef59856746267beedc000a15ee3384aae24b0611e20ca5`  
		Last Modified: Wed, 10 May 2023 01:45:24 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079e97ba795ef33077d3adec29756d746b1770b10fd4625881edcef794037e1c`  
		Last Modified: Wed, 10 May 2023 01:45:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb79b38ccc75aeae87db4cf726d0dca1e9d555cd554c4556b9968117ef8f7cbf`  
		Last Modified: Wed, 10 May 2023 01:45:28 GMT  
		Size: 25.5 MB (25531790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd856add23470d3d95bee9f5f2ece447db6ec28e58975639ca4a4d7633ca09b`  
		Last Modified: Wed, 10 May 2023 01:45:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e2692a8e8e09064af3cb6bbd4e5562607b52cf8ed9fa0aa22c9bc50a7117ae`  
		Last Modified: Wed, 10 May 2023 01:45:22 GMT  
		Size: 264.1 KB (264060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc66119745b33b0a20bc0491b46d73b61bd8a4a47a5cfc59162796dfff09c60`  
		Last Modified: Wed, 10 May 2023 01:45:22 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240227f2d5d2bbdae1a7f550a08a8ac9db8cf4d7b4770ee94f6bc41634b4ea6e`  
		Last Modified: Wed, 10 May 2023 01:45:45 GMT  
		Size: 108.9 MB (108881085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e76ee5f16685fd53c5826b56d98b837a8ab1174726d51a23b3fe815f40d12`  
		Last Modified: Wed, 10 May 2023 01:45:22 GMT  
		Size: 1.6 KB (1565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
