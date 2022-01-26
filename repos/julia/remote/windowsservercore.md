## `julia:windowsservercore`

```console
$ docker pull julia@sha256:be3ecdecb3f1196b60c3ed339b65ccd2206bae643335b74c2eeaa84a2b268507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `julia:windowsservercore` - windows version 10.0.20348.473; amd64

```console
$ docker pull julia@sha256:2f78f2d2ce489a467aea6dcc8acc3262ed6f6101d0ea48c5d5f44750d66e94fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2352439480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849185f69b0def18c06d2c3fd1d8d98c8492c2d3d51694712b247317f8eab5b6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 26 Jan 2022 18:37:04 GMT
ENV JULIA_VERSION=1.7.1
# Wed, 26 Jan 2022 18:37:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.1-win64.exe
# Wed, 26 Jan 2022 18:37:06 GMT
ENV JULIA_SHA256=820f31de28d409ae8fda2ea01d39c67564fc6138d010e8b7e5d3d883d7daee23
# Wed, 26 Jan 2022 18:38:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 26 Jan 2022 18:38:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a49671e7c6abfbe5c055731704ce75743f1820732bce7aea59ebec0c5a33f87`  
		Last Modified: Wed, 26 Jan 2022 18:47:38 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3810b31d68a743688eaa3620379297cf8bbdb388335e9253242d4c65132ac74`  
		Last Modified: Wed, 26 Jan 2022 18:47:38 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08be012fc7438de8cf7437ee336cf47a6da417638eb0ed9b376cc4c1bb624cf0`  
		Last Modified: Wed, 26 Jan 2022 18:47:39 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08c17e3138738b76b24896b980b465fac3de690af3ff87fbf23a1f443b87559`  
		Last Modified: Wed, 26 Jan 2022 18:50:29 GMT  
		Size: 144.9 MB (144932583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e146030e66450fd18f6544ea361a8dbed7a7cf1b408e22f4d06e4351c96ad8e`  
		Last Modified: Wed, 26 Jan 2022 18:47:38 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull julia@sha256:bb59b2e01f564d6d0eceb4b52005aee43cd648fee9e4572b5875d57f3cc9b83a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2858039928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1e5e91135e595187dab8f6c469947869a4ce192d72d4cf8db5a9f37991a5d1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 26 Jan 2022 18:39:02 GMT
ENV JULIA_VERSION=1.7.1
# Wed, 26 Jan 2022 18:39:03 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.1-win64.exe
# Wed, 26 Jan 2022 18:39:04 GMT
ENV JULIA_SHA256=820f31de28d409ae8fda2ea01d39c67564fc6138d010e8b7e5d3d883d7daee23
# Wed, 26 Jan 2022 18:41:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 26 Jan 2022 18:41:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684c74cd5269b168adff68020d47b966694f7ec68a910897e97ac0dedf66170`  
		Last Modified: Wed, 26 Jan 2022 18:50:45 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6581f2b954c9b2a671f0fdce10aa08686399a79389ce914d5b32f5ffff70fba4`  
		Last Modified: Wed, 26 Jan 2022 18:50:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4028ae6c2011cc86868c40d164ed5e6e83fb3c0b47ba5cdf29d28ef3b80706`  
		Last Modified: Wed, 26 Jan 2022 18:50:45 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6050b1206dff57d0d78d28c3c68efae9ca715409bc64d66cfa5e47ed1d55b31`  
		Last Modified: Wed, 26 Jan 2022 18:51:25 GMT  
		Size: 144.7 MB (144711328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a864b696180f70f6f08f25d4e1c08afdc1ba5c7d93ce0ddf18a42c0897e7f8`  
		Last Modified: Wed, 26 Jan 2022 18:50:45 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
