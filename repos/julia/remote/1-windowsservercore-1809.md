## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:8f2a927aee1c07b4964b53f4c29eafc17f93865933f89502a58da0b2988335bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull julia@sha256:b3871b6da204d39816bdded68a989c1c64519649774a316a481eece65924f91b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2856911869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ef659499a92fcf4e479ab1c3166823ee0ca48fd8a3dad20b8dd4ff39c1339`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 05:11:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 15:02:05 GMT
ENV JULIA_VERSION=1.7.1
# Wed, 12 Jan 2022 15:02:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.1-win64.exe
# Wed, 12 Jan 2022 15:02:07 GMT
ENV JULIA_SHA256=820f31de28d409ae8fda2ea01d39c67564fc6138d010e8b7e5d3d883d7daee23
# Wed, 12 Jan 2022 15:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 15:04:29 GMT
CMD ["julia"]
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
	-	`sha256:0494dbd67e135ee5263a5530affe62be92c8546fc9a98231d01ee97280f2794f`  
		Last Modified: Wed, 12 Jan 2022 15:08:06 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ac89e913c91d5169806d0ea56edc329df909b8223d1440887215b96bc0ec77`  
		Last Modified: Wed, 12 Jan 2022 15:08:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3673a3e7c3b7f76f5095a5dab525d6c7d1c7a8f8a544eae51c970ed7243499b`  
		Last Modified: Wed, 12 Jan 2022 15:08:06 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a65ebad860515f484386331a15dda435a2cd9d3248bc5099213f5d5fbd98eb`  
		Last Modified: Wed, 12 Jan 2022 15:08:38 GMT  
		Size: 144.7 MB (144673843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a8f7634f45673316f9cdd71cae02cca4f3bc4d8900d203780ecefa1fb2e388`  
		Last Modified: Wed, 12 Jan 2022 15:08:06 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
