## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:01454c54bdfd3905a2a19bf4edc81694ae2ac63610b4c2378aaa7d4947ea11f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull julia@sha256:deb179d549707ec99fce6b2305126b7a8ec73e499432a3c0705ea5f8505e8966
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1936796937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726753482e30f8ae6901a05ccbad0578c0409c3661a1b65f387aa9b601ea4518`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 09 Jun 2023 00:34:40 GMT
ENV JULIA_VERSION=1.9.1
# Fri, 09 Jun 2023 00:34:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.1-win64.exe
# Fri, 09 Jun 2023 00:34:41 GMT
ENV JULIA_SHA256=e2f105d0ebdcd9a375bfb386bbdacc462effceba0b252f95f27b5660211c8df1
# Fri, 09 Jun 2023 00:36:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 09 Jun 2023 00:36:16 GMT
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
	-	`sha256:a38f406dfeef8d638080fee6dbc302198824cbf29a026eafb6118f8f2355e1a5`  
		Last Modified: Fri, 09 Jun 2023 00:39:46 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36de2ae5d23482a7549045189e37fcb611f495477deb11c7ad084ece3ee37c8d`  
		Last Modified: Fri, 09 Jun 2023 00:39:46 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5be70deeb5601d9c337e4a8960d71deb910c479f199a1c8638933beb774f8c`  
		Last Modified: Fri, 09 Jun 2023 00:39:46 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f39bb8e9865619fd0566b025629352d4a762cf55db993f71900bd979164417c`  
		Last Modified: Fri, 09 Jun 2023 00:40:29 GMT  
		Size: 161.8 MB (161808371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306f3aca6b977181a5a31d77980c8eacf100135e72eb7899317700effa9f8c4e`  
		Last Modified: Fri, 09 Jun 2023 00:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
