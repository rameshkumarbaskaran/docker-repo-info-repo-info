## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:30526016f4cdb9c4c5c531ce9e9955b2328b495c64587b2767af1ad1561439b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull julia@sha256:25ab1a544fb2ce3fd59e5fbaf47ad242e28c63c4bbf2d0b0e4dc47cd55b3d225
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2233512867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76648ae4ac059222749064fa8c307f696e203873d350d53c97f553cc997c583a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 17:18:35 GMT
ENV JULIA_VERSION=1.9.0
# Wed, 10 May 2023 17:18:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-win64.exe
# Wed, 10 May 2023 17:18:37 GMT
ENV JULIA_SHA256=096ed36b1bc1fd7d00abc47d9e9f339d051961c2d0c5021005bb8f7e7a93ef0e
# Wed, 10 May 2023 17:20:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 May 2023 17:20:29 GMT
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
	-	`sha256:d785f01b4ee99c7ba82c3b5b935ca2f788a3def4e57145b304e7d1d3c9728ded`  
		Last Modified: Wed, 10 May 2023 17:22:07 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d291d304af7e0c57143faa61f0eda518c4bfb4ff210d19e47a0abb77e0914f`  
		Last Modified: Wed, 10 May 2023 17:22:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356cccccf4b0bbca7afcd352d1b472c323ca99fe17eeab8dea3eb1146b926687`  
		Last Modified: Wed, 10 May 2023 17:22:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a64a1eda873b1cea949cfe88cda836dcb34d676ca7d6f01bfc0862e9e518880`  
		Last Modified: Wed, 10 May 2023 17:22:38 GMT  
		Size: 161.5 MB (161470633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae670d86aeef0dedbb6d00c9207edde78d7c2fea34b1b2245633ed9f724c9ad`  
		Last Modified: Wed, 10 May 2023 17:22:07 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
