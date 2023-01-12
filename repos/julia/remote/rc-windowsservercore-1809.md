## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:ad956187c7bfdd75f2ec98ac5ba9813cc887296d4b6813bded26236d0f959556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull julia@sha256:47911d13475fc0db55fe1d7c60d2d628d56a8c2a240a1b52b8ae423a609d1b77
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1868249266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f3f84644abe5bd93322cf26c288d8ba682048f99d8b3bfb95053a1063bfcd0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 07:15:08 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Thu, 12 Jan 2023 07:15:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-beta2-win64.exe
# Thu, 12 Jan 2023 07:15:11 GMT
ENV JULIA_SHA256=b651d54e41243fba9b979d4d8c5d6f770030c0a8089062d2fe74638c3e736cec
# Thu, 12 Jan 2023 07:16:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 12 Jan 2023 07:16:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3957efb289f7c193e18ab4ed3d195f9277d9dc5325b4890f0d3fb2ba90de749`  
		Last Modified: Thu, 12 Jan 2023 07:26:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a2ab9e48d3ae1a36885e7d1767ce3b0f7e53ec07a35fdb9009e104263dea89`  
		Last Modified: Thu, 12 Jan 2023 07:26:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68f44bc6ea14080bb7c9d96ffdd82dd68378b610d7f7cf36abf49eaa682b424`  
		Last Modified: Thu, 12 Jan 2023 07:26:31 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ab305a53aa36787e83fba8a33ac96bb0ae1a5d9a4de85cafdbc11cdfdda929`  
		Last Modified: Thu, 12 Jan 2023 07:27:12 GMT  
		Size: 160.3 MB (160298587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e1278496cf78a05fadfca7476c15102fff9865ec8bedb38cb54490043ad6bf`  
		Last Modified: Thu, 12 Jan 2023 07:26:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
