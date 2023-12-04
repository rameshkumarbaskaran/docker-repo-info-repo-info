## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:5b0e1a66af62c08fa703833dcd366eb204a36062f5347af514659a3e7eaa3c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull julia@sha256:36801d9b12b51f6d553893ac5c0bab1e6c72eb9e7bc9d74c13cc0dabaf16ba7d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2219065951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e069c41fc17884209d906f0126b35afabeb4477294717e9e878b892e2d3791e3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 02:34:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:34:57 GMT
ENV JULIA_VERSION=1.9.4
# Thu, 16 Nov 2023 02:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.4-win64.exe
# Thu, 16 Nov 2023 02:34:59 GMT
ENV JULIA_SHA256=8a491b31a8430c3662dff34bf349653e2d13ef98a4dcf7caa740359b6c5fef3e
# Thu, 16 Nov 2023 02:36:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 16 Nov 2023 02:36:43 GMT
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
	-	`sha256:cd90ed1489332d6672aa8ec23f05c3e8a299bdc59cd2b65c0e2295a538608781`  
		Last Modified: Thu, 16 Nov 2023 02:36:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1da954ff6e1aa230719a02fd39cccda51aafae0cb12b80bd37c025ac8146391`  
		Last Modified: Thu, 16 Nov 2023 02:36:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccead3b4770cf8d90ecaedad1cc3c4e263776359b2dd0f75ac09cedc8a43658d`  
		Last Modified: Thu, 16 Nov 2023 02:36:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597136e0a3575b4851ea0bf48c58dbb3c00fbde3a7c958af3ca2841f7f4539a1`  
		Last Modified: Thu, 16 Nov 2023 02:36:47 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ace3b9d376f966932b94b76f860ad5fd402316cf61f3bdcb1f9ac0ac725ee2`  
		Last Modified: Thu, 16 Nov 2023 02:37:08 GMT  
		Size: 161.6 MB (161627871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba015fdc31b030ad8a75463ad393ee392c41efdcba198948bd514a8904ab804`  
		Last Modified: Thu, 16 Nov 2023 02:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
