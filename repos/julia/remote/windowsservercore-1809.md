## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:e1a05891b1ceadb1e4e76e4e137561f4a8872e5c3a5f96f848e730c27ea556a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull julia@sha256:660c44049dbeddc3a9d1b81d942210fb8c431ccf58e3d25ca80f37365a1f3833
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2233857811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfd5df3e4ede56b31608ec07aaaa846008160801338629dd1edec5d6f1fa070`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 09 Jun 2023 00:36:37 GMT
ENV JULIA_VERSION=1.9.1
# Fri, 09 Jun 2023 00:36:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.1-win64.exe
# Fri, 09 Jun 2023 00:36:39 GMT
ENV JULIA_SHA256=e2f105d0ebdcd9a375bfb386bbdacc462effceba0b252f95f27b5660211c8df1
# Fri, 09 Jun 2023 00:38:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 09 Jun 2023 00:38:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6843915d8c89b6524c72964ff224097bb26322a44c1b608f18b8db2f52aacf41`  
		Last Modified: Fri, 09 Jun 2023 00:40:42 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611aab275558eccf1184659a54a5729fa89631bc936628a1d287528f2d08342c`  
		Last Modified: Fri, 09 Jun 2023 00:40:42 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e17a91d283721defc6d239f0c0f5f0f88bfa1b41eaf6d66d07c4f5ee7fcf79`  
		Last Modified: Fri, 09 Jun 2023 00:40:42 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6487525160d3e6300ddab43fdfc2f608e4d523a9a31013d78170cdaf82c555`  
		Last Modified: Fri, 09 Jun 2023 00:41:20 GMT  
		Size: 161.8 MB (161815537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ee81846c7d0e006b37bb927c3a1cdfd26d336c4dce16d17620eb02a70d1d7d`  
		Last Modified: Fri, 09 Jun 2023 00:40:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
