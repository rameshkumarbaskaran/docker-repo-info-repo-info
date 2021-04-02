## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:707fee0b94dcb8bb07e1cc0f86e10c540509ee572b69240bc0556cfafa586cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4283; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4283; amd64

```console
$ docker pull caddy@sha256:017255652cc26ea2af428ecc3b6f2222ee64d88cfdf1c34e3522f048aa461ee9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5997836720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a9fde1e66982a65a46dea5c07548ac8afcd29b6f304afe23a8ea9bcdcf186f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Mar 2021 18:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Mar 2021 13:42:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 13:42:06 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Mar 2021 13:42:07 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Mar 2021 13:42:08 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Mar 2021 13:42:09 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Mar 2021 13:44:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Mar 2021 13:44:32 GMT
ENV GOPATH=C:\gopath
# Wed, 10 Mar 2021 13:45:47 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 02 Apr 2021 00:28:41 GMT
ENV GOLANG_VERSION=1.15.11
# Fri, 02 Apr 2021 00:32:35 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 02 Apr 2021 00:32:37 GMT
WORKDIR C:\gopath
# Fri, 02 Apr 2021 01:04:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 02 Apr 2021 01:04:14 GMT
ENV XCADDY_VERSION=v0.1.8
# Fri, 02 Apr 2021 01:04:15 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 02 Apr 2021 01:04:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 02 Apr 2021 01:05:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 02 Apr 2021 01:05:45 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30bda99601c5cbd3b2118409f401852ea648e2319bd81518723e476b28d764c5`  
		Size: 1.7 GB (1726924885 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76680da9dc6db108ddf2e353c494b45e8486a6751619a13ed8fb3ad64b9a16e9`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2092de86b10f822dfd3a0d8e8dc35924823393cf8301e6db8f8a0a2879fb18`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ac6e05dba1a284b10130ada4ed7581f5a1c5a90986038e31cc8213e215ca23`  
		Last Modified: Wed, 10 Mar 2021 14:06:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a636ee1e87a6b10caeaef03b68f084d58b5c8412fe4b10ba5d851a6965917196`  
		Last Modified: Wed, 10 Mar 2021 14:06:01 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e03ef5102108f3595c37759ead10b0cfb624aa0f102dbae3b6abb18f03b56`  
		Last Modified: Wed, 10 Mar 2021 14:06:01 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840634d0d343cc458ff1f028b165fab14415bf252ce2b7fdb726c41d035c64ff`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 35.3 MB (35273703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b968b2b2cb37afe5893ed1aa040b1055605f41e8371fe42fca9c6e06bb96c2ed`  
		Last Modified: Wed, 10 Mar 2021 14:05:55 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b01350c0465bbc3ff96b788fef94740af9378a1cfe9f3c1fb50ffed30c8a7ad`  
		Last Modified: Wed, 10 Mar 2021 14:05:59 GMT  
		Size: 10.1 MB (10139029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a055a610a3b2e63b54d561bc3512bd068b4443a7417486b9dc65a4ad292583c7`  
		Last Modified: Fri, 02 Apr 2021 00:44:26 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c202a262d335726e6d079774ca9e11f52da7326ee18860265595a97527a7b545`  
		Last Modified: Fri, 02 Apr 2021 00:44:55 GMT  
		Size: 144.0 MB (143966864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737da401effa5536406d2508db65af6f54d9be0a3c5f1347ae56dc5ad1b8c1a4`  
		Last Modified: Fri, 02 Apr 2021 00:44:26 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c52d85af463d5a66468c058122750336a2d002544c19dbaff721875cb8c6c24`  
		Last Modified: Fri, 02 Apr 2021 01:09:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f1bf71cbf1adab82ad5a9d8f5b71571306bf6bcf254b686963f2ed7562e7fc`  
		Last Modified: Fri, 02 Apr 2021 01:09:44 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba22c0fd4b07e8d5ff2ab18028eb3f4d87c20420e43a2afbf78c8da9032399b2`  
		Last Modified: Fri, 02 Apr 2021 01:09:44 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562b238ffe2f30d1bebcac0de5c7d019504926664c08f5730389c7c1e426c12a`  
		Last Modified: Fri, 02 Apr 2021 01:09:44 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0b00fc7a9cc9546977571c1922da63009fc89865ee5ae6b603cdf38d5b56ad`  
		Last Modified: Fri, 02 Apr 2021 01:09:47 GMT  
		Size: 11.5 MB (11528518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606193453afd7f6b2c5d21cdd640e297c0e3b0514642cc7044ff5a83ef6e66c7`  
		Last Modified: Fri, 02 Apr 2021 01:09:44 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
