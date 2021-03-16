## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:355c0babceb68f87f8a1f0d50d66aee62671b3937c8a44034bdeceec2355e6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull julia@sha256:9d37ca4c77142d3d9a877fbc041ca3391144fed519035b91e761812671d7c829
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2598973480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b069aae2d8a78f75c6a0a13b03d7a889492eddb665a537b844b79e63c09fbfa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 15 Mar 2021 19:21:01 GMT
ENV JULIA_VERSION=1.5.4
# Mon, 15 Mar 2021 19:21:02 GMT
ENV JULIA_SHA256=5942d2cd2535daf6f49979e9dda4968a8ca35fdbfaa7923e8c8929ed785aa0a3
# Mon, 15 Mar 2021 19:22:45 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Mon, 15 Mar 2021 19:22:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b55952611ae14f35a152f6e312008f029fb45625298ef6b9b0aa0b9de82756`  
		Last Modified: Mon, 15 Mar 2021 19:28:20 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a5cb3df8f09ed7f64be985210752dd2892539ed2f5f1c1ac858c09de887bb1`  
		Last Modified: Mon, 15 Mar 2021 19:28:19 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17582e2439f2a4a42dcd9ad7cbbcb79eb127dff90a77e11d580f8d86cc81673b`  
		Last Modified: Mon, 15 Mar 2021 19:30:58 GMT  
		Size: 137.4 MB (137433298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01231a2defd09c0e171eb2f80a14236560868b9d716bd04a119bf786519f04b`  
		Last Modified: Mon, 15 Mar 2021 19:28:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
