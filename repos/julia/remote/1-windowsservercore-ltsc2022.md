## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:abacfdbf4b3d782ecaee66d40609bc3403e186d4083b2d9c07976c6380f66cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull julia@sha256:081e5d567c48c0e7191d9c1be9b93086d093717726d14c4217ad7152e24bfb02
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1917842526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b4c097ba45028f86d73f60b2706cd018853d5257c421a0cad11b87a1735de8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 05:28:53 GMT
ENV JULIA_VERSION=1.8.5
# Wed, 10 May 2023 05:28:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.5-win64.exe
# Wed, 10 May 2023 05:28:54 GMT
ENV JULIA_SHA256=866e160d46c85167d10e8a925776c2fb1cea0f668eb8c80a605842fd35ef28b5
# Wed, 10 May 2023 05:30:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 May 2023 05:30:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ccb120173a470e3dd7cc0499248b05f20593861b1fae89498ede9efdac3fe`  
		Last Modified: Wed, 10 May 2023 05:37:37 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374a50c0b874859be97a224c81d55c0983937135f94b8b8fea3e17dc779da9b8`  
		Last Modified: Wed, 10 May 2023 05:37:37 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9817d200a0b3617fbccf292d7f3b2f18c4719fdc33462b03eabd119056a1ae`  
		Last Modified: Wed, 10 May 2023 05:37:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0ff15326986067b6acdc0932062fded5c9a3244a233ac4a1cf6fa92663edae`  
		Last Modified: Wed, 10 May 2023 05:38:05 GMT  
		Size: 142.9 MB (142853975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2144ae69e7edf5811be1404f19661c9cc3d4e546c93a97d209477745d3858d3e`  
		Last Modified: Wed, 10 May 2023 05:37:37 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
