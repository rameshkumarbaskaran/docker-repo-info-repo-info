## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:e885f4a02a4cccc6bc3a426441ea9f923d0c43ce54d3db4cbcc896505da30c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull julia@sha256:1d7c3127a0a68d943296e3b54fd29be2933e6e9eb564c6b4d939e5d6d5eef7ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214200262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8666714c619eddaf3e7c87a01d4727ad49ba715f6941b0b90795e083addba3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Tue, 11 Apr 2023 23:40:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 06:08:22 GMT
ENV JULIA_VERSION=1.8.5
# Wed, 12 Apr 2023 06:08:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.5-win64.exe
# Wed, 12 Apr 2023 06:08:23 GMT
ENV JULIA_SHA256=866e160d46c85167d10e8a925776c2fb1cea0f668eb8c80a605842fd35ef28b5
# Wed, 12 Apr 2023 06:10:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Apr 2023 06:10:42 GMT
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
	-	`sha256:0b19c66c39719cb638439a294fbca206b5f12a5a2efee2a8a38074e39c0c7fb5`  
		Last Modified: Wed, 12 Apr 2023 06:18:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f139b8e77eda87e178a285dbd0134eb3d8074a72e99a0b6808ef13ca40b1195f`  
		Last Modified: Wed, 12 Apr 2023 06:18:02 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340b3feecbf2028af8ac66d83a10f934ff5ea0158c11303b93c089c3ccba47ec`  
		Last Modified: Wed, 12 Apr 2023 06:18:02 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f641384c9c547b6a55a6b169f4c3890153c293518780912b4e873c04e013b10b`  
		Last Modified: Wed, 12 Apr 2023 06:18:35 GMT  
		Size: 142.9 MB (142901953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b65cf86844452ed64f0a478eb6e8b860ff646542d973f8198d3c7b727a76ea4`  
		Last Modified: Wed, 12 Apr 2023 06:18:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
