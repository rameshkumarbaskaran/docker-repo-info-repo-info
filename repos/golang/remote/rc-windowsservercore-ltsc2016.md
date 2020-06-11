## `golang:rc-windowsservercore-ltsc2016`

```console
$ docker pull golang@sha256:335ceb7fcb28876c91bf83fdd580c967b4e0069f86a77d03e339bdc6e2e53360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `golang:rc-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull golang@sha256:c3f944ad2c184bf43366bfce4c593580b3bf28964f6809149fc15763afe7e727
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5913541927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbf8ce847783fd6249b87396729b6094fc9b3567555f6c3e5ac4cd5a18fbc3b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Jun 2020 22:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 12:12:16 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jun 2020 12:12:17 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jun 2020 12:12:18 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jun 2020 12:12:19 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jun 2020 12:14:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 12:14:02 GMT
ENV GOPATH=C:\gopath
# Wed, 10 Jun 2020 12:15:24 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 11 Jun 2020 22:15:39 GMT
ENV GOLANG_VERSION=1.15beta1
# Thu, 11 Jun 2020 22:19:56 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '072c7d6a059f76503a2533a20755dddbda58b5053c160cb900271bb039537f88'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 22:19:58 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c938241e0507e1ada5f864325483d86fd08533a5a31e7cb6ec1357db9891b245`  
		Last Modified: Tue, 09 Jun 2020 23:18:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e55345ed04421345a2308c193cd2b3ee2ea2d1d03c6aca6dca476e6ac5fdf`  
		Last Modified: Wed, 10 Jun 2020 12:38:10 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28f74567e1ed23ec88993e7f0c8edb9457f0052976cafb0ba244f71acdafc`  
		Last Modified: Wed, 10 Jun 2020 12:38:09 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d9d2adaa155205462f0838c91c10c4c471332d52fd8f09d6715c18271fcd56`  
		Last Modified: Wed, 10 Jun 2020 12:38:06 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daaae427663ac308e774d70aea7aa07c3e014b28ac5ea82d8c5593464b90f7d4`  
		Last Modified: Wed, 10 Jun 2020 12:38:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcb8713f2596697e43c935f45b92ea7e21bbaf614e7a5758bb82859da8fc361`  
		Last Modified: Wed, 10 Jun 2020 12:38:15 GMT  
		Size: 30.5 MB (30483933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f769368d71826b997fcf48fffc511465d99c1c40b9d4fe6f71db5dedc377a5`  
		Last Modified: Wed, 10 Jun 2020 12:38:03 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6abd64e1593c149cdeb68dc3419c4dacecfedb54f657cfbb6c7e8779fc6d47`  
		Last Modified: Wed, 10 Jun 2020 12:38:05 GMT  
		Size: 5.3 MB (5339850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b97c0efe975052aef794052a5322f48ddc62629fa78490f279b1dc4087b4d6`  
		Last Modified: Thu, 11 Jun 2020 22:27:56 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743a00006e5d44ea2a17cc024c68a3a5f8a19b3368611a8af8b325bfd00476a7`  
		Last Modified: Thu, 11 Jun 2020 22:28:27 GMT  
		Size: 143.7 MB (143711150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74571a7b98f62baa59b3ba17630d9f46427b4f366e4a65b05a490344be7864`  
		Last Modified: Thu, 11 Jun 2020 22:27:57 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
