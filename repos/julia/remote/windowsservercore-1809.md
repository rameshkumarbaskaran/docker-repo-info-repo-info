## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:db16ce264322f8c524a5c9310b4b4eb1b8ee10184b020d1b06f96098fe0f8afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull julia@sha256:375bc7b74687228fc19c283ad77aaa413ba083c877d656fbc2c1137c1d3a6ef4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2354245638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1702a1bf98c9138b7acf63d73c54a7e4b2d9dda7c68abed5a4ddf515ae69a5b9`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 05:58:47 GMT
ENV JULIA_VERSION=1.3.1
# Thu, 20 Feb 2020 05:58:48 GMT
ENV JULIA_SHA256=8350ca66f80484c5ca6f7341ffbdb9d5182f8d4231762d585e229567b227ef7f
# Thu, 20 Feb 2020 06:01:50 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 06:01:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec7821797f7d610f0520ec28206260f950edbce9966bbd70a893cb2d6945224`  
		Last Modified: Thu, 20 Feb 2020 06:15:32 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a6b3e47dbaf18d1d64dda1add2a7f05f61015e388a005cfdc2de28c4342718`  
		Last Modified: Thu, 20 Feb 2020 06:15:32 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5867f33cc325e4dc08c2ebc8466df4811f5d8c8dabd6f778044ca62665a3315`  
		Last Modified: Thu, 20 Feb 2020 06:16:05 GMT  
		Size: 123.7 MB (123736935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20569d9b4589746440cc9eccc6eba25b7891ba9af05bfe789bad4a1c06aa25b4`  
		Last Modified: Thu, 20 Feb 2020 06:15:32 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
