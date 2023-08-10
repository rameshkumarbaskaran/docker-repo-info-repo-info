## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:c56024980d2162a00b9f8a78be84807473e20ef32aa768acc5d64d4e9d340dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.1906; amd64

```console
$ docker pull julia@sha256:991a704ed0a227d587cc1f0cb37056cc5cfa05e90f8416addf27d55ad98c9b7e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958936694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d74827fa21f3cba34a75a18aff0741b16c919fb2e3efc8f50c291f3412531`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 03:13:44 GMT
ENV JULIA_VERSION=1.9.2
# Thu, 10 Aug 2023 03:13:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.2-win64.exe
# Thu, 10 Aug 2023 03:13:46 GMT
ENV JULIA_SHA256=bcc8a0eb217ee128638e12b756e1f41df5c83cff6c6749839d081618f6c79e57
# Thu, 10 Aug 2023 03:15:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 10 Aug 2023 03:15:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030a399460ce9d32ff5a7f2b088e2204e188cee9db7ba13a89994b3a942fa035`  
		Last Modified: Thu, 10 Aug 2023 03:23:27 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b6364ac679f298d1bfad73af9a7c2501259b2561585aac5082f5f04d27b5`  
		Last Modified: Thu, 10 Aug 2023 03:23:27 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eace3d6dd2d3ea31140f2b2950dd8c0c906586028da9e8f656515a8b12dc3cb2`  
		Last Modified: Thu, 10 Aug 2023 03:23:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a29f8ea2b7a7e4f162f63d3e2f9f59bb3c29bfd836b014e59e60e5d7e2db857`  
		Last Modified: Thu, 10 Aug 2023 03:24:03 GMT  
		Size: 161.6 MB (161565837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2145606345be82f5a982ff1468e465e50e1f9ada23ceab02270d62c9d0f8df6c`  
		Last Modified: Thu, 10 Aug 2023 03:23:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.4737; amd64

```console
$ docker pull julia@sha256:a799eeba7494644e9bbb086497cc0decbad9713b20c2f9c040b38632a3c32a56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2157540596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e21d9faa2808501ea6c1c1c3b166060d2c051db905a7008257b3aa73da90db`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 03:15:27 GMT
ENV JULIA_VERSION=1.9.2
# Thu, 10 Aug 2023 03:15:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.2-win64.exe
# Thu, 10 Aug 2023 03:15:29 GMT
ENV JULIA_SHA256=bcc8a0eb217ee128638e12b756e1f41df5c83cff6c6749839d081618f6c79e57
# Thu, 10 Aug 2023 03:17:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 10 Aug 2023 03:17:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e329d6376ed7e6deb63bba9d766a955f819f4c34a438951fecd752b22a0e31a`  
		Last Modified: Thu, 10 Aug 2023 03:24:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068ff0279d53d23a17d9ea9da2339672142d1694beacdebf25c869369e07ba3f`  
		Last Modified: Thu, 10 Aug 2023 03:24:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef209e7cb95b086bfa690083a6671f0f3dac9c651f764e23da5eaf83522e3189`  
		Last Modified: Thu, 10 Aug 2023 03:24:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522467a665ef72cf5035d3ba3bc0a1cdd76855ee61807eb078d95e31d55567af`  
		Last Modified: Thu, 10 Aug 2023 03:24:52 GMT  
		Size: 161.6 MB (161578606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01ca09eb33802774b15ca6714684d0b3d74a362a45d276ba1cfe2b0bbfd75d9`  
		Last Modified: Thu, 10 Aug 2023 03:24:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
