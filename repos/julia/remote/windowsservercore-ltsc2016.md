## `julia:windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:74b0eb833d1e674472f619245ba7239d89a22952867086af9b08009e0d922c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `julia:windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull julia@sha256:659412cf9463e43b6f83ea129e891cd43062f491700bae5bf6d84df316f71768
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5856097730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd928920a5cc2b14f1c10a39acdd77ae966f2084eb22d82b27f8770f7bf324f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 05:54:19 GMT
ENV JULIA_VERSION=1.3.1
# Thu, 20 Feb 2020 05:54:20 GMT
ENV JULIA_SHA256=8350ca66f80484c5ca6f7341ffbdb9d5182f8d4231762d585e229567b227ef7f
# Thu, 20 Feb 2020 05:58:16 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 05:58:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48c5e6f3ff403b264008be9aa0ac4a6c1ec87cf25779b258df127290a67822b`  
		Last Modified: Thu, 20 Feb 2020 06:14:15 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d2af9527e6fb3788c8c62ac765f531ea6805446829870177ec8a017a6594ce`  
		Last Modified: Thu, 20 Feb 2020 06:14:16 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe3120b6bdcafc4cc909a34e201e47b43a36992b63686965026aca4b86974ca`  
		Last Modified: Thu, 20 Feb 2020 06:14:51 GMT  
		Size: 129.0 MB (129027985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ae4d80ca53a99d12172579c946b51ae6a7ee554ba96b1da028ce45393efa66`  
		Last Modified: Thu, 20 Feb 2020 06:14:16 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
