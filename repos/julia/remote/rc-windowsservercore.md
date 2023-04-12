## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:fef37876b95f5d0366124d46817f7f07a8993b42b6b92ee64b9875da56f20ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `julia:rc-windowsservercore` - windows version 10.0.20348.1668; amd64

```console
$ docker pull julia@sha256:ce25411d30958360a94d0c1b1d9f2cd9a36d362c964b0141ef25d9fbe9d0a500
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1924386731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6562d7df4c8a17336b07171971d4af89183cee8039baa1247a4921943a7c53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Wed, 05 Apr 2023 00:38:27 GMT
RUN Install update 10.0.20348.1668
# Tue, 11 Apr 2023 23:37:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 06:02:09 GMT
ENV JULIA_VERSION=1.9.0-rc2
# Wed, 12 Apr 2023 06:02:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-rc2-win64.exe
# Wed, 12 Apr 2023 06:02:11 GMT
ENV JULIA_SHA256=ea884f779347b1e307b62b1458ed0430de23259b69016004ef5271736d77309c
# Wed, 12 Apr 2023 06:03:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Apr 2023 06:03:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ecfa9c953d28a9da9d422b57cd0361c57c44e1faaaed7e50a2537d1c29cee1`  
		Last Modified: Wed, 12 Apr 2023 00:50:33 GMT  
		Size: 376.6 MB (376573004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98474c9b39bb0e3a2d79dca81a90952011b65d1fa352021dacd30335d1bb69f4`  
		Last Modified: Wed, 12 Apr 2023 00:49:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a1be118a0c3dc4e9c05ffe4c71803171bfdbc4be4026dcbd352a0121570171`  
		Last Modified: Wed, 12 Apr 2023 06:15:38 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4062883a6538e9c8556820fb978699473a07d741fec7040466055612b6807f1`  
		Last Modified: Wed, 12 Apr 2023 06:15:38 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd16ca5de1fa248209b46e18e35fa5e742f3a255803d714506dbcdfd3d412a48`  
		Last Modified: Wed, 12 Apr 2023 06:15:38 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d932c6dcde691f1177a7227b468d525f51a68f2574008121bfaa1a55ab78482f`  
		Last Modified: Wed, 12 Apr 2023 06:16:17 GMT  
		Size: 161.8 MB (161777538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0397ec875cee5b16aee9f29ab9de2ac4280f868e7d7bd5d0f4607e0b30991b6b`  
		Last Modified: Wed, 12 Apr 2023 06:15:38 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.4252; amd64

```console
$ docker pull julia@sha256:2936d9f463670072c5d1412f58e12b64dff676df2c92fd2ee8b3ea5871ce29f6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2232809785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e70f8b6e45483ad904f4aaa7fedd96e1810da1813c53f7a2bb11dd120f921e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Tue, 11 Apr 2023 23:40:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 06:03:53 GMT
ENV JULIA_VERSION=1.9.0-rc2
# Wed, 12 Apr 2023 06:03:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-rc2-win64.exe
# Wed, 12 Apr 2023 06:03:55 GMT
ENV JULIA_SHA256=ea884f779347b1e307b62b1458ed0430de23259b69016004ef5271736d77309c
# Wed, 12 Apr 2023 06:06:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Apr 2023 06:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9103f1e2cdefe8f16dae9619b88e38aa659abb17276d2362d435ad0721d3bf41`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b303297aebce0a6e960ee45b3369509c6d8c8ddea26f2332553dd4758ba09`  
		Last Modified: Wed, 12 Apr 2023 06:16:28 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d59a54aac2667f73634725881b0d9732851a197de268574fbb75f1d2d781f9`  
		Last Modified: Wed, 12 Apr 2023 06:16:28 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852cb60230b348d48dc8b86a18d12530ca2900d64c93529e2848f69053d5ab73`  
		Last Modified: Wed, 12 Apr 2023 06:16:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a55b87c6d403d37aa9c085931a3c7fefcb921bb53f8c139bb75c828ab76a52`  
		Last Modified: Wed, 12 Apr 2023 06:17:06 GMT  
		Size: 161.5 MB (161511490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0f01d0b554e99cc80bf6d6bc0001393c3f6977cfd7b984ec11c25ddce4ce9`  
		Last Modified: Wed, 12 Apr 2023 06:16:28 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
