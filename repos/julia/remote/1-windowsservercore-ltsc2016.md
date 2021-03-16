## `julia:1-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:f52c9b91f31f0657515631c66bd04685d245e17d3be255d630c6304028fde84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4283; amd64

### `julia:1-windowsservercore-ltsc2016` - windows version 10.0.14393.4283; amd64

```console
$ docker pull julia@sha256:9d5e628c8a9f31b4161cbbb0d784a18650ff3e7b4d0aeeacfd90939ac99762be
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5935089898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a183044a570388c8512ecc6261d81d67923c90b4395de196536d95d7dadef79`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Mar 2021 18:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Mar 2021 13:42:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 15 Mar 2021 19:22:59 GMT
ENV JULIA_VERSION=1.5.4
# Mon, 15 Mar 2021 19:23:00 GMT
ENV JULIA_SHA256=5942d2cd2535daf6f49979e9dda4968a8ca35fdbfaa7923e8c8929ed785aa0a3
# Mon, 15 Mar 2021 19:25:31 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Mon, 15 Mar 2021 19:25:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30bda99601c5cbd3b2118409f401852ea648e2319bd81518723e476b28d764c5`  
		Size: 1.7 GB (1726924885 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76680da9dc6db108ddf2e353c494b45e8486a6751619a13ed8fb3ad64b9a16e9`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57b36f10653ee03dbee47af57e232ca36a73557e870896955158281a812aa66`  
		Last Modified: Mon, 15 Mar 2021 19:31:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f87449e53f98d6319b2b4382a8c4d0c77d7d5de9822447e3660bb3d729dd3b`  
		Last Modified: Mon, 15 Mar 2021 19:31:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6e03c673f732345abe6c3147b711d7f00e0289cbbd0d06f16c90ca8a7526a`  
		Last Modified: Mon, 15 Mar 2021 19:33:59 GMT  
		Size: 138.2 MB (138173541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4296d1e717f8d1be536f5a1768d27f3a9966921b239d906ce9c7b410b89b3ce3`  
		Last Modified: Mon, 15 Mar 2021 19:31:15 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
