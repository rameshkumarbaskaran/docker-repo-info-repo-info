## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:1d4207c11db277f3b761476842c993efac2457842c33435aad36ff7096aa1d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull golang@sha256:ca75b13869cd20e4c2684896d5c0feefe672dce1faad34d635e4250deb11570f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2883355978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8c1cc9a48df4984a6c4532d1097604d3c55aa0d8551771bd99534061aefc1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 05:11:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 13:12:57 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Jan 2022 13:12:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Jan 2022 13:13:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Jan 2022 13:13:01 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Jan 2022 13:14:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Jan 2022 13:14:34 GMT
ENV GOPATH=C:\go
# Wed, 12 Jan 2022 13:15:32 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jan 2022 13:24:27 GMT
ENV GOLANG_VERSION=1.17.6
# Wed, 12 Jan 2022 13:28:15 GMT
RUN $url = 'https://dl.google.com/go/go1.17.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5bf8f87aec7edfc08e6bc845f1c30dba6de32b863f89ae46553ff4bbcc1d4954'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jan 2022 13:28:16 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3a70d5fd54e2005efbf590b48700ed40509210354a0d8f3f18c3b444a5325896`  
		Last Modified: Wed, 12 Jan 2022 06:20:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab3a92c283c23da1114b5a193a81bc6464487c56644cd0bbb282c8006c0ffaa`  
		Last Modified: Wed, 12 Jan 2022 13:42:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1027379611971de6bc3465f90bc32c2729568caf4dfb1a06f4d6cc4ff35e99e`  
		Last Modified: Wed, 12 Jan 2022 13:42:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b47e1608cc7d7d18e98e6db8694fd18ddcc8ba3d16a703a425dae7226d8e48`  
		Last Modified: Wed, 12 Jan 2022 13:42:03 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c81b433ad7a26ae8b6d6fc12e05f2d425fd833e56075e1fb78fcadfab87bb2`  
		Last Modified: Wed, 12 Jan 2022 13:42:03 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7eeae2fccea1e527dd0fa62be4cffc50ba8b29e94ec11fa0c5215f818ab8629`  
		Last Modified: Wed, 12 Jan 2022 13:42:30 GMT  
		Size: 25.4 MB (25431808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f7bf5edc2db8a4a216d6e45e182173d1d422212d465f1ea289b8ea42bc9e9`  
		Last Modified: Wed, 12 Jan 2022 13:42:01 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfbbfd1398b65c72295f46f951a4ab9d97d5b234d1019afdd12eaa588dd478f`  
		Last Modified: Wed, 12 Jan 2022 13:42:01 GMT  
		Size: 309.2 KB (309240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912d5a4566414455b622cf1a91c2cd6e565b78a383566ab64c3e4cd217cf9ddc`  
		Last Modified: Wed, 12 Jan 2022 13:47:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81d59df23b6aba8c9f30cf14101d7ec177a7d4e7d2e5f679569c808963d2b7a`  
		Last Modified: Wed, 12 Jan 2022 13:50:24 GMT  
		Size: 145.4 MB (145372614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee9ff7c47c6224d253fed4f2a7b07c3af665e4a89a6a47587d971f4491cc185`  
		Last Modified: Wed, 12 Jan 2022 13:47:58 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
