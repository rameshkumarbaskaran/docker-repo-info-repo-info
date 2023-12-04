## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:724ac558c962af337f2eb35482091a9413ad9790b287c8508625009e8d04a4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `julia:rc-windowsservercore` - windows version 10.0.20348.2113; amd64

```console
$ docker pull julia@sha256:dfe7439c253486232f22b3700adda29c067388970e67c721b0e185e71bd0f940
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2068482965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528700542894016550fa1284d50cbb13270a0b85769445f0571db16dec511d9d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 02:33:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:33:02 GMT
ENV JULIA_VERSION=1.10.0-rc1
# Thu, 16 Nov 2023 02:33:03 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-rc1-win64.exe
# Thu, 16 Nov 2023 02:33:04 GMT
ENV JULIA_SHA256=1d9c521623cc7064c3b8f5e16d0152d7c3a858bee58138411f7e73beffc9a21e
# Thu, 16 Nov 2023 02:34:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 16 Nov 2023 02:34:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1b4bab0cda4778cf9835c8de6cf3ebaa21a5679741ef9e7b0774dbe10d6b55`  
		Last Modified: Thu, 16 Nov 2023 02:34:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17efa9c35cb12c696faa8f3a6eba0a5c6ff829eab64dea2c2adcc2d0731c3193`  
		Last Modified: Thu, 16 Nov 2023 02:34:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deda01b776ed02dc04bb9ae392d69e91ab7d46ade0d26818bd6f203d10b8d43`  
		Last Modified: Thu, 16 Nov 2023 02:34:13 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fc0d2661404868e2b3a6c54d2204df64eff21e7cfed3b391b50adaccc77661`  
		Last Modified: Thu, 16 Nov 2023 02:34:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32584eb3083f025faf3edb5287c6ce35dd4b2242f59e73ca33db24aefb3068f0`  
		Last Modified: Thu, 16 Nov 2023 02:34:37 GMT  
		Size: 181.7 MB (181695139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3764bc4dbb03708f6da79e0f8ec7e820e0eb4db4eb0c57d6e4fbe76f4523ef0`  
		Last Modified: Thu, 16 Nov 2023 02:34:13 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull julia@sha256:c579100a13ab8ec85ef14b5a2d084100913b8b714fe68ed5207ed5bdff625add
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2239097193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b469353575ba65f26fddcf60e1062f0eefa419b3cc34ef04dc6e066cf44b5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 02:31:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:31:48 GMT
ENV JULIA_VERSION=1.10.0-rc1
# Thu, 16 Nov 2023 02:31:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-rc1-win64.exe
# Thu, 16 Nov 2023 02:31:49 GMT
ENV JULIA_SHA256=1d9c521623cc7064c3b8f5e16d0152d7c3a858bee58138411f7e73beffc9a21e
# Thu, 16 Nov 2023 02:33:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 16 Nov 2023 02:33:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037f88b715502923ba2f28adf758bac88cdda3994285975d8e43b2d2efd008f8`  
		Last Modified: Thu, 16 Nov 2023 02:33:29 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f2b81c8ecc4bf3c27cb3f505fc133f9a604ad4c3051046fad2e0f998235d41`  
		Last Modified: Thu, 16 Nov 2023 02:33:27 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0ad83174e17d7d4b0892ceb4d122cd31ede8c47ab7903651e479e8c494d2d5`  
		Last Modified: Thu, 16 Nov 2023 02:33:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f42081e3d5f15a5b5562d399fbc2a7ad47e605270feac163c3321d7d28783e5`  
		Last Modified: Thu, 16 Nov 2023 02:33:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2419ce7c82f6daec93568f05cb14986877bbbf2c22f9f6d87cd271562fa0f5b`  
		Last Modified: Thu, 16 Nov 2023 02:33:51 GMT  
		Size: 181.7 MB (181659155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a315424c54abf538c1174358e0dcfc4a2568401527b9ea226886414ca1fad15c`  
		Last Modified: Thu, 16 Nov 2023 02:33:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
