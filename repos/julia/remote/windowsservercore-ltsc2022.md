## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:d456bc1037ec50a9558c1143a8dfb6712820851fae28aa4773ce45ddeb8d40e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull julia@sha256:f6241fcf25f0f14ee094adf4a0872efe74ef72d34fa74d55849640d6903ab3ee
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2477394509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005dec4146ebaaffc984e7f1a3d00f1ab3e1126d87a14ddbe8c53d33a5e9df3d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 12:11:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Aug 2022 00:16:00 GMT
ENV JULIA_VERSION=1.8.0
# Fri, 19 Aug 2022 00:16:01 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.0-win64.exe
# Fri, 19 Aug 2022 00:16:03 GMT
ENV JULIA_SHA256=a1699278e4884578c10580cf19f8d42401abce78f459c416998221902ea26d38
# Fri, 19 Aug 2022 00:17:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 19 Aug 2022 00:17:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a5e3787c778295a5877e0381020b02273a985f7db2dd483ddff586869546e4c`  
		Last Modified: Wed, 10 Aug 2022 12:42:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f2d471be84413e3e4e6902f7bd63ab118d4c43d14367861367ede14cbff58`  
		Last Modified: Fri, 19 Aug 2022 00:21:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f1c99f603d86e2c9fe398b1e62de63ea5c4b37fa1bc0a74c9dd03af68cf773`  
		Last Modified: Fri, 19 Aug 2022 00:21:04 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2daa8117b050cc6db64f65f4d4afa44e0c1487d694fae17d8eabcf2afcf44610`  
		Last Modified: Fri, 19 Aug 2022 00:21:04 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60d4abe59ff41e01dbdc4fee230b6ca75ff4b3481d4d294c7c8a722d0e45092`  
		Last Modified: Fri, 19 Aug 2022 00:21:39 GMT  
		Size: 160.5 MB (160498317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1fb16fac4eec8b752d2a6a6ff9c4b8394d9404339102879b3165ebd22f9667`  
		Last Modified: Fri, 19 Aug 2022 00:21:04 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
