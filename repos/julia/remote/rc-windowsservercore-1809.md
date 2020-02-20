## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:66d0979786e7c2a8b10a5f0b1e385be54d3a04a6cd15fbbe4b7e5f0e9e268b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull julia@sha256:4a9e459a91673ed3150df77b9e155c3e784caaf33748f69fc0426b8eae5ac7e1
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359285097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cedba90e9fa29e21127933a61084f22c4507992f3c898349696bd1535c1210b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 05:51:11 GMT
ENV JULIA_VERSION=1.4.0-rc1
# Thu, 20 Feb 2020 05:51:13 GMT
ENV JULIA_SHA256=fc718bfd1fa9da9c306376c8994d3dee4b08131d3198036c33f878cf469f7567
# Thu, 20 Feb 2020 05:54:01 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 05:54:03 GMT
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
	-	`sha256:f1f0d48300526ecc6cfce7680c18cc3a9e066a48024636eff30493ce9d053721`  
		Last Modified: Thu, 20 Feb 2020 06:12:49 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b49966838edd0538b2fcd95c96f19168fd2b77a59a6b2da46d86dd1c9d6402`  
		Last Modified: Thu, 20 Feb 2020 06:12:49 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3aace25d669f4ceff612c57bea5e7711e884f4d75a6b69b5bd144763f8dc8e`  
		Last Modified: Thu, 20 Feb 2020 06:13:27 GMT  
		Size: 128.8 MB (128776384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0215f743723fb751883cbd70a7cac5ae937cde5eefe7b4cb01576e7bdae4c822`  
		Last Modified: Thu, 20 Feb 2020 06:12:50 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
