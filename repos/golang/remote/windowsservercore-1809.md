## `golang:windowsservercore-1809`

```console
$ docker pull golang@sha256:be8a26218ddb814c95401f2eac09ebfd4c7685404bad37b2ebbde31a7d67c152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `golang:windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull golang@sha256:425c30c295a4d68900c89b2e912f921c50f12df30630f615e77faf5ebba61877
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2964135724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51145f4550103955be84b50e7c2678efea52386ae270c430af482511ca2941f9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Tue, 13 Dec 2022 22:48:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Dec 2022 00:18:40 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Dec 2022 00:18:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Dec 2022 00:18:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Dec 2022 00:18:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Dec 2022 00:20:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 00:20:53 GMT
ENV GOPATH=C:\go
# Wed, 14 Dec 2022 00:22:23 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Dec 2022 00:39:30 GMT
ENV GOLANG_VERSION=1.19.4
# Wed, 14 Dec 2022 00:44:49 GMT
RUN $url = 'https://dl.google.com/go/go1.19.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ada490e188bfb57c7388da7c5eba7565390992b6496204d30e710d37755956b0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 00:44:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc9debb9503ac53c2f64685982eca56ac5110ea6baf7278b27af54ab8fbc409`  
		Last Modified: Tue, 13 Dec 2022 23:54:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e19a727cee4cff521509e4f3066980b49514cae5f0e8343cb5e1726647ed0bd`  
		Last Modified: Wed, 14 Dec 2022 01:12:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0965d1c4ecd2141edbdca68ccc00c3aec3ef8f7ed032cd1046f18f19ccb0fda7`  
		Last Modified: Wed, 14 Dec 2022 01:12:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa52be7c0b9474e21af5d159c9fd30df24c3582a8b38eb7533dfed805527edbe`  
		Last Modified: Wed, 14 Dec 2022 01:12:42 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840377a87f6fcb66c0740c425e434c26df421953b9d7d92957b2e70a4c0708e1`  
		Last Modified: Wed, 14 Dec 2022 01:12:42 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dede380cb9ca0829da61be2571bbbc5111c4bf1c6899b2a016c46083ff588613`  
		Last Modified: Wed, 14 Dec 2022 01:12:49 GMT  
		Size: 25.4 MB (25440328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec496d87261cb41e24b6026752d127d0a6d25092f5a19b7b92c8c75b5a35f15`  
		Last Modified: Wed, 14 Dec 2022 01:12:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8ccbcba5f81db88da4bd54e487fdb66dda804fe6b98f539499c48b13f3d9c7`  
		Last Modified: Wed, 14 Dec 2022 01:12:40 GMT  
		Size: 315.2 KB (315247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efc5399861a7f89a85cc92de7398d4286c323ee685a61804326759484824caa`  
		Last Modified: Wed, 14 Dec 2022 01:16:00 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ca13821699d672692516020d4ba11d5f66f8f13b8aeb8f4a470d1f38613e43`  
		Last Modified: Wed, 14 Dec 2022 01:16:52 GMT  
		Size: 157.7 MB (157671914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501deedc3ba99b8597a0000230deb96f57a9064e6a61b3a347aba6b451a76014`  
		Last Modified: Wed, 14 Dec 2022 01:16:00 GMT  
		Size: 1.5 KB (1496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
