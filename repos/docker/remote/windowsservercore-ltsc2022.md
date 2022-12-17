## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:2ff9e07b822eb1e39313bd81a0b017c322fcea13a6cb52461882131f5292c0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull docker@sha256:a1a4511dc68bc32f907d2fcf0e33d9b5e03730b7bcbc3ca00b382b259ee02038
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2550888582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03229ced9071a21da3bff832ea3b4e06c709e402c5b874cca9598fcccbf08668`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 09 Dec 2022 09:36:47 GMT
RUN Install update 10.0.20348.1366
# Tue, 13 Dec 2022 22:45:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Dec 2022 03:16:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Dec 2022 23:15:40 GMT
ENV DOCKER_VERSION=20.10.22
# Fri, 16 Dec 2022 23:15:41 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.22.zip
# Fri, 16 Dec 2022 23:16:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa20ce142ecceb471dc070d9582fff942cef447b7c8ff22f2223ffe3737c99`  
		Last Modified: Tue, 13 Dec 2022 23:54:14 GMT  
		Size: 1.0 GB (1021665190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb8b9a4ec3ca516cfaa44f64e80b1e3aaecdbde870177411ff046f81f991dd2`  
		Last Modified: Tue, 13 Dec 2022 23:51:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9d034b6762cd43683e1a06d639dc882ef3570cd611b77a89c8394fafaf65fe`  
		Last Modified: Wed, 14 Dec 2022 03:24:23 GMT  
		Size: 574.5 KB (574465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8215b7582705be1ad8d16db3ef1a535c50f8e45f41f4fcdac2101731324c14a`  
		Last Modified: Fri, 16 Dec 2022 23:20:03 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1b7a38a52d0062b91d18baac3fd3266b981d291d3febb5c60de81d0f8cb1c5`  
		Last Modified: Fri, 16 Dec 2022 23:20:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdb1531928831dd35358fba38e8a15c6b6e450ba98920295e38b73ec8e6be8c`  
		Last Modified: Fri, 16 Dec 2022 23:20:14 GMT  
		Size: 54.6 MB (54647048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
