## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:9eaefb3a7dcf2da73277d66cf06371b78ef2363bad2f83b2bd897fc2e7e2d19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull julia@sha256:a17731a4076cc7c39a4972cf859551b6575f21f8a99a099e938d58f0d48aaafc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2640377690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eba6d17075365088771e6b6bebf2099773bc572f6a3996d986423acf133d8fc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Tue, 08 Nov 2022 18:28:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 16:35:19 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 09 Nov 2022 16:35:21 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 09 Nov 2022 16:35:22 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 09 Nov 2022 16:37:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Nov 2022 16:37:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becc14271944025e3fa6c2ef2689bdfbf09bfc54ec339115d3082df315898e4`  
		Last Modified: Tue, 08 Nov 2022 19:38:57 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df7c8cc17ef1aa27bb39211e58ac878b1af812663febe57924c9fd27895c779`  
		Last Modified: Wed, 16 Nov 2022 13:25:23 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02febd2681a62af23a56f76194dd5364f99b900de6d69719a250317a9355416b`  
		Last Modified: Wed, 16 Nov 2022 13:25:24 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a102833da827b12c6306df6a900be9885d2bf50febe8259ec663fa29a6f2114`  
		Last Modified: Wed, 16 Nov 2022 13:25:24 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208aa90f096c8b059113d35a12788f8efa0fa83796881abcf1c40392d743c376`  
		Last Modified: Wed, 16 Nov 2022 13:26:09 GMT  
		Size: 158.6 MB (158602141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d1ef404f7e0bba7d06a2d5cc52e17756feb210c910a3e6df96243d1c7d3074`  
		Last Modified: Wed, 16 Nov 2022 13:25:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
