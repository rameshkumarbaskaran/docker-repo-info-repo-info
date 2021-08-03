## `golang:rc-windowsservercore`

```console
$ docker pull golang@sha256:e256abcc598c779f28fab44f466a7eb23d716572dbaf465bf964906ac71e6a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2061; amd64
	-	windows version 10.0.14393.4530; amd64

### `golang:rc-windowsservercore` - windows version 10.0.17763.2061; amd64

```console
$ docker pull golang@sha256:dd9ec29ad572bb406de8391315bf102560d30706b1381793b603619ec0083fde
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2856618138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65adfda3d2345767cede3387b4e05f76a93d76861e02f228e0c363662e63306`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 02:41:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 04:25:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Jul 2021 04:25:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Jul 2021 04:25:48 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Jul 2021 04:25:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Jul 2021 04:27:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 20 Jul 2021 18:15:30 GMT
ENV GOPATH=C:\go
# Tue, 20 Jul 2021 18:16:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Aug 2021 03:15:25 GMT
ENV GOLANG_VERSION=1.17rc2
# Tue, 03 Aug 2021 03:18:28 GMT
RUN $url = 'https://dl.google.com/go/go1.17rc2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '4b4d5aa3a393c3d633286053ffad08a2b2ae558a7ee09116014f42fccb12c753'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 03 Aug 2021 03:18:32 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dd3b24b55401566ea01a5005138a23766b6b6408c2276b7ebd097da01de80897`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1c50202491861e9cc59ef0cad62ab13b4d8585699abaf13275f815b0ab53bf`  
		Last Modified: Wed, 14 Jul 2021 05:03:35 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700aac46fe704c190ed71a3f8ec8f1eca6d0fed9861862fcab96996d21678657`  
		Last Modified: Wed, 14 Jul 2021 05:03:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce5c766a8b7a15e6b68bef29d1932c4e9cf7086c6413acfcb35b89e6363813f`  
		Last Modified: Wed, 14 Jul 2021 05:03:32 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee3527d984880519c45793ad5f901d15605068f0a52a819044cd79ded461f09`  
		Last Modified: Wed, 14 Jul 2021 05:03:33 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064f16e3c9a35398857e96f60776b71b2af7e30419946307d58f942fe090b2f9`  
		Last Modified: Wed, 14 Jul 2021 05:04:02 GMT  
		Size: 25.5 MB (25460385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ddba869c49ae52e2da33b9d7755619fb390b3f5e76ad3a20f4de29a61fa63e`  
		Last Modified: Tue, 20 Jul 2021 18:31:59 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4b160532fc55fa51cd7200360f33a7fefd6f40d3d7950cca7d7b3e54ad1ab1`  
		Last Modified: Tue, 20 Jul 2021 18:32:00 GMT  
		Size: 339.8 KB (339761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb8567d87695c91bfbdd1fb3b3ebe648ef8fb9570fab37d1a93b5f233bb26f`  
		Last Modified: Tue, 03 Aug 2021 03:26:35 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad5568925b545ac7147dae2f935be5662acedf80bd162782079d5975c26da67`  
		Last Modified: Tue, 03 Aug 2021 03:27:04 GMT  
		Size: 145.4 MB (145359716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863a38e9c138ec991309fa0f8e6796b27c47f3fe156c3b284e54f543a6b0856`  
		Last Modified: Tue, 03 Aug 2021 03:26:35 GMT  
		Size: 1.6 KB (1561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-windowsservercore` - windows version 10.0.14393.4530; amd64

```console
$ docker pull golang@sha256:6f30c176e9ade962e2577367165f220d73afcb9093eb616ea0c86275492ba45c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6445220231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2f048f37dbea9c47b59bc61f9b4ce7ce01d1d3591ea1ec81e39f307c2f3e1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 02:46:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 04:31:42 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Jul 2021 04:31:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Jul 2021 04:31:47 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Jul 2021 04:31:49 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Jul 2021 04:33:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 20 Jul 2021 18:20:46 GMT
ENV GOPATH=C:\go
# Tue, 20 Jul 2021 18:22:40 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Aug 2021 03:18:52 GMT
ENV GOLANG_VERSION=1.17rc2
# Tue, 03 Aug 2021 03:22:18 GMT
RUN $url = 'https://dl.google.com/go/go1.17rc2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '4b4d5aa3a393c3d633286053ffad08a2b2ae558a7ee09116014f42fccb12c753'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 03 Aug 2021 03:22:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:624cc64d28951435759fcbbc930532718666f3285fc939c97e36c2cda79f80f2`  
		Last Modified: Wed, 14 Jul 2021 03:41:42 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f667c0fc8186714bfddbd565e9cdd1dd6497e3c112f1eddb17a37d1abae30c93`  
		Last Modified: Wed, 14 Jul 2021 05:04:30 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3566f190f34782035012abf2530315039000f1d137ad0098f1903a99127b3b8e`  
		Last Modified: Wed, 14 Jul 2021 05:04:24 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036fdd63bb05506922a2462b2487bb4ff12b9c29097537ee7d0ca4c18cad7507`  
		Last Modified: Wed, 14 Jul 2021 05:04:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8904dd19478585c0fa1c9b4a25c5ac4560759b61f3f9e2ef0e6475729d5d482`  
		Last Modified: Wed, 14 Jul 2021 05:04:24 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a50006063e099df0e3d1f22baa504b0f0de1563cd642c48340cf2a8b7152bd`  
		Last Modified: Wed, 14 Jul 2021 05:04:30 GMT  
		Size: 25.4 MB (25447622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7864578bceea568afe27b7e36ac8553d02c32cced6968a92946f3df6a830276`  
		Last Modified: Tue, 20 Jul 2021 18:32:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1531fa125afdce941775d96c1324ca122edb1be40606b27a2c0a588e111261c5`  
		Last Modified: Tue, 20 Jul 2021 18:32:49 GMT  
		Size: 331.5 KB (331522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520a1e9ad437678f91d990c9cf01fc6129a359907be4ba2113f359ed2e906c47`  
		Last Modified: Tue, 03 Aug 2021 03:27:18 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3828e3ac9043344fd3ba693ca89558baa2ecda5bde0f423abf8c8a7d362cd439`  
		Last Modified: Tue, 03 Aug 2021 03:27:51 GMT  
		Size: 149.8 MB (149797712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314ecd53d2b376171083c3f868d81a7878fd109383aa76764c35900ebface450`  
		Last Modified: Tue, 03 Aug 2021 03:27:18 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
