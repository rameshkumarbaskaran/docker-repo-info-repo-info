## `julia:windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:10e088aad15e9619bbf141e37f769c15a2d799c98156d71ea47aef15072617c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `julia:windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
