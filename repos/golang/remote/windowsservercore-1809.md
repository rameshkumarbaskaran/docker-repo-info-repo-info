## `golang:windowsservercore-1809`

```console
$ docker pull golang@sha256:36475dc72be93196db1868c0a68a155b5212ec1551bd58e7e511f8c91c5f58f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `golang:windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull golang@sha256:3c46c8d76721128cb640dc59bf25797e4ce51b3e313fb897f2a7fdfd74b276f1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1877390975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87625ef88d819b59e88614173dd5d178ea38c5d22d42e33039b571ea93038ff8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 12:41:47 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 May 2020 12:41:48 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 May 2020 12:41:49 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 May 2020 12:41:50 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 May 2020 12:42:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 May 2020 12:42:47 GMT
ENV GOPATH=C:\gopath
# Wed, 13 May 2020 12:43:08 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 May 2020 12:43:09 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 13 May 2020 12:45:37 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1b5a60b3bbaa81106d5ee03499b5734ec093c6a255abf9a6a067f0f497a57916'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 May 2020 12:45:39 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab29cecca7bcbda2c597002df3455f14ecd6e1e255624faeb782851f5808e123`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beddff0184164c7525ffdf35ba620099ed0de8e34ee5eac9feba1b3d1f6d8b08`  
		Last Modified: Wed, 13 May 2020 13:00:16 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d62d5306f69de301a3da0098e43f6877bcd793751aa69649fbf153e5b80844`  
		Last Modified: Wed, 13 May 2020 13:00:14 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b7f47046d1b96f631bced4b78ab3533856931a0b17151ecd686fc696a38daa`  
		Last Modified: Wed, 13 May 2020 13:00:15 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485f15f0f01c8b67ae80b392c731ed4f6e8f9ece9080f4d51837906b5e001246`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 25.4 MB (25433290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777191637dda5a3401ae57c057af755a1c87b5c2b168786119f18def6d77a43b`  
		Last Modified: Wed, 13 May 2020 13:00:10 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea1f3b8205267e65831ebb254905af6cfc8a9fc30840f0f1556fd86ea6f8bca`  
		Last Modified: Wed, 13 May 2020 13:00:10 GMT  
		Size: 305.5 KB (305481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730a3346fef2d984ec206269248b29425c4374eed5ac16189f2792f4c04ac914`  
		Last Modified: Wed, 13 May 2020 13:00:10 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2d677d1225984c602388b19c35c9f1d99f82bac962b69fc4e1f6977e525265`  
		Last Modified: Wed, 13 May 2020 13:00:41 GMT  
		Size: 133.3 MB (133309924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcd46a0b76ccdd65dd76d268b6f5f1a49fa4994678a4576ca53e92db3ec0843`  
		Last Modified: Wed, 13 May 2020 13:00:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
