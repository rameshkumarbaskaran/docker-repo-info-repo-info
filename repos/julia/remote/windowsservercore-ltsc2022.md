## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:5f1b52f9698c5d4b76580f3933a7f37a4489d963573120b6466948b4d1fdb7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.768; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.768; amd64

```console
$ docker pull julia@sha256:1b909fc42089298708300b0a29e88a0242e1ef7b07da4d2f29d2667be6e93b01
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2423693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01291f212c7d0a959d0a49dc8f632fbe468b65fced7ea8dd0f9ee8e71b61efed`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 09 Jun 2022 04:32:50 GMT
RUN Install update 10.0.20348.768
# Wed, 15 Jun 2022 12:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 16:28:48 GMT
ENV JULIA_VERSION=1.7.3
# Wed, 15 Jun 2022 16:28:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.3-win64.exe
# Wed, 15 Jun 2022 16:28:50 GMT
ENV JULIA_SHA256=ef5915eaf35bb71359072e8c41f84fa73f1059fecb198e7fc838270d4ba5bbae
# Wed, 15 Jun 2022 16:30:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 15 Jun 2022 16:30:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c71967ff41928927e4c407171e4ffbac3c9ab4221eb64f5ca5a34ff4c230567`  
		Size: 841.6 MB (841600427 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dec0338feaf01f35eb916b7fd9ecc08b719354163254885d5215e513c1a3eb2e`  
		Last Modified: Wed, 15 Jun 2022 12:49:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b355a272488ee06891e5ce42aec28bb48454b0c805a70b58f273c7277ad848`  
		Last Modified: Wed, 15 Jun 2022 16:44:48 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deffc7591938abbf567186ba1124f4460e20f08db3e2521ffd30d54700edf116`  
		Last Modified: Wed, 15 Jun 2022 16:44:48 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b5d70c3220c695baea8d14b28066ee2a577c23faa77d5b0f8ca874bd981a22`  
		Last Modified: Wed, 15 Jun 2022 16:44:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf4800432735b884ea0787c6f45c4773efc185d1b275fca670ef7e5ac11ce59`  
		Last Modified: Wed, 15 Jun 2022 16:47:48 GMT  
		Size: 145.2 MB (145222695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed62a385dabc084f93e02157d67e3a629fb3e87cf3f9ce9709892cd9d647a93`  
		Last Modified: Wed, 15 Jun 2022 16:44:48 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
